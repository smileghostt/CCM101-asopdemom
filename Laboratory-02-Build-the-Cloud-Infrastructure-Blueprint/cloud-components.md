# Cloud Components ☁️
The following provides information on cloud components. You may use the following table of contents to skip to certain parts:

│\
├ [⚙️Compute Resources](#compute-resources-️)\
│&emsp;&emsp;├ [🧠 CPU](#cpu)\
│&emsp;&emsp;│&emsp;&nbsp;&nbsp;└ [ℹ️ Info](#info)\
│&emsp;&emsp;└ [📟 RAM](#ram)\
│&emsp;&emsp;&emsp;&emsp;└ [ℹ️ Info](#info)\
│\
├ [💾 Storage Resources](#storage-resources-)\
│&emsp;&emsp;└ [💿 Drives](#drives-)\
│&emsp;&emsp;&emsp;&emsp;└ [ℹ️ Info](#info-1)\
│\
├ [🛜 Network Resources](#network-resources-)\
│&emsp;&emsp;└ [📡 IP and Networks](#ip-and-networks)\
│&emsp;&emsp;&emsp;&emsp;└ [ℹ️ Info](#info-2)\
│\
└ [🖥️ Operating System](#operating-system-️)\
&emsp;&emsp;&emsp;&emsp;└ [🐧 Host Operating System](#host-operating-system)\
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;└ [ℹ️ Info](#info-3)

## Compute Resources ⚙️

### CPU 🧠
**root@ubuntu**_:~$_ lscpu\
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
&emsp;&emsp;    BogoMIPS:                7392.00\
&emsp;&emsp;    Flags:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov p
                             at pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm constant_tsc rep_good nopl xtopology cpuid tsc_known_freq pni pclmulqd
                             q ssse3 cx16 pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_time
                             r aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ibrs ib
                             pb stibp tsc_adjust xsaveopt arat md_clear\
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

---
### RAM 📟
**root@ubuntu**_:~$_ free -h\
|   | total |       used |       free     | shared | buff/cache |  available|
|-|-|-|-|-|-|-|
|Mem:           |1.9Gi|       416Mi|       866Mi|       1.1Mi|       788Mi|       1.5Gi|
|Swap:          |1.0Gi|          |0B|       1.0Gi|

### Info
The purpose of the CPU and RAM is within the whole process of computing. The CPU handles a lot of the computation that happens within a system. Having a powerful CPU provides you with a lot more computational power. Of course, this does not mean a good CPU is what you need within computation. Your RAM is also important in the computation process, as RAM allows for quicker computations and multitasking. These two become very important portions within cloud computing, as better CPU and RAM allows for quicker computation and heavier tasks to be handled with ease. Within the Killercoda environment, the Linux system's own RAM and CPU tells you the very limits of the infrastructure you are using within the computation side.
## Storage Resources 💾
### Drives 💿
**root@ubuntu**_:~$_ df -h\
|Filesystem      |Size|  Used| Avail| Use%| Mounted on|
|-|-|-|-|-|-|
|tmpfs           |191M|  996K|  190M|   1%| /run|
|/dev/vda1        |19G|  5.4G|   13G|  30%| /|
|tmpfs           |952M   |84K  |952M|   1% |/dev/shm|
|tmpfs           |5.0M     |0  |5.0M|   0% |/run/lock|
|/dev/vda16      |881M  |117M  |703M|  15% |/boot|
|/dev/vda15      |105M  |6.2M   |99M|   6% |/boot/efi|

### Info
Your storage space allows you to know just how much information can be stored within the system you are going to use. This is crucial for the system to function within cloud computing other than the CPU and RAM, as this allows for the ability to store information (which also means being able to bring it in and out of the cloud for your own needs). Within the Linux system, the filesystem provides you with information on how much you can store within it, so depending on what you may store, it may either fit or not.
## Network Resources 🛜
### IP and Networks 📡
**root@ubuntu**_:~$_ ip addr\
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000\
&emsp;    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00\
&emsp;    inet 127.0.0.1/8 scope host lo  \
&emsp;&emsp;       valid_lft forever preferred_lft forever\
&emsp;    inet6 ::1/128 scope host noprefixroute \
&emsp;&emsp;       valid_lft forever preferred_lft forever\
2: enp1s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1450 qdisc fq_codel state UP group default qlen 1000\
&emsp;    link/ether 26:93:68:01:23:0d brd ff:ff:ff:ff:ff:ff\
&emsp;    inet 172.30.1.2/24 brd 172.30.1.255 scope global dynamic noprefixroute enp1s0\
&emsp;&emsp;       valid_lft 86312371sec preferred_lft 75523171sec\
&emsp;    inet6 fe80::9472:c426:9bea:48af/64 scope link \
&emsp;&emsp;       valid_lft forever preferred_lft forever\
3: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1454 qdisc noqueue state DOWN group default\
&emsp;    link/ether 52:1b:e0:19:62:14 brd ff:ff:ff:ff:ff:ff\
&emsp;    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0\
&emsp;&emsp;       valid_lft forever preferred_lft forever

### Info
The network is another crucial part of cloud computing in general. Unlike the other three, this one is a lot less visible within cloud computing, as it does not look as obvious in hindsight until you look within the backbone of cloud computing in general. Network resources allow you to communicate within multiple systems, receive information from other systems, and overall reach others. Within the Killercoda environment, having a network allow for connection within the web, and it is especially needed when dealing with written information that you may wish to bring out of the Linux environment before the session expires.
## Operating System 🖥️
### Host Operating System 🐧
**root@ubuntu**_:~$_ hostnamectl\
&emsp; Static hostname: ubuntu\
&emsp;&emsp;       Icon name: computer-vm\
&emsp;&emsp;&emsp;         Chassis: vm 🖴\
&emsp;&emsp;      Machine ID: b4f277f01b6649c285b0f3d7f640d633\
&emsp;&emsp;&emsp;         Boot ID: 427475c3c963431db3a2a1938be8310f\
&emsp;  Virtualization: kvm\
Operating System: Ubuntu 24.04.4 LTS              \
&emsp;&emsp;&emsp;          Kernel: Linux 6.8.0-136-generic\
&emsp;    Architecture: x86-64\
&emsp; Hardware Vendor: KubeVirt\
&emsp;  Hardware Model: None\
Firmware Version: 1.16.3-4.el9\
&emsp;   Firmware Date: Tue 2014-04-01\
&emsp;    Firmware Age: 12y 4month 2w 5d
### Info
The operating system is the barebones of the software side within cloud computing. While very much more background than that of networking, as it is something we work in daily, it is not to be underestimated. The work of the OS is as the manager of a cloud computing system. It schedules tasks, and also, depending on the user, provide more freedom or ease of access depending on what OS you may be given. Within the Killercoda instance, we are aware it is a Linux environment that runs on Ubuntu. Ubuntu is one of the more accessible environments that even beginners can pick up. This makes it a feasible starting point for those getting into cloud computing.