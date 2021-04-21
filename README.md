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
[   81.088906] CMPE 283 Assignment 1 Module Start
[   81.094432] Basic Controls MSR: 0xd8100011e57ed0
[   81.100614] Pinbased Controls MSR: 0x3f00000016
[   81.106823]   External Interrupt Exiting: Can set=Yes, Can clear=Yes
[   81.114838]   NMI Exiting: Can set=Yes, Can clear=Yes
[   81.121393]   Virtual NMIs: Can set=Yes, Can clear=Yes
[   81.128651]   Activate VMX Preemption Timer: Can set=No, Can clear=Yes
[   81.136681]   Process Posted Interrupts: Can set=No, Can clear=Yes
[   81.144741] procbased Controls MSR: 0xf7b9fffe04006172
[   81.151384]   Interrupt-window: Can set=Yes, Can clear=Yes
[   81.158569]   Use TSC offsetting: Can set=Yes, Can clear=Yes
[   81.167033]   HLT exiting: Can set=Yes, Can clear=Yes
[   81.173603]   INVLPG exiting: Can set=Yes, Can clear=Yes
[   81.180651]   MWAIT exiting: Can set=Yes, Can clear=Yes
[   81.187484]   RDPMC exiting: Can set=Yes, Can clear=Yes
[   81.194290]   RDTSC exiting: Can set=Yes, Can clear=Yes
[   81.201108]   CR3-load exiting: Can set=Yes, Can clear=Yes
[   81.208187]   CR3-store exiting: Can set=Yes, Can clear=Yes
[   81.215261]   CR8-load exiting: Can set=Yes, Can clear=Yes
[   81.222253]   CR8-store exiting: Can set=Yes, Can clear=Yes
[   81.229337]   Use TPR shadow: Can set=Yes, Can clear=Yes
[   81.236251]   NMI-window exiting: Can set=No, Can clear=Yes
[   81.243339]   MOV-DR exiting: Can set=Yes, Can clear=Yes
[   81.250240]   Unconditional I/O: Can set=Yes, Can clear=Yes
[   81.257326]   Use I/O bitmaps: Can set=Yes, Can clear=Yes
[   81.264518]   Monitor trap flag: Can set=No, Can clear=Yes
[   81.271680]   Use MSR Bitmaps: Can set=Yes, Can clear=Yes
[   81.278583]   MONITOR exiting: Can set=Yes, Can clear=Yes
[   81.285563]   PAUSE exiting: Can set=Yes, Can clear=Yes
[   81.292297]   Activate secondary controls: Can set=Yes, Can clear=Yes
[   81.298943] VM Exit Controls MSR: 0x3fefff00036dfb
[   81.303852]   Save debug controls: Can set=Yes, Can clear=Yes
[   81.309713]   Host address- space size: Can set=Yes, Can clear=Yes
[   81.316029]   Load IA32_PERF_GLOB AL_CTRL: Can set=No, Can clear=Yes
[   81.322494]   Acknowledge interrupt on exit: Can set=Yes, Can clear=Yes
[   81.329506]   Save IA32_PAT: Can set=Yes, Can clear=Yes
[   81.335097]   Load IA32_PAT: Can set=Yes, Can clear=Yes
[   81.340436]   Save IA32_EFER: Can set=Yes, Can clear=Yes
[   81.345862]   Load IA32_EFER: Can set=Yes, Can clear=Yes
[   81.351308]   Save VMX-preemption timer value: Can set=No, Can clear=Yes
[   81.358524]   Clear IA32_BNDCFGS: Can set=No, Can clear=Yes
[   81.364210]   Conceal VM exits from Intel PT: Can set=No, Can clear=Yes
[   81.370939]   Clear IA32_RTIT_CTL: Can set=No, Can clear=Yes
[   81.376780]   Load CET state: Can set=No, Can clear=Yes
[   81.382120]   Load PKRS: Can set=No, Can clear=Yes
[   81.387024] VM Entry Controls MSR: 0xd3ff000011fb
[   81.391840]   Load debug controls: Can set=Yes, Can clear=Yes
[   81.397825]   IA-32e mode guest: Can set=Yes, Can clear=Yes
[   81.403528]   Entry to SMM: Can set=No, Can clear=Yes
[   81.408783]   Deactivate dual-monitor treatment: Can set=No, Can clear=Yes
[   81.415868]   Load IA32_PERF_GLOBAL_CTRL: Can set=No, Can clear=Yes
[   81.422337]   Load IA32_PAT: Can set=Yes, Can clear=Yes
[   81.428017]   Load IA32_EFER: Can set=Yes, Can clear=Yes
[   81.433454]   Load IA32_BNDCFGS: Can set=No, Can clear=Yes
[   81.439062]   Conceal VM entries from Intel PT: Can set=No, Can clear=Yes
[   81.445969]   Load IA32_RTIT_CTL: Can set=No, Can clear=Yes
[   81.451657]   Load CET state: Can set=No, Can clear=Yes
[   81.456994]   Load PKRS: Can set=No, Can clear=Yes
```
