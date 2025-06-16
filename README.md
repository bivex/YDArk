# YDArk

> Disclaimer: This is a free software. If you use this software and it directly or indirectly causes you loss or damage, I will not be held responsible. By using this software, you are deemed to have accepted this disclaimer.

> This software is packed with VMProtect, and some antivirus software may report it as a virus... Please rest assured that this is a false positive by the antivirus software.

> This software is free, but without the author's written authorization, it is forbidden for commercial use; furthermore, this software is forbidden for malicious purposes (e.g., as part of a virus or Trojan, cracking Internet cafe billing systems, etc.).

> This software is for learning and communication only. If there is any infringement, please delete it within 24 hours.

---

> This driver is packed with VMProtect and does not support enabling kernel isolation.

> The driver is not signed. Please sign the driver file yourself or enable debugging mode. If the driver fails to load even after signing, please disable Secure Boot, or Microsoft EV signature, or use it in a virtual machine.

> If you find any bugs during use, please contact us for feedback, and we will fix them as soon as possible. If you have any good suggestions or opinions, you can also contact the following QQ or QQ group.
> QQ: 3269334485; QQ Group: 399309204

---

## Tool Screenshots

![Process Screenshot](https://github.com/ClownQq/YDArk/blob/master/screenshots/Process.png)
![System Notify Screenshot](https://github.com/ClownQq/YDArk/blob/master/screenshots/SystemNotify.png)

## Features

### Process
- Threads: View/Kill/Suspend/Resume
- Modules: View/Unload/Dump
- Handles: View/Close/Modify Granted Access
- Windows: View/Show/Hide/Maximized/Minimized/Enable/Disable/Close/Attack
- Memories: View/Dump/Modify Protection
- Timers: View/Remove
- HotKeys: View/Remove

### Driver Module
- Driver: View/Unload/Dump/View Hide Driver

### Kernel
- System Notify: View/Remove/Disassembling
- Filter Driver: View/Remove/Disassembling
- DPC Timer: View/Remove/Disassembling
- Hal Call: View/Restore/Disassembling
- Wdf Call: View/Restore/Disassembling
- File System: View/Remove/Disassembling
- Object Hijack: View/Restore (Disk)
- Global Descriptor Table: View

### Kernel Hook
- SSDT: View/Restore/Disassembling
- ShadowSSDT: View/Restore/Disassembling
- FSD: View/Restore/Disassembling
- Keyboard: View/Restore/Disassembling
- I8042prt: View/Restore/Disassembling
- Mouse: View/Restore/Disassembling
- Partmgr: View/Restore/Disassembling
- Disk: View/Restore/Disassembling
- Atapi: View/Restore/Disassembling
- Acpi: View/Restore/Disassembling
- Scsi: View/Restore/Disassembling
- Kernel Hook: Scan/Restore/Disassembling
- Object Type: View/Restore/Disassembling
- Interrupt Descriptor Table: View

### User Hook
- Message Hook: View/Remove
- User Hook: Scan/Restore
- Kernel Hook Table: Scan/Restore

### Network
- Port: View/Remove
- Tcpip: View/Restore/Disassembling
- Nsiproxy: View/Restore/Disassembling
- Tdx: View/Restore/Disassembling
- Wfp WfpFilter: View/Remove
- Wfp Callout: View
- Ndis: View
- IE Plugin: View/Remove
- IE Shell: View/Remove
- SPI: View/Repair
- Hosts: View/Edit

### Registry
- Create/Enumerate/Delete/Rename/Export/View Watch

### File
- Create/Enumerate/Delete/Rename/View Lock/View File Pending/Delay Delete/Copy To/Copy In/Drag In

### Startup Info
- Startup: View/Remove
- Services: View/Start/Stop/Pause/Resume/Restart/Delete
- Schedule Task: View/Disable/Enable/Delete

### Monitor
- Create Exit Process/Create Thread/Load Image/Load Driver/Remote Thread Injection

### About

---

## Version History

### 1.0.0.6
- Added enumeration/restoration of Disk object hijacking

### 1.0.0.7
- Optimized driver module enumeration
- Fixed blue screen crash when setting registry values on 17763-18362 systems
- Fixed disappearing controls after minimizing the interface for a period, now supports maximizing the interface window
- Added enumeration/deletion/repair of startup items
- Fixed process window functionality

### 1.0.0.8
- Fixed blue screen crash caused by restoring SSDT/ShadowSSDT
- Added kernel inline hook restoration

### 1.0.0.9
- Added update detection
- Added display of service modules for svchost.exe processes
- Enumerated/started/stopped/paused/resumed/restarted/deleted services
- Added enumeration/disabling/enabling/deleting scheduled tasks

### 1.0.0.10
- Fixed a bug in enumerating thread modules
- Optimized update detection
- Added enumeration/removal of registry monitoring modification callbacks (right-click TREE control in registry window)

### 1.0.0.11
- Fixed Win7-Win8 system callbacks displaying Thread type as Process type
- Added Ctrl+C to copy a line
- Added monitoring of process/driver loading/remote thread injection (Stack loading symbols is slow, you can rename symsrv.dll to another filename to cancel symbol loading)

### 1.0.0.12
- Added support for Windows 10 18363
- Added monitoring of create/exit threads/module loading
- Fixed several bugs

### 1.0.0.13
- Added support for Traditional Chinese and English

### 1.0.0.14
- Added process creation Dump
- Added Pte Hook scanning

### 1.0.0.15
- Fixed a bug causing abnormal file paths
- Added registry export to .reg file
- Added application layer inline hook scanning

### 1.0.0.16
- Optimized driver module enumeration
- Optimized kernel hook scanning
- Added application layer EAT hook scanning
- Added Infinity hook detection (SSDT Tab pop-up)

### 1.0.0.17
- Added support for 7600
- Added network IE plugins/right-click menu/SPI/Host

### 1.0.0.18
- Added System Miscellaneous Tab
- Fixed kernel hook scan not displaying bug

### 1.0.1.1
- Changed tool icon
- Added application layer IAT hook scanning (X64: Ntdll\\KernelBase\\Kernel32; X32: Ntdll)
- Disassembly engine changed to Zydis (https://github.com/zyantific/zydis)
- Enhanced driver module scanning
- Optimized kernel hook scanning (random page table base address)

### 1.0.1.2
- Fixed incorrect process protection count bug
- Added IRP dispatch routine display (Driver Module Tab - right-click menu)
- Added file directory copy
- Added enumeration of worker threads
- Added Sysenter hook detection (SSDT Tab pop-up)
- Added enumeration of ExCallBack (Kernel Hook Tab - Object Hook Tab)
- Referenced several BMP icons from https://github.com/zodiacon/ProcMonX

### 1.0.1.3
- Fixed individual original functions failing to be obtained for FastFat, ExFat, MsFs
- Added process injection
- Added process hiding

### 1.0.1.4
- Optimized process handle information
- Added file protection

### 1.0.1.5
- Added support for Windows 10 19041
- Added process unlink support for process protection
- Added detection/removal of ATs startup
- Fixed PG blue screen triggered by process unlinking on system versions greater than or equal to 17134; ps: For VMware virtual machines, please remove the vm3dmp.sys process callback, otherwise the process will blue screen upon exit~
- Enhanced acquisition of driver module information

### 1.0.1.6
- Enhanced system thread module acquisition
- Added Windows 10 driver module rename scanning
- Added system speed change (System Miscellaneous Tab - Miscellaneous), currently supports 7600, 7601, 9200, 9600, 10240, 10586, 14393, 15063

### 1.0.1.7
- Changed tool icon (thanks to group members for providing)
- Fixed blue screen during driver module enumeration
- Fixed blue screen for monitoring function

### 1.0.1.8
- Optimized process hook scanning

### 1.0.1.9
- Fixed service enumeration failure bug
- Added system speed change (System Miscellaneous Tab - Miscellaneous), 16299-19041, currently supports all systems

### 1.0.1.10
- Added process command line
- Added modification of process path
- Added modification of process parent process Id
- Added display of specified driver threads (Driver Module Tab - right-click - Driver Threads)
- Added enumeration/removal of VEH VCH UEF (Application Layer Hook Tab - Exception Callbacks)

### 1.0.1.11
- Added support for Windows 10 19042
- Optimized process inline hook restoration
- Optimized process memory attribute modification
- Fixed application layer interface related bugs
- Added title ads (gotta make a living, right?)
- Fixed pop-up 1073 error

### 1.0.2.1
- Fixed 19042 DPC timer enumeration defect (thanks to group members for reminding)
- Fixed driver loading defect

### 1.0.2.2
- Added support for Windows 10 19043
- Enhanced process related operations
- Added remote IP identification for network ports

### 1.0.2.3
- Added SSDT VtHook detection
- Added 19041-19043 Infinity hook detection (SSDT Tab pop-up)
- Removed software update detection

### 1.0.2.4
- Added support for Windows 11 22000
- Enhanced process related operations
- Enhanced file related operations

### 1.0.2.5
- Added support for Windows 10 19044
- Repaired Windows Server 2016 loading BSOD

### 1.0.3.1
- Added support for Windows 10 19045
- Added support for Windows 11 22621
- Disabled process hide
- Optimized file traversal

### 1.0.3.2
- Optimized process enumeration
- Optimized driver enumeration
- Optimized kernel hook scanning
- Fixed Windows 10 SSDT bug
- Fixed process message bug
- Optimized Loading driver error code
- Added modification process timer time (milliseconds)

### 1.0.3.3
- Added support for Windows 11 22631
- Repaired driver module tab BSOD
- Optimized HAL information