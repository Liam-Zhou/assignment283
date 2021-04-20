# CMPE283 assignment1:
1, For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched. (You may skip this question if you are doing the lab by yourself). 

I did this assignment by myself. Yilin Zhou (012571026) 

2, Describe in detail the steps you used to complete the assignment. Consider your reader to be someone skilled in software development but otherwise unfamiliar with the assignment. Good answers to this question will be recipes that someone can follow to reproduce your development steps. 
Step 1: created an instance in google cloud, configuring ssh connection, generating private and public key to connect to VM.

Step 2: set up environment to run the code. Installing the environment to compile the c file. 

Step 3: use git clone command to download linux source code and build the source code.

Step 4: after adding new features on existing c file, I send the file to VM using scp command, and run “make” command to create new module.

Step 5: after compiling the file, I used  “sudo /sbin/insmod cmpe283-1.ko ” to insert this file into kernel module, and check the print information using “Dmesg” command.

Here is the result:
```
[  449.160731] Pinbased Controls MSR: 0x0
[  449.168505]   External Interrupt Exiting: Can set=No, Can clear=Yes
[  449.177659]   NMI Exiting: Can set=No, Can clear=Yes
[  449.185707]   Virtual NMIs: Can set=No, Can clear=Yes
[  449.193576]   Activate VMX Preemption Timer: Can set=No, Can clear=Yes
[  449.204765]   Process Posted Interrupts: Can set=No, Can clear=Yes
[  449.217489] procbased Controls MSR: 0x0
[  449.223829]   Interrupt-window: Can set=No, Can clear=Yes
[  449.233735]   Use TSC offsetting: Can set=No, Can clear=Yes
[  449.246093]   HLT exiting: Can set=No, Can clear=Yes
[  449.257972]   INVLPG exiting: Can set=No, Can clear=Yes
[  449.269648]   MWAIT exiting: Can set=No, Can clear=Yes
[  449.280094]   RDPMC exiting: Can set=No, Can clear=Yes
[  449.288073]   RDTSC exiting: Can set=No, Can clear=Yes
[  449.299142]   CR3-load exiting: Can set=No, Can clear=Yes
[  449.307742]   CR3-store exiting: Can set=No, Can clear=Yes
[  449.320345]   CR8-load exiting: Can set=No, Can clear=Yes
[  449.331000]   CR8-store exiting: Can set=No, Can clear=Yes
[  449.341005]   Use TPR shadow: Can set=No, Can clear=Yes
[  449.352056]   NMI-window exiting: Can set=No, Can clear=Yes
[  449.360136]   MOV-DR exiting: Can set=No, Can clear=Yes
[  449.369228]   Unconditional I/O: Can set=No, Can clear=Yes
[  449.378649]   Use I/O bitmaps: Can set=No, Can clear=Yes
[  449.388306]   Monitor trap flag: Can set=No, Can clear=Yes
[  449.396848]   Use MSR Bitmaps: Can set=No, Can clear=Yes
[  449.407039]   MONITOR exiting: Can set=No, Can clear=Yes
[  449.416170]   PAUSE exiting: Can set=No, Can clear=Yes
[  449.424289]   Activate secondary controls: Can set=No, Can clear=Yes
[  449.434562] Secondary Processor-Based Controls MSR: 0x0
[  449.443641]   Virtualize APIC accesses: Can set=No, Can clear=Yes
[  449.456417]   Enable EPT: Can set=No, Can clear=Yes
[  449.465075]   Descriptor-table exiting: Can set=No, Can clear=Yes
[  449.475633]   Enable RDTSCP: Can set=No, Can clear=Yes
[  449.485139]   Virtualize x2APIC mode: Can set=No, Can clear=Yes
[  449.496478]   Enable VPID: Can set=No, Can clear=Yes
[  449.508649]   WBINVD exiting: Can set=No, Can clear=Yes
[  449.520065]   Unrestricted guest: Can set=No, Can clear=Yes
[  449.530095]   APIC-register virtualization: Can set=No, Can clear=Yes
[  449.539849]   Virtual-interrupt delivery: Can set=No, Can clear=Yes
[  449.553580]   PAUSE-loop exiting: Can set=No, Can clear=Yes
[  449.567618]   RDRAND exiting: Can set=No, Can clear=Yes
[  449.577091]   Enable INVPCID: Can set=No, Can clear=Yes
[  449.589377]   Enable VM functions: Can set=No, Can clear=Yes
[  449.602247]   VMCS shadowing: Can set=No, Can clear=Yes
[  449.612608]   Enable ENCLS exiting: Can set=No, Can clear=Yes
[  449.626240]   RDSEED exiting: Can set=No, Can clear=Yes
[  449.637009]   Enable PML: Can set=No, Can clear=Yes
[  449.645639]   EPT-violation: Can set=No, Can clear=Yes
[  449.653913]   Conceal VMX nonroot operation from Intel PT: Can set=No, Can clear=Yes
[  449.667186]   Enable XSAVES/XRSTORS: Can set=No, Can clear=Yes
[  449.677525]   Mode-based execute control for EPT: Can set=No, Can clear=Yes
[  449.688568]   Sub-page write permissions for EPT: Can set=No, Can clear=Yes
[  449.702106]   Intel PT uses guest physical addresses: Can set=No, Can clear=Yes
[  449.715809]   Use TSC scaling: Can set=No, Can clear=Yes
[  449.726467]   Enable user wait and pause: Can set=No, Can clear=Yes
[  449.736890]   Enable ENCLV exiting: Can set=No, Can clear=Yes
[  449.751132] VM Exit Controls MSR: 0x0
[  449.759237]   Save debug controls: Can set=No, Can clear=Yes
[  449.772177]   Host address- space size: Can set=No, Can clear=Yes
[  449.785664]   Load IA32_PERF_GLOB AL_CTRL: Can set=No, Can clear=Yes
[  449.795756]   Acknowledge interrupt on exit: Can set=No, Can clear=Yes
[  449.805842]   Save IA32_PAT: Can set=No, Can clear=Yes
[  449.815862]   Load IA32_PAT: Can set=No, Can clear=Yes
[  449.823609]   Save IA32_EFER: Can set=No, Can clear=Yes
[  449.832593]   Load IA32_EFER: Can set=No, Can clear=Yes
[  449.842513]   Save VMX-preemption timer value: Can set=No, Can clear=Yes
[  449.856569]   Clear IA32_BNDCFGS: Can set=No, Can clear=Yes
[  449.867543]   Conceal VM exits from Intel PT: Can set=No, Can clear=Yes
[  449.882629]   Clear IA32_RTIT_CTL: Can set=No, Can clear=Yes
[  449.894447]   Load CET state: Can set=No, Can clear=Yes
[  449.905745]   Load PKRS: Can set=No, Can clear=Yes
[  449.914915] VM Entry Controls MSR: 0x0
[  449.922040]   Load debug controls: Can set=No, Can clear=Yes
[  449.934548]   IA-32e mode guest: Can set=No, Can clear=Yes
[  449.942941]   Entry to SMM: Can set=No, Can clear=Yes
[  449.951832]   Deactivate dual-monitor treatment: Can set=No, Can clear=Yes
[  449.963988]   Load IA32_PERF_GLOBAL_CTRL: Can set=No, Can clear=Yes
[  449.978992]   Load IA32_PAT: Can set=No, Can clear=Yes
[  449.989101]   Load IA32_EFER: Can set=No, Can clear=Yes
[  449.996350]   Load IA32_BNDCFGS: Can set=No, Can clear=Yes
[  450.004300]   Conceal VM entries from Intel PT: Can set=No, Can clear=Yes
[  450.013246]   Load IA32_RTIT_CTL: Can set=No, Can clear=Yes
[  450.020537]   Load CET state: Can set=No, Can clear=Yes
[  450.029438]   Load PKRS: Can set=No, Can clear=Yes
```
