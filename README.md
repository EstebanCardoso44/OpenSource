# OpenSource
# CARDOSO Esteban 
2
               total        used        free      shared  buff/cache   available
Mem:           3.8Gi       805Mi       2.2Gi       5.6Mi       1.1Gi       3.0Gi
Swap:          953Mi          0B       953Mi
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        79G   16G   59G  21% /
Architecture:                            x86_64
CPU op-mode(s):                          32-bit, 64-bit
Address sizes:                           39 bits physical, 48 bits virtual
Byte Order:                              Little Endian
CPU(s):                                  2
On-line CPU(s) list:                     0,1
Vendor ID:                               GenuineIntel
Model name:                              Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz
CPU family:                              6
Model:                                   126
Thread(s) per core:                      1
Core(s) per socket:                      2
Socket(s):                               1
Stepping:                                5
BogoMIPS:                                2380.80
Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid tsc_known_freq pni pclmulqdq ssse3 cx16 pcid sse4_1 sse4_2 movbe popcnt aes rdrand hypervisor lahf_lm abm 3dnowprefetch ibrs_enhanced fsgsbase bmi1 bmi2 invpcid rdseed adx clflushopt sha_ni arat md_clear flush_l1d arch_capabilities
Hypervisor vendor:                       KVM
Virtualization type:                     full
L1d cache:                               96 KiB (2 instances)
L1i cache:                               64 KiB (2 instances)
L2 cache:                                1 MiB (2 instances)
L3 cache:                                12 MiB (2 instances)
NUMA node(s):                            1
NUMA node0 CPU(s):                       0,1
Vulnerability Gather data sampling:      Not affected
Vulnerability Ghostwrite:                Not affected
Vulnerability Indirect target selection: Mitigation; Aligned branch/return thunks
Vulnerability Itlb multihit:             Not affected
Vulnerability L1tf:                      Not affected
Vulnerability Mds:                       Not affected
Vulnerability Meltdown:                  Not affected
Vulnerability Mmio stale data:           Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
Vulnerability Old microcode:             Not affected
Vulnerability Reg file data sampling:    Not affected
Vulnerability Retbleed:                  Mitigation; Enhanced IBRS
Vulnerability Spec rstack overflow:      Not affected
Vulnerability Spec store bypass:         Vulnerable
Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
Vulnerability Spectre v2:                Mitigation; Enhanced / Automatic IBRS; PBRSB-eIBRS SW sequence; BHI SW loop, KVM SW loop
Vulnerability Srbds:                     Unknown: Dependent on hypervisor status
Vulnerability Tsa:                       Not affected
Vulnerability Tsx async abort:           Not affected
Vulnerability Vmscape:                   Not affected
Do you want to install it? (N/y)System:
  Kernel: 6.18.12+kali-amd64 arch: x86_64 bits: 64 compiler: gcc v: 15.2.0
  Desktop: Xfce v: 4.20.1 Distro: Kali GNU/Linux 2026.1 kali-rolling
    base: Debian testing
Machine:
  Type: Virtualbox System: innotek GmbH product: VirtualBox v: 1.2
    serial: N/A
  Mobo: Oracle model: VirtualBox v: 1.2 serial: N/A Firmware: BIOS
    vendor: innotek GmbH v: VirtualBox date: 12/01/2006
Battery:
  ID-1: BAT0 charge: 50 Wh (100%) condition: 50/50 Wh (100%) volts: 10
    min: 10 model: innotek 1 status: full
CPU:
  Info: dual core model: Intel Core i5-1035G1 bits: 64 type: MCP
    arch: Ice Lake rev: 5 cache: L1: 160 KiB L2: 1024 KiB L3: 12 MiB
  Speed (MHz): avg: 1190 min/max: N/A cores: 1: 1190 2: 1190
    bogomips: 4761
  Flags-basic: ht lm nx pae sse sse2 sse3 sse4_1 sse4_2 ssse3
Graphics:
  Device-1: VMware SVGA II Adapter driver: vmwgfx v: 2.21.0.0
    bus-ID: 00:02.0
  Display: x11 server: X.Org v: 21.1.21 driver: X: loaded: modesetting
    unloaded: fbdev,vesa dri: swrast gpu: vmwgfx resolution: 799x600~60Hz
  API: EGL v: 1.5 drivers: kms_swrast,swrast platforms:
    active: gbm,x11,surfaceless,device inactive: wayland,device-0
  API: OpenGL v: 4.5 vendor: mesa v: 26.0.0-1 glx-v: 1.4
    direct-render: yes renderer: llvmpipe (LLVM 21.1.8 128 bits)
  Info: Tools: api: eglinfo,glxinfo de: xfce4-display-settings
    x11: xdriinfo, xdpyinfo, xprop, xrandr
Audio:
  Device-1: Intel 82801AA AC97 Audio vendor: Dell driver: snd_intel8x0
    v: kernel bus-ID: 00:05.0
  API: ALSA v: k6.18.12+kali-amd64 status: kernel-api
  Server-1: PipeWire v: 1.4.10 status: n/a (root, process)
Network:
  Device-1: Intel 82540EM Gigabit Ethernet driver: e1000 v: kernel
    port: d020 bus-ID: 00:03.0
  IF: eth0 state: up speed: 1000 Mbps duplex: full mac: <filter>
  Device-2: Intel 82371AB/EB/MB PIIX4 ACPI type: network bridge
    driver: piix4_smbus v: N/A port: N/A bus-ID: 00:07.0
Drives:
  Local Storage: total: 80.09 GiB used: 15.76 GiB (19.7%)
  ID-1: /dev/sda vendor: VirtualBox model: VBOX HARDDISK size: 80.09 GiB
Partition:
  ID-1: / size: 78.28 GiB used: 15.76 GiB (20.1%) fs: ext4 dev: /dev/sda1
Swap:
  ID-1: swap-1 type: file size: 953.7 MiB used: 0 KiB (0.0%) file: /swap
Sensors:
  Src: lm-sensors+/sys Message: No sensor data found using
    /sys/class/hwmon or lm-sensors.
Info:
  Memory: total: 4 GiB available: 3.83 GiB used: 907.1 MiB (23.1%)
  Processes: 188 Uptime: 10m Init: systemd
  Packages: 2873 Compilers: clang: 21.1.8 gcc: 15.2.0 Shell: Zsh v: 5.9
    inxi: 3.3.40
