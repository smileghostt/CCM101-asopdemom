The following markdown file presents the findings regarding the system used, it is sorted in order for readability compared to the screenshot in which the md file has information copy pasted on. Any inconsistencies is because I have done my best to ensure that the md file is proper

# Linux Distribution 🐧
>This is where information regarding the linux distro lies. The use of commands such as `cat` allows us to read files that may contain information regarding our OS. The complex version gives us the full information regarding our distribution. For a more simplified version that doesn't require a PATH, use `lsb_release -a`, which presents the linux standard base release with the flag `-a` indicating that all information is to be provided.

## complex 📜
**asopdemom@ubuntu**:~$ `cat /etc/os-release`\
*PRETTY_NAME*="Ubuntu 24.04.4 LTS"\
*NAME*="Ubuntu"\
*VERSION_ID*="24.04"\
*VERSION*="24.04.4 LTS (Noble Numbat)"\
*VERSION_CODENAME*=noble\
*ID*=ubuntu\
*ID_LIKE*=debian\
*HOME_URL*="https://www.ubuntu.com/"\
*SUPPORT_URL*="https://help.ubuntu.com/"\
*BUG_REPORT_URL*="https://bugs.launchpad.net/ubuntu/"\
*PRIVACY_POLICY_URL*="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"\
*UBUNTU_CODENAME*=noble\
*LOGO*=ubuntu-logo

## simplified 📝
**asopdemom@ubuntu**:~$ `lsb_release -a`\
No LSB modules are available.\
*Distributor ID*: Ubuntu\
*Description*:    Ubuntu 24.04.4 LTS\
*Release*:        24.04\
*Codename*:       noble

# Kernel Version ⚙️
> This segment presents the kernel version itself. Fun fact! Did you know that Linux itself is not the OS but the kernel? Linux itself is the core of every Linux distribution (the OS). In order to find out the kernel version of the Killercoda instance we have, we use `uname`. Using the flag `-a` dumps all information, while `-r` filters it to only the version of the kernel.

## complex 📜
**asopdemom@ubuntu**:~\$ `uname -a`\
Linux ubuntu 6.8.0-136-generic #136-Ubuntu SMP PREEMPT_DYNAMIC Wed Jul  1 21:53:05 UTC 2026 x86_64 x86_64 x86_64 GNU/Linux
## simplified 📝
**asopdemom@ubuntu**:~$ `uname -r`\
6.8.0-136-generic\

# CPU Information
> The CPU information can easily be obtained by using the command `lscpu`. This is a standard Linux command that provides you the CPU architecture from multiple libraries and paths. It is a quick way to get information regarding your CPU albeit rather massive.

**asopdemom@ubuntu**:~$ `lscpu`\
*Architecture*:                x86_64\
*CPU op-mode(s)*:            32-bit, 64-bit\
&emsp;*Address sizes*:             46 bits physical, 48 bits virtual\
&emsp;*Byte Order*:                Little Endian\
*CPU(s)*:                      1\
&emsp;*On-line CPU(s) list*:       0\
*Vendor ID*:                   GenuineIntel\
&emsp;*Model name*:                Intel Xeon E312xx (Sandy Bridge, IBRS update)\
&emsp;&emsp;*CPU family*:              6\
&emsp;&emsp;*Model*:                   42\
&emsp;&emsp;*Thread(s) per core*:      1\
&emsp;&emsp;*Core(s) per socket*:      1\
&emsp;&emsp;*Socket(s)*:               1\
&emsp;&emsp;*Stepping*:                1\
&emsp;&emsp;*BogoMIPS*:                7199.92\
&emsp;&emsp;*Flags*:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm constant_tsc rep_good nopl xtopology cpu\
&emsp;&emsp;id tsc_known_freq pni pclmulqdq ssse3 cx16 pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ibrs ibpb\
&emsp;&emsp;stibp tsc_adjust xsaveopt arat md_clear\
*Virtualization features*:     
&emsp;*Hypervisor vendor*:         KVM\
&emsp;*Virtualization type*:       full\
*Caches (sum of all)*:         
&emsp;*L1d*:                       32 KiB (1 instance)\
&emsp;*L1i*:                       32 KiB (1 instance)\
&emsp;*L2*:                        4 MiB (1 instance)\
&emsp;*L3*:                        16 MiB (1 instance)\
*NUMA*:                        
&emsp;*NUMA node(s)*:              1\
&emsp;*NUMA node0 CPU(s)*:         0\
*Vulnerabilities*:             
&emsp;*Gather data sampling*:      Not affected\
&emsp;*Indirect target selection*: Mitigation; Aligned branch/return thunks\
&emsp;*Itlb multihit*:             KVM: Mitigation: VMX unsupported\
&emsp;*L1tf*:                      Mitigation; PTE Inversion\
&emsp;*Mds*:                       Mitigation; Clear CPU buffers; SMT Host state unknown\
&emsp;*Meltdown*:                  Mitigation; PTI\
&emsp;*Mmio stale data*:           Unknown: No mitigations\
&emsp;*Reg file data sampling*:    Not affected\
&emsp;*Retbleed*:                  Not affected\
&emsp;*Spec rstack overflow*:      Not affected\
&emsp;*Spec store bypass:*         Mitigation; Speculative Store Bypass disabled via prctl\
&emsp;*Spectre v1*:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization\
&emsp;*Spectre v2*:                Mitigation; Retpolines; IBPB conditional; IBRS_FW; STIBP disabled;\ RSB filling; PBRSB-eIBRS Not affected; BHI Retpoline\
&emsp;*Srbds*:                     Not affected\
&emsp;*Tsa*:                       Not affected\
&emsp;*Tsx async abort*:           Not affected\
&emsp;*Vmscape*:                   Not affected

# Total Memory 🧠
> In order to get your total memory, the command `free` can provide you with information about your total memory. This process however won't be readable for humans, and in order to make it readable for you, add the flag `-h` right after `free`.

**asopdemom@ubuntu**:~$ `free -h`\
|   | total |       used |       free     | shared | buff/cache |  available|
|-|-|-|-|-|-|-|
|Mem:|           1.9Gi|       425Mi|       844Mi |      1.1Mi|       801Mi|       1.4Gi
|Swap:|          1.0Gi |         0B |      1.0Gi|

# Available Disk Space 💾
> The command `df` provides information regarding disk space, with the name literally being an abbreviation of disk free. Just like `free`, `df` is not in human readable information and must have the `-h` flag (human flag) in order to indicate that it should be human readable.

**asopdemom@ubuntu**:~$ `df -h`\
|Filesystem      |Size  |Used |Avail |Use% |Mounted on|
|-|-|-|-|-|-|
|tmpfs           |191M |1012K  |190M   |1% |/run
|/dev/vda1        |19G  |5.4G   |13G  |30% |/
|tmpfs           |952M   |84K  |952M   |1% |/dev/shm
|tmpfs           |5.0M     |0  |5.0M   |0% |/run/lock
|/dev/vda16      |881M  |117M  |703M  |15% |/boot
|/dev/vda15      |105M  |6.2M   |99M   |6% |/boot/efi
|tmpfs           |191M  |8.0K  |191M   |1% |/run/user/1001