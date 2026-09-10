# Operating System 🖥️

**root@ubuntu:~$ uname -a**\
Linux ubuntu 6.8.0-138-generic #138-Ubuntu SMP PREEMPT_DYNAMIC Fri Jul 31 22:41:49 UTC 2026 x86_64 x86_64 x86_64 GNU/Linux

# CPU Information 🧠

**root@ubuntu:~$ lscpu**\
Architecture:                x86_64\
&emsp;CPU op-mode(s):            32-bit, 64-bit\
&emsp;Address sizes:             39 bits physical, 48 bits virtual\
&emsp;Byte Order:                Little Endian\
CPU(s):                      1\
&emsp;On-line CPU(s) list:       0\
Vendor ID:                   GenuineIntel\
&emsp;  BIOS Vendor ID:            Red Hat\
&emsp;  Model name:                Intel Xeon E312xx (Sandy Bridge, IBRS update)\
&emsp;&emsp;    BIOS Model name:         RHEL-9.6.0 PC (Q35 + ICH9, 2009)  CPU @ 2.0GHz\
&emsp;&emsp;    BIOS CPU family:         1\
&emsp;&emsp;    CPU family:              6\
&emsp;&emsp;    Model:                   42\
&emsp;&emsp;    Thread(s) per core:      1\
&emsp;&emsp;    Core(s) per socket:      1\
&emsp;&emsp;    Socket(s):               1\
&emsp;&emsp;    Stepping:                1\
&emsp;&emsp;BogoMIPS:                7008.00\
&emsp;&emsp;Flags:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm constant_tsc rep_good nopl xtopology cpu
                             id tsc_known_freq pni pclmulqdq ssse3 cx16 pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ibrs ibpb 
                             stibp tsc_adjust xsaveopt arat md_clear\
Virtualization features:     \
&emsp;  Hypervisor vendor:         KVM\
&emsp;  Virtualization type:       full\
Caches (sum of all):         \
&emsp;  L1d:                       32 KiB (1 instance)\
&emsp;  L1i:                       32 KiB (1 instance)\
&emsp;  L2:                        4 MiB (1 instance)\
&emsp;  L3:                        16 MiB (1 instance)\
NUMA:                        \
&emsp;  NUMA node(s):              1\
&emsp;  NUMA node0 CPU(s):         0\
Vulnerabilities:             \
&emsp;  Gather data sampling:      Not affected\
&emsp;  Indirect target selection: Mitigation; Aligned branch/return thunks\
&emsp;  Itlb multihit:             KVM: Mitigation: VMX unsupported\
&emsp;  L1tf:                      Mitigation; PTE Inversion\
&emsp;  Mds:                       Mitigation; Clear CPU buffers; SMT Host state unknown\
&emsp;  Meltdown:                  Mitigation; PTI\
&emsp;  Mmio stale data:           Unknown: No mitigations\
&emsp;  Reg file data sampling:    Not affected\
&emsp;  Retbleed:                  Not affected\
&emsp;  Spec rstack overflow:      Not affected\
&emsp;  Spec store bypass:         Mitigation; Speculative Store Bypass disabled via prctl\
&emsp;  Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitiz
                             ation\
&emsp;  Spectre v2:                Mitigation; Retpolines; IBPB conditional; IBRS_FW; STIBP disabl
                             ed; RSB filling; PBRSB-eIBRS Not affected; BHI Retpoline\
&emsp;  Srbds:                     Not affected\
&emsp;  Tsa:                       Not affected\
&emsp;  Tsx async abort:           Not affected\
&emsp;  Vmscape:                   Not affected

# Memory 📼

**root@ubuntu:~$ free -h**
|  | total | used | free | shared | buff/cache | available |
|---|---|---|---|---|---|---|
| Mem: | 1.9Gi | 418Mi | 860Mi | 1.1Mi | 791Mi | 1.4Gi |
| Swap: | 1.0Gi | 0B | 1.0Gi |  |  |  |

# Disk Space 💾

**root@ubuntu:~$ df -h**
| Filesystem | Size | Used | Avail | Use% | Mounted on |
|---|---|---|---|---|---|
| tmpfs | 191M | 996K | 190M | 1% | /run |
| /dev/vda1 | 19G | 5.4G | 13G | 30% | / |
| tmpfs | 952M | 84K | 952M | 1% | /dev/shm |
| tmpfs | 5.0M | 0 | 5.0M | 0% | /run/lock |
| /dev/vda16 | 881M | 117M | 703M | 15% | /boot |
| /dev/vda15 | 105M | 6.2M | 99M | 6% | /boot/efi |

**root@ubuntu:~$ lsblk**
| NAME | MAJ:MIN | RM | SIZE | RO | TYPE | MOUNTPOINTS |
| --- | --- | --- | --- | --- | --- | --- |
| vda | 253:0 | 0 | 20G | 0 | disk |  |
| ┣ vda1 | 253:1 | 0 | 19G | 0 | part | / |
| ┣ vda14 | 253:14 | 0 | 4M | 0 | part |  |
| ┣ vda15 | 253:15 | 0 | 106M | 0 | part | /boot/efi |
| ┗ vda16 | 259:0 | 0 | 913M | 0 | part | /boot |

### <u>If this Linux server were migrated to the cloud, which AWS, Azure, and GCP services could host it?</u>
- Considering this is merely just a Linux VM contained within a playground, for the most part the following services within AWS, Azure, and GCP can host this light Linux system:
    1. Amazon EC2
    2. Azure Virtual Machines
    3. Compute Engine