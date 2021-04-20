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
[ 4588.009004] CMPE 283 Assignment 1 Module Start
[ 4588.014101] Basic Controls MSR: 0x0
[ 4588.017873] Pinbased Controls MSR: 0x0
[ 4588.022041]   External Interrupt Exiting: Can set=No, Can clear=Yes
[ 4588.028883]   NMI Exiting: Can set=No, Can clear=Yes
[ 4588.034123]   Virtual NMIs: Can set=No, Can clear=Yes
[ 4588.039583]   Activate VMX Preemption Timer: Can set=No, Can clear=Yes
[ 4588.046536]   Process Posted Interrupts: Can set=No, Can clear=Yes
[ 4588.052888] procbased Controls MSR: 0x0
[ 4588.058361]   Interrupt-window: Can set=No, Can clear=Yes
[ 4588.064146]   Use TSC offsetting: Can set=No, Can clear=Yes
[ 4588.071509]   HLT exiting: Can set=No, Can clear=Yes
[ 4588.076851]   INVLPG exiting: Can set=No, Can clear=Yes
[ 4588.082429]   MWAIT exiting: Can set=No, Can clear=Yes
[ 4588.088170]   RDPMC exiting: Can set=No, Can clear=Yes
[ 4588.093655]   RDTSC exiting: Can set=No, Can clear=Yes
[ 4588.100578]   CR3-load exiting: Can set=No, Can clear=Yes
[ 4588.106295]   CR3-store exiting: Can set=No, Can clear=Yes
[ 4588.112031]   CR8-load exiting: Can set=No, Can clear=Yes
[ 4588.117827]   CR8-store exiting: Can set=No, Can clear=Yes
[ 4588.123827]   Use TPR shadow: Can set=No, Can clear=Yes
[ 4588.129240]   NMI-window exiting: Can set=No, Can clear=Yes
[ 4588.136613]   MOV-DR exiting: Can set=No, Can clear=Yes
[ 4588.142521]   Unconditional I/O: Can set=No, Can clear=Yes
[ 4588.148601]   Use I/O bitmaps: Can set=No, Can clear=Yes
[ 4588.154319]   Monitor trap flag: Can set=No, Can clear=Yes
[ 4588.160271]   Use MSR Bitmaps: Can set=No, Can clear=Yes
[ 4588.165760]   MONITOR exiting: Can set=No, Can clear=Yes
[ 4588.173636]   PAUSE exiting: Can set=No, Can clear=Yes
[ 4588.179381]   Activate secondary controls: Can set=No, Can clear=Yes
[ 4588.188846] Secondary Processor-Based Controls MSR: 0x0
[ 4588.195805]   Virtualize APIC accesses: Can set=No, Can clear=Yes
[ 4588.202428]   Enable EPT: Can set=No, Can clear=Yes
[ 4588.207794]   Descriptor-table exiting: Can set=No, Can clear=Yes
[ 4588.214134]   Enable RDTSCP: Can set=No, Can clear=Yes
[ 4588.219503]   Virtualize x2APIC mode: Can set=No, Can clear=Yes
[ 4588.227422]   Enable VPID: Can set=No, Can clear=Yes
[ 4588.233058]   WBINVD exiting: Can set=No, Can clear=Yes
[ 4588.238618]   Unrestricted guest: Can set=No, Can clear=Yes
[ 4588.245911]   APIC-register virtualization: Can set=No, Can clear=Yes
[ 4588.252982]   Virtual-interrupt delivery: Can set=No, Can clear=Yes
[ 4588.261051]   PAUSE-loop exiting: Can set=No, Can clear=Yes
[ 4588.267257]   RDRAND exiting: Can set=No, Can clear=Yes
[ 4588.274270]   Enable INVPCID: Can set=No, Can clear=Yes
[ 4588.279887]   Enable VM functions: Can set=No, Can clear=Yes
[ 4588.286096]   VMCS shadowing: Can set=No, Can clear=Yes
[ 4588.292076]   Enable ENCLS exiting: Can set=No, Can clear=Yes
[ 4588.298893]   RDSEED exiting: Can set=No, Can clear=Yes
[ 4588.304277]   Enable PML: Can set=No, Can clear=Yes
[ 4588.309598]   EPT-violation: Can set=No, Can clear=Yes
[ 4588.315494]   Conceal VMX nonroot operation from Intel PT: Can set=No, Can clear=Yes
[ 4588.323574]   Enable XSAVES/XRSTORS: Can set=No, Can clear=Yes
[ 4588.329810]   Mode-based execute control for EPT: Can set=No, Can clear=Yes
[ 4588.337057]   Sub-page write permissions for EPT: Can set=No, Can clear=Yes
[ 4588.344356]   Intel PT uses guest physical addresses: Can set=No, Can clear=Yes
[ 4588.352351]   Use TSC scaling: Can set=No, Can clear=Yes
[ 4588.359277]   Enable user wait and pause: Can set=No, Can clear=Yes
[ 4588.365958]   Enable ENCLV exiting: Can set=No, Can clear=Yes
[ 4588.372342] VM Exit Controls MSR: 0x0
[ 4588.376134]   Save debug controls: Can set=No, Can clear=Yes
[ 4588.383434]   Host address- space size: Can set=No, Can clear=Yes
[ 4588.389885]   Load IA32_PERF_GLOB AL_CTRL: Can set=No, Can clear=Yes
[ 4588.396509]   Acknowledge interrupt on exit: Can set=No, Can clear=Yes
[ 4588.403311]   Save IA32_PAT: Can set=No, Can clear=Yes
[ 4588.408987]   Load IA32_PAT: Can set=No, Can clear=Yes
[ 4588.414638]   Save IA32_EFER: Can set=No, Can clear=Yes
[ 4588.421968]   Load IA32_EFER: Can set=No, Can clear=Yes
[ 4588.427889]   Save VMX-preemption timer value: Can set=No, Can clear=Yes
[ 4588.435386]   Clear IA32_BNDCFGS: Can set=No, Can clear=Yes
[ 4588.442862]   Conceal VM exits from Intel PT: Can set=No, Can clear=Yes
[ 4588.449680]   Clear IA32_RTIT_CTL: Can set=No, Can clear=Yes
[ 4588.455674]   Load CET state: Can set=No, Can clear=Yes
[ 4588.461124]   Load PKRS: Can set=No, Can clear=Yes
[ 4588.466172] VM Entry Controls MSR: 0x0
[ 4588.470151]   Load debug controls: Can set=No, Can clear=Yes
[ 4588.477503]   IA-32e mode guest: Can set=No, Can clear=Yes
[ 4588.483764]   Entry to SMM: Can set=No, Can clear=Yes
[ 4588.489139]   Deactivate dual-monitor treatment: Can set=No, Can clear=Yes
[ 4588.497873]   Load IA32_PERF_GLOBAL_CTRL: Can set=No, Can clear=Yes
[ 4588.504553]   Load IA32_PAT: Can set=No, Can clear=Yes
[ 4588.510190]   Load IA32_EFER: Can set=No, Can clear=Yes
[ 4588.515572]   Load IA32_BNDCFGS: Can set=No, Can clear=Yes
[ 4588.521860]   Conceal VM entries from Intel PT: Can set=No, Can clear=Yes
[ 4588.528998]   Load IA32_RTIT_CTL: Can set=No, Can clear=Yes
[ 4588.534930]   Load CET state: Can set=No, Can clear=Yes
[ 4588.540344]   Load PKRS: Can set=No, Can clear=Yes
```
