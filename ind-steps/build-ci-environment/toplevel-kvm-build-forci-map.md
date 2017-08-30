The map was made from this tree: <a href="../../../../tree/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/">../../../../tree/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/</a>
<br>
<code>* Status of all steps in dependency hierarchy with no pruning</code><br>
<code>&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/toplevel-kvm-build.sh#L6">1.0&nbsp;Setup&nbsp;VMs&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/kvm-vm-setup.sh#L11">1.1.0&nbsp;Basic&nbsp;setup&nbsp;for&nbsp;the&nbsp;CI&nbsp;VM&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/kvmsteps/vmdir-scripts/kvm-expand-fresh-image.sh#L6">1.1.1&nbsp;Expand&nbsp;VM&nbsp;image&nbsp;for&nbsp;civmdir&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/kvmsteps/vmdir-scripts/kvm-boot.sh#L39">1.1.2.0&nbsp;Boot&nbsp;KVM&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/kvmsteps/vmdir-scripts/kvm-boot.sh#L41">1.1.2.1&nbsp;Find&nbsp;qemu&nbsp;binary&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/kvmsteps/vmdir-scripts/kvm-boot.sh#L155">1.1.2.2&nbsp;Start&nbsp;KVM&nbsp;process&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/kvmsteps/vmdir-scripts/kvm-boot.sh#L194">1.1.2.3&nbsp;Wait&nbsp;for&nbsp;SSH&nbsp;port&nbsp;response&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/kvm-vm-setup.sh#L21">1.1.3&nbsp;Allow&nbsp;sudo&nbsp;for&nbsp;ubuntu&nbsp;user&nbsp;account,&nbsp;remove&nbsp;mtod&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/kvm-vm-setup.sh#L35">1.1.4&nbsp;Added&nbsp;step&nbsp;to&nbsp;give&nbsp;VMs&nbsp;8.8.8.8&nbsp;for&nbsp;dns&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/kvm-vm-setup.sh#L49">1.1.5&nbsp;Install&nbsp;git&nbsp;and&nbsp;supervisor&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/kvm-vm-setup.sh#L63">1.1.6&nbsp;Change&nbsp;hostname&nbsp;VM&nbsp;civmdir&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/toplevel-kvm-build.sh#L12">2.0&nbsp;Install&nbsp;Jupyternotebook&nbsp;Environment&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L9">2.1.0&nbsp;Cache&nbsp;used&nbsp;repositories&nbsp;locally&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L22">2.1.1&nbsp;Cache&nbsp;git&nbsp;repository:&nbsp;https:/&nbsp;/github.com/pyenv/pyenv.git&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L37">2.2.0&nbsp;Copy&nbsp;repositories&nbsp;to&nbsp;build&nbsp;VMs&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L46">2.2.1&nbsp;Copy&nbsp;pyenv&nbsp;repository&nbsp;into&nbsp;civmdir&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L65">2.3.0&nbsp;Install&nbsp;jupyter&nbsp;in&nbsp;main&nbsp;KVM&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L67">2.3.1&nbsp;Set&nbsp;up&nbsp;pyenv&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L84">2.3.2&nbsp;Install&nbsp;anaconda&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L100">2.3.3&nbsp;Install&nbsp;jupyter&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L113">2.3.4.0&nbsp;Configure&nbsp;jupyter&nbsp;server&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L121">2.3.4.1&nbsp;Generate&nbsp;default&nbsp;configuration&nbsp;file&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L134">2.3.4.2&nbsp;Set&nbsp;jupyter&nbsp;password&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L149">2.3.4.3&nbsp;Miscellaneous&nbsp;jupyter&nbsp;configuration&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L165">2.3.4.4&nbsp;Set&nbsp;up&nbsp;jupyter&nbsp;with&nbsp;supervisord&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L198">2.3.5.0&nbsp;Install&nbsp;extra&nbsp;kernels&nbsp;and&nbsp;extensions&nbsp;for&nbsp;jupyter&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L201">2.3.5.1&nbsp;Install&nbsp;bash_kernel&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L219">2.4.0&nbsp;Set&nbsp;up&nbsp;for&nbsp;CI&nbsp;notebook&nbsp;:::</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L222">2.4.1&nbsp;Set&nbsp;ssh&nbsp;key&nbsp;pair&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L237">2.4.2&nbsp;Upload&nbsp;repository&nbsp;to&nbsp;this&nbsp;KVM&nbsp;(not&nbsp;done)</a></code><br>
<code>&#42;&#42;&#42;&#42;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;&nbsp;--&nbsp;&nbsp;&nbsp;<a href="../../../../blob/5a0e6b36d40eb39c3e82adfbce79dbb27718a7ec/./ind-steps/build-ci-environment/build-ci-environment.sh#L256">2.4.3&nbsp;Upload&nbsp;notebooks&nbsp;to&nbsp;jupyter&nbsp;server&nbsp;(not&nbsp;done)</a></code><br>