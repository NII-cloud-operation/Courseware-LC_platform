## Clone repository:

```
$ git clone git@github.com:axsh/jupyter-platform-dev.git
$ cd jupyter-platform-dev
```

## Generic Build

For a generic build, the build directory can be create either before
or after the instance servers.  For the explanation here, let's start
with the build directory.

```
$ nodecount=3 ./ind-steps/build-jh-environment/toplevel-generic-build.sh-new /some/directory/path/buildname
## ( The value for the environment variable nodecount could be 1, 2 or some other reasonable integer. )
```

The ``toplevel-kvm-build.sh-new`` script creates a folder structure with the following files and contents:

```
$ head $(find /some/directory/path/buildname -name datadir.conf)
==> /some/directory/path/buildname/jhvmdir-node3/datadir.conf <==
VMIP=192.168.999.999  # replace with the private IP used between instances
publicip=180.123.999.999 # replace with IP used by this script
publicport=22   # if needed, replace with the port used by this script

==> /some/directory/path/buildname/jhvmdir-node2/datadir.conf <==
VMIP=192.168.999.999  # replace with the private IP used between instances
publicip=180.123.999.999 # replace with IP used by this script
publicport=22   # if needed, replace with the port used by this script

==> /some/directory/path/buildname/jhvmdir-node1/datadir.conf <==
VMIP=192.168.999.999  # replace with the private IP used between instances
publicip=180.123.999.999 # replace with IP used by this script
publicport=22   # if needed, replace with the port used by this script

==> /some/directory/path/buildname/jhvmdir/datadir.conf <==
VMIP=192.168.999.999  # replace with the private IP used between instances
publicip=180.123.999.999 # replace with IP used by this script
publicport=22   # if needed, replace with the port used by this script

==> /some/directory/path/buildname/jhvmdir-hub/datadir.conf <==
VMIP=192.168.999.999  # replace with the private IP used between instances
publicip=180.123.999.999 # replace with IP used by this script
publicport=22   # if needed, replace with the port used by this script

==> /some/directory/path/buildname/datadir.conf <==
node_list="node1 node2 node3"
```

Each ``jhvmdir*/datadir.conf`` file will contain information for one
instance.  (In this example, there are 5, i.e. three docker swarm
instances plus a hub instance, plus an instance for ansible.)

The ``publicip`` variable value should be replaced by an IP address
that can be used to ssh from the machine hosting the build directory
to the corresponding instance.  The ``publicport`` variable value
should point to the ssh port, if port forwarding is used to reach the
instance.

``VMIP`` should be a private IP address visible to all the other
instances.  Ssh must be possible to port 22 on this address.

The instances be a fresh install of Ubuntu 14.4 with an account with
user name "ubuntu".  It should also have the same public ssh key saved
at ``/home/ubuntu/.ssh/authorized_keys`` and
``/root/.ssh/authorized_keys``.  The corresponding private key should
be saved in the build directory in a file named ``sshkey``.  The
commands ``apt-get update``, then ``apt-get upgrade`` should be run on
each instance.

Once all the instances exist and all the information has been filled into
the ``datadir.conf" files, the following will install JupyterHub, taking
somewhat more than 60 minutes:

```
$ /path/to/just/a/little/disk/buildname/toplevel-generic-build.sh do
```

The build can be checked by running: 

```
$ /path/to/just/a/little/disk/buildname/toplevel-generic-build.sh check
```

## Build on KVM

The directory ``~/ubuntu-image-resources`` must exist in the home directory
and contain the following files:

```
$ cd ~/
$ cd ubuntu-image-resources/
$ ls -l
total 580760
-rw-r--r-- 8 k-oyakata k-oyakata 594675764 Dec  6 23:16 ubuntu-14-instance-build.img-sshkeys-update-upgrade.tar.gz
-rw-r--r-- 4 k-oyakata k-oyakata      1675 Jul 15  2016 ubuntu-14-instance-build.img-sshkeys-update-upgrade.sshkey
-rw-r--r-- 4 k-oyakata k-oyakata         7 Jul 15  2016 ubuntu-14-instance-build.img-sshkeys-update-upgrade.sshuser
```

The ``*.tar.gz`` file contains Ubuntu 14.04.1 LTS with a 242GB root
file system.  It was made by doing a fresh install from an ISO, then
``apt-get update``, then ``apt-get upgrade``.  Finally, a public key
was placed in both ``/home/ubuntu/.ssh/authorized_keys`` and
``/root/.ssh/authorized_keys``.  The private part of the key
pair is in the ``*.sshkey``.  The ``*.sshuser`` file just contains the
string "ubuntu", because that is the user name to use when doing ssh
to a VM booted from the image.

The next step is to make a build directory by using the toplevel-kvm-build.sh-new
in the repository like this:
```
$ ./ind-steps/build-jh-environment/toplevel-kvm-build.sh-new /some/directory/path/buildname
```
Be sure to substitute ``/some/directory/path`` with a path for a disk that
has 60GB or so of free disk space.

The above step quickly creates a new directory tree that includes this structure:
```
$ cd /some/directory/path/buildname
$ find -name datadir.conf
./datadir.conf
./jhvmdir/datadir.conf
./jhvmdir-hub/datadir.conf
./jhvmdir-node1/datadir.conf
./jhvmdir-node2/datadir.conf
```

Each ``jhvmdir*`` represents one of the 4 VMs for the build, and its ``datadir.conf``
gives configuration information used during building.  Additional information from
the build will be added to the appropriate ``datadir.conf``.

The actual build is done by running a script that is now inside the
build directory:

```
$ /some/directory/path/buildname/toplevel-kvm-build.sh do
```
The whole build takes about 60 to 90 minutes.

The following command can be used to verify which steps of the
build have completed. (The same as above, just change ``do`` to ``check``)

```
$ /some/directory/path/buildname/toplevel-kvm-build.sh check
```

The above command will output a list of steps similar to this:
https://github.com/axsh/jupyter-platform-dev/blob/master/ind-steps/build-jh-environment/toplevel-kvm-build-map.md

The build defaults to 2 docker swarm nodes.  This can be changed
with the ``nodecount`` environment variable.

```
$ nodecount=3 ./ind-steps/build-jh-environment/toplevel-kvm-build.sh-new /some/directory/path/buildname
```

## Build on AWS

Install awscli:  http://docs.aws.amazon.com/cli/latest/userguide/installing.html
Also make sure ``.aws/config`` and ``.aws/credentials`` are set up correctly.

Then:
```
$ ./ind-steps/build-jh-environment/toplevel-aws-build.sh-new /path/to/just/a/little/disk/buildname

$ /path/to/just/a/little/disk/buildname/toplevel-aws-build.sh check
$ /path/to/just/a/little/disk/buildname/toplevel-aws-build.sh do
```

(Some waits still need to be implemented, so repeating "toplevel-aws-build.sh do" several
times may be necessary.)

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
