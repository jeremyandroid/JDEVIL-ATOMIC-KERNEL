JDEVIL-ATOMIC-KERNEL
====================

THIS IS A CUSTOM KERNEL FOR LINUX DEBIAN/UBUNTU BASED DISTROS. IT IS ALL ABOUT PERFORMANCE AND GIVES AMAZING RESULTS. 



This Kernel is custom built from source code by me under my internet name jeremyandroid and under copyrighted name JDEVIL. The specs listed are NOT for everyone or every computer. Be very careful on the listed below to make sure its compatible with your machine. This kernel is for performance only and will make a stock cooling machine run around 41C. This kernel is not recommend for Laptops as the default I/O is set at performance and hotplug is NOT supported. This kernel has all logging disabled. This Kernel has been slimmed as much as I could and with less overhead as possible to increase speed. I have noticed 2xs the speed on my machine versus the stock generic kernel.
Intel 64 bit only Machine only no other processor support(best suited for quad-core processors)
I have highly modified Kernel as following:
 JDEVIL CONFIG-TASK-DELAY: The standard time on collect information spent by a task waiting for system resources like CPU,synchronous block I/O completion and swapping has been cut by an aggressive 80%
JDEVIL CONFIG-TASK XACCT: This feature has been extended for the task of accounting data and then the send data file to the user for processing over the task set interface
JDEVIL CONFIG-TASK-TO-ACCOUNTING: The amount of room for the collect bytes of I/O storage for task has been added by an aggressive 70%
JDEVIL CONFIG-RCU-FANOUT-LEAF This leaf-level fanout of hierarchical implementation of RCU has been modified for a quicker trade of cache missed against lock contention.
JDEVIL RCU-FAST-HZ: DISABLED This tune permits CPUs to enter dynastic-idle state even if they have RCU callbacks queued. It will finish tasks at hand Because IM IMPATIENT and we are not concerned with energy efficiency 
JDEVIL CONFIG-NUMA-BALANCING: Added support for auto NUMA aware memory/task placement
JDEVIL CONFIG CPUSETS: This allows CPU sets to dynamically partition a system into sets of CPUs and memory nodes and assigning task to run only within those sets. Set size modified JDEVIL
JDEVIL CONFIG RELAY:DISABLED support or relay interface such as debugfs.
JDEVIL CONFIG BLK-DEV-INITRD: The initial RAM file system is a ram that is loaded faster by the boot loader and mounted as ROOT and will load JDEVIL modules faster.
JDEVIL SUPPORT FOR GZIP,BZIP2,LZMA,XS,LZO ram disks and optimize for size
JDEVIL CONFIG-UID16: This enables the legacy 16 it UID system call wrappers
JDEVIL CONFIG-SYSCTL-SYSCALL:DISABLED This uses binary paths that have been found challenging to maintain
JDEVIL CONFIG-KALLSYMS: DISABLED Will not print out symbolic crash information and symbolic stack backtracks. This allows less overhead.
JDEVIL CONFIG-KALLSMS-ALL:DISABLED Lowers size and overhead
JDEVIL CONFIG-ELF-CORE: Disabled support for core-dumps
JDEVIL CONFIG-SLUB-DEBUG: DISABLED For saving of code size no support for cache validation. Lets get to the point and keep things fast.
JDEVIL Many of the stock internal systems files have been moved to modules such as Profile system profiling, Dev/CPU/*/msr,Dev/CPU/*/cpuid,CPU microcode loading support
JDEVIL TIMER FREQUENCY Has been modified from the stock 250hz to 1000hz
JDEVIL CONFIG-KPROBES Allows faster trap at the kernel address and faster callback function
JDEVIL CONFIG-UPROBES Faster instrumentation of applications to establish unitrusive probes in the user space binaries and libraries.
JDEVIL CONFIG-MODULES As many modules as I could make are supported
JDEVIL CONFIG-ZONE-DMA: DISABLED This is for 32bit machines 
JDEVIL CONFIG-X86-X2APIC: DISABLED
JDEVIL CONFIG-X86-MPPARSE:DISABLED This is for old smp systems that don't have proper acpi support
JDEVIL CONFIG-X86-EXTENDED PLATFORM: DISABLED This kernel will only support standard PC platforms no other to keep overhead low code size down etc.
JDEVIL CONFIG-SCHED-OMIT-FRAME-POINTER:DISABLED This forces wchan values to recurse back to the caller function and provides more accurate wchan values but at the expenses of more scheduling overhead.
JDEVIL CONFIG-MEMTEST:DISABLED This takes away kernel parameter which allows a memtest to be set.
JDEVIL CONFIG-GGART-IOMMU: This provides support with many usb devices and usb 32 bit, flash drives etc.
JDEVIL CONFIG-CALGARY-IOMMU:Support for hardware IOMMUS needed for systems with more than 3gig of ram
JDEVIL DIRECT-GBPAGES: Allows the kernel linear mapping to use 1gb pages on cpus for faster mapping
JDEVIL CONFIG-NUMA: The kernel will try to allocate memory used by a CPU on the local memory controller of the CPU and add more numa awareness to the JDEVIL ATOMIC KERNEL
JDEVIL CONFIG-INTEL-NUMA: This is an old method that I believe to be faster for a multi amd chip set for node topology detection
JDEVIL-NUMA-EMU:DISABLED This is only useful for debugging
JDEVIL-NODES-SHIFT TUNE: This increases miry reserved to accommodate various tables.
JDEVIL-SPARSEMEM-VMEMMAP: Used to virtually mapped memmap to optimize pfn to page to pfn operations tuned aggressively.
JDEVIL CONFIG-MOVABLE-NODE: DISABLED This prevents memory device from a hotplug.
JDEVIL CONFIG-BALLOON-COMPACTION: This will reduce the number of contiguous memory blocks and improves memory defragmentation
JDEVIL CONFIG-MIGRATION: An aggressive tune to make migration of the physical location of pages of processes while the virtual addresses are not changed.
JDEVIL CONFIG-TRANSPARENT-HUGEPAGE: This allows the kernel to use huge pages and huge tib transparently to the applications whenever possible. This feature can improve computing in performance to certain applications by speeding up page faults during memory allocation, by reducing the number of tib misses and speeding up the pagetable walking JDEVIL MOD.
JDEVIL CONFIG.CLEANCACHE: This is a page-granularity victim cache for clean pages that the kernels pageframe replacement algorithm would like to keep around but cant since there isn't enough memory. So it the evicts it at an aggressive JDEVIL rate.
JDEVIL CONFIG-FRONTSWAP: Support for backing a store from a swap device.
JDEVIL -X86-RESERV-LOW :Reserved the amount of low memory to reserve the BIOS
JDEVIL -EFI SUPPORT:
JDEVIL CONFIG-EFI-STUB: This allows a bzimage to be loaded by efi firmware without the use of a boot loader for possible faster speed.
JDEVIL-HOTPLUG-CPU-DISABLED This forces cpus to stay on and not turn off or sleep NO HOTPLUG SUPPORT
JDEVIL CONFIG-PM-RUNTIME;DISABLED This is an energy saving low power feature we don't need on a desktop
JDEVIL I32-EMULATION: This includes a code to still use those old 32 bit programs you may have
JDEVIL-CONFIG-DEBUG-INFO: DISABLED This makes the kernel image larger with all the debugging info
JDEVIL CONFIG-EARLY-PRINTK: DISABLED I don't want to debug a crash before the console code is loaded
JDEVIL PREEMPTIBLE KERNEL LOW LATENCY DESKTOP CONFIGURATION
JDEVIL DISABLED:
Hibernation (aka 'suspend to disk')                           
  Default resume partition                                      
  Opportunistic sleep                                           
  User space wakeup sources interface                           
  Run-time PM core functionality                                
  Power Management Debug Support                                
  Enable work queue power-efficient mode by default              
  ACPI (Advanced Configuration and Power Interface) Support 
  JDEVIL CHANGED TO MODULES:
  -*- Kernel support for ELF binaries                               
      Kernel support for scripts starting with #!                   
      Kernel support for MISC binaries                              
      Enable core dump support                                      
      IA32 Emulation                                                
      IA32 a.out support                                          
      x32 ABI for 64-bit mode     
      Packet socket                                                 
      Packet: sockets monitoring interface                        
      Unix domain sockets                                           
      UNIX: socket monitoring interface                           
      Transformation user configuration interface                   
      Transformation sub policy support                             
      Transformation migrate database                               
      Transformation statistics                                     
      PF_KEY sockets                                                
      PF_KEY MIGRATE                                              
 
      TCP/IP networking                                             
      IP: multi casting                                            
      IP: advanced router                                         
      FIB TRIE statistics                                       
      IP: policy routing                                        
      IP: equal cost multi path                                  
      IP: verbose route monitoring                              
      IP: kernel level auto configuration                          
      IP: tunneling  
      
      IP: GRE demultiplexer                                       
      IP: GRE tunnels over IP                                     
      IP: broadcast GRE over IP                                 
      IP: multi cast routing                                       
      IP: multi cast policy routing                              
      IP: PIM-SM version 1 support                              
      IP: PIM-SM version 2 support                              
      IP: TCP syn cookie support                                   
      Virtual (secure) IP: tunneling  

      IP: IPComp transformation                                   
      IP: IPsec transport mode                                    
      IP: IPsec tunnel mode                                       
      IP: IPsec BEET mode                                         
      Large Receive Offload (ipv4/tcp)                            
      INET: socket monitoring interface                           
      UDP: socket monitoring interface                          
      TCP: advanced congestion control  --->                      
    TCP: MD5 Signature Option support (RFC2385)                 
   The IPv6 protocol  --->  
   Net Label subsystem support                                  
  Security Marking                                              
  Time stamping in PHY devices                                   
  Network packet filtering framework (Net filter)  --->          
  The DCCP Protocol  --->                                       
  The SCTP Protocol  --->                                       
  The    [ ]   RDS debugging messages                                      
  The TIPC Protocol  --->                                       
  Asynchronous Transfer Mode (ATM)                              
  Classical IP over ATM                                       
  Do NOT send ICMP if no neighbor                          
  LAN Emulation (LANE) support                                
  Multi-Protocol Over ATM (MPOA) support                    
  RFC1483/2684 Bridged protocols                              
  Per-VC 
