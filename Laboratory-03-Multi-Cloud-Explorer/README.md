# Linux Server Investigation 

This document records the results of a Linux system investigation performed on a KillerCoda Playground instance, and discusses how the server could be migrated to the cloud.

## 1. Operating System

**Command used:**
```bash
cat /etc/os-release
```

**Output:**
```
PRETTY_NAME="Ubuntu 24.04.4 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.4 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
```



## 2. CPU Information

**Command used:**
```bash
lscpu
```

**Output:**
```
Architecture:                x86_64
  CPU op-mode(s):            32-bit, 64-bit
  Address sizes:             46 bits physical, 48 bits virtual
  Byte Order:                Little Endian
CPU(s):                      1
  On-line CPU(s) list:       0
Vendor ID:                   GenuineIntel
  BIOS Vendor ID:            Red Hat
  Model name:                Intel Xeon E312xx (Sandy Bridge, IBRS update)
    BIOS Model name:         RHEL-9.6.0 PC (Q35 + ICH9, 2009)  CPU @ 2.0GHz
    BIOS CPU family:         1
    CPU family:              6
    Model:                   42
    Thread(s) per core:      1
    Core(s) per socket:      1
    Socket(s):               1
    Stepping:                1
    BogoMIPS:                7199.94
    Flags:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp 
                             lm constant_tsc rep_good nopl xtopology cpuid tsc_known_freq pni pclmulqdq ssse3 cx16 pcid sse4_1 sse4_2 x2apic popc
                             nt tsc_deadline_timer aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ibrs ibpb stibp tsc_adjust xsaveopt arat
                              md_clear
Virtualization features:     
  Hypervisor vendor:         KVM
  Virtualization type:       full
Caches (sum of all):         
  L1d:                       32 KiB (1 instance)
  L1i:                       32 KiB (1 instance)
  L2:                        4 MiB (1 instance)
  L3:                        16 MiB (1 instance)
NUMA:                        
  NUMA node(s):              1
  NUMA node0 CPU(s):         0
Vulnerabilities:             
  Gather data sampling:      Not affected
  Indirect target selection: Mitigation; Aligned branch/return thunks
  Itlb multihit:             KVM: Mitigation: VMX unsupported
  L1tf:                      Mitigation; PTE Inversion
  Mds:                       Mitigation; Clear CPU buffers; SMT Host state unknown
  Meltdown:                  Mitigation; PTI
  Mmio stale data:           Unknown: No mitigations
  Reg file data sampling:    Not affected
  Retbleed:                  Not affected
  Spec rstack overflow:      Not affected
  Spec store bypass:         Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:                Mitigation; Retpolines; IBPB conditional; IBRS_FW; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Retpol
                             ine
  Srbds:                     Not affected
  Tsa:                       Not affected
  Tsx async abort:           Not affected
  Vmscape:                   Not affected
```



## 3. Memory

**Command used:**
```bash
free -h
```

**Output:**
```
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       412Mi       867Mi       1.1Mi       791Mi       1.5Gi
Swap:          1.0Gi          0B       1.0Gi
```


## 4. Disk Space

**Command used:**
```bash
df -h
```

**Output:**
```
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M  996K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           952M   84K  952M   1% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
/dev/vda16      881M  117M  703M  15% /boot
/dev/vda15      105M  6.2M   99M   6% /boot/efi
root@ubuntu:~$ ^C
```


## 5. Cloud Migration: Which Services Could Host This Server?

If this Linux server were migrated to the cloud, its role as a general-purpose Linux VM maps directly onto the core virtual machine services of each major provider:

| Provider | Recommended Service | Notes |
|---|---|---|
| **AWS** | **Amazon EC2** (Elastic Compute Cloud) | Launch an EC2 instance matching the observed CPU/RAM specs (e.g., a `t3` or `m5` instance type), attach an EBS volume sized to match the observed disk space, and choose an AMI running the same Linux distribution identified in `/etc/os-release`. |
| **Microsoft Azure** | **Azure Virtual Machines** | Deploy a VM of comparable size (e.g., a `Bv2` or `Dv5`-series VM), using an Azure Managed Disk for storage and selecting a matching Linux image (Ubuntu, CentOS, etc.) from the Azure Marketplace. |
| **Google Cloud Platform** | **Compute Engine** | Create a Compute Engine VM instance with a matching machine type (e.g., `e2-medium` or `n2-standard`), a Persistent Disk sized to match observed disk usage, and the equivalent Linux OS image. |

**Summary:** All three providers offer a direct equivalent for hosting a plain Linux server as an IaaS virtual machine — EC2 (AWS), Azure Virtual Machines (Azure), and Compute Engine (GCP). The choice between them would depend on factors like existing cloud relationships, budget/pricing, required integrations (e.g., Microsoft ecosystem tools favor Azure), and whether the workload might later benefit from serverless or container-based services instead of a traditional VM.