IP filter kludge    
 [ ]   DECnet: router support                                      
     ANSI/IEEE 802.2 LLC type 2 Support                            
     The IPX protocol                                              
     IPX: Full internal IPX network                              
     Apple talk protocol support                                 
     Apple talk interfaces support                             
     IP to Apple talk-IP Encapsulation support                
     CCITT X.25 Packet Layer                                       
     LAPB Data Link Drive
     6lowpan support over IEEE 802.15.4                          
     Generic IEEE 802.15.4 Soft Networking Stack (mac802154)       
     QoS and/or fair queuing  --->                                
     Data Center Bridging support                                  
     DNS Resolver support                                          
     B.A.T.M.A.N. Advanced Meshing Protocol                        
     Bridge Loop Avoidance                                       
     Distributed ARP Table                                       
     Network Coding                       
     Amateur Radio support                                         
     Packet Radio protocols ***                              
     Amateur Radio AX.25 Level 2 protocol                        
     AX.25 DAMA Slave support                                  
     Amateur Radio NET/ROM protocol                            
     Amateur Radio X.25 PLP (Rose)                             
     AX.25 network device drivers  --->                        
     CAN bus subsystem to control vehicle and ONSTAR                                  
     Raw CAN Protocol (raw access with CAN-ID filtering)         
     Broadcast Manager CAN Protocol (with content filtering)     
     CAN Gateway/Router (with net link configuration)             
     CAN Device Drivers  --->                                    
                                
     NFC subsystem support                                         
     NFC Digital Protocol stack support                          
     NCI protocol support                                        
     NCI over SPI protocol support                             
     NFC HCI implementation                                      
     SHDLC link layer for HCI based NFC drivers                
   Near Field Communication (NFC) devices  --->                
                                                                      
    NVM Express block device                                    
    STEC S1120 Block Driver                                     
    OSD object-as-blkdev support                                
    Promise SATA SX8 support                                    
    RAM block device support                                    
    (16)    Default number of RAM disks                               
    (16384) Default RAM disk size (k bytes)                            
     Support XIP file systems on RAM block device               
     Packet writing on CD/DVD media                              
    ( Free buffers for data
CONFIG_BTRFS_FS:                                                                                                                                Btrfs is a general purpose copy-on-write file system with extents,       writable snapshotting, support for multiple devices and many more       features focused on fault tolerance, repair and easy administration.                                                                            The file system disk format is no longer unstable, and it's not          expected to change unless there are strong reasons to do so. If there   is a format change, file systems with a unchanged format will           continue to be mountable and usable by newer kernels.                                                                                           For more information, please see the web pages at                       HTTP://btrfs.wiki.kernel.org.                                                                                                                   To compile this file system support as a module, choose M here. The     module will be called btrfs.        
OCFS2 file system support                                     
     O2CB Kernel space Clustering                                 
     OCFS2 User space Clustering                                  
     OCFS2 statistics                                            
     OCFS2 logging support                                       
     OCFS2 expensive checks                                      
     Btrfs file system support                                      
     Btrfs POSIX Access Control Lists                            
     Btrfs with integrity check tool compiled in (DANGEROUS)     
     Btrfs will run sanity tests upon loading                    
 v(+) CONFIG_INTEL_TXT:                                                         Able to turn on many Intel features disabled by default because of the generic build default format. This option enables support for booting the kernel with the Trusted Boot (tboot) module. This will utilize Intel(R) Trusted Execution Technology to perform a measured launch of the kernel. If the system does not support Intel(R) TXT, this       will have no effect.                                                                                                                         Intel TXT will provide higher assurance of system configuration and initial state as well as data reset protection. This is used to create a robust initial kernel measurement and verification, which helps to ensure that kernel security mechanisms are functioning correctly. This level of protection requires a root of trust outside of the kernel itself.                   
  
 



























