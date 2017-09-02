# Solving Windows and Linux Boot Issues
<p><strong><u>Order of call during Computer Booting</u></strong></p>
<ol>
	<li>BIOS (Basic Input Output System) of the Computer</li>
	<li>MBR (Master Boot Record) for the Boot Disk Selected</li>
	<li>VBR (Volume Boot Record) for the Boot Volume Selected within the Boot Disk</li>
	<li>Second Stage Boot Loader</li>
</ol>
<p>A boot sector or boot block is a region of a hard disk, floppy disk, optical disc, or other data storage device that contains machine code to be loaded into random-access memory (RAM) by a computer system's built-in firmware. The purpose of a boot sector is to allow the boot process of a computer to load a program (usually, but not necessarily, an operating system) stored on the same storage device. The location and size of the boot sector is specified by the design of the computing platform.</p>
<p>On an IBM PC compatible machine, the BIOS selects a boot device, then copies the first sector from the device (which may be a MBR, VBR or any executable code), into physical memory at memory address 0x7C00. On other systems, the process may be quite different.</p>
<p>Several major kinds of boot sectors could be encountered on the IBM PC compatible hard disks, floppy disks and similar storage devices:</p>
<ul>
	<li>A Master Boot Record (MBR) is the first sector of a data storage device that has been partitioned. The MBR sector may contain code to locate the active partition and invoke its Volume Boot Record.</li>
	<li>A Volume Boot Record (VBR) is the first sector of a data storage device that has not been partitioned, or the first sector of an individual partition on a data storage device that has been partitioned. It may contain code to load an operating system (or other standalone program) installed on that device or within that partition.</li>
</ul>
<p>On IBM PC compatible machines, the BIOS is ignorant of the distinction between VBRs and MBRs, and of partitioning. The firmware simply loads and runs the first sector of the storage device. If the device is a floppy or USB flash drive, that will be a VBR. If the device is a hard disk, that will be an MBR. It is the code in the MBR which generally understands disk partitioning, and in turn, is responsible for loading and running the VBR of whichever primary partition is set to boot (the active partition). The VBR then loads a second-stage bootloader from another location on the disk.</p>
<p>Furthermore, whatever is stored in the first sector of a floppy diskette, USB device, hard disk or any other bootable storage device, is not required to immediately load any bootstrap code for an OS, if ever. The BIOS merely passes control to whatever exists there, as long as the sector meets the very simple qualification of having the boot record signature of 0x55, 0xAA in its last two bytes. This is why it's easy to replace the usual bootstrap code found in an MBR with more complex loaders, even large multi-functional boot managers (programs stored elsewhere on the device which can run without an operating system), allowing users a number of choices in what occurs next.</p>
<p>&nbsp;</p>
<p><strong><u>Boot Configuration Data (BCD) Store (Windows Specific)</u></strong></p>
<p>The Boot Configuration Data (BCD) store contains boot configuration parameters and controls how the operating system is started in latest Microsoft® operating systems. These parameters were previously in the Boot.ini file (in BIOS-based operating systems) or in the nonvolatile RAM (NVRAM) entries (in Extensible Firmware Interface–based operating systems).</p>
<p>BCD was created to provide an improved mechanism for describing boot configuration data. With the development of new firmware models (for example, the Extensible Firmware Interface (EFI)), an extensible and interoperable interface was required to abstract the underlying firmware. This new design provides the foundation for a variety of new features in Windows Vista (for example, the Startup Repair tool and Multi-User Install shortcuts).</p>
<p>The BCD file is located in the registry as shown below:</p>
<ul>
	<li>BIOS-based operating systems: The BCD registry file is located in the \Boot\Bcd directory of the active partition.</li>
	<li>EFI (Extensible Firmware Interface) –based operating systems: The BCD registry file is located on the EFI system partition.</li>
</ul>
<p>&nbsp;</p>
<p><strong><u>Using the Windows Recovery CD/DVD to resolve Windows Boot Issues</u></strong></p>
<p>Always keep a Windows Recovery CD/DVD/Bootable USB Drive for troubleshooting issues.  Run the disk and invoke the automated tool for “Startup Repair”.  Please refer <a href="http://windows.microsoft.com/en-sg/windows/what-are-system-recovery-options#what-are-system-recovery-options=windows-7" target="_blank" rel="noopener">here</a> for more information.</p>
<p>Alternatively, use the Bootrec.exe tool which can be invoked through a Command Prompt which can be launched through the Windows Recovery Disk.  Please see this <a href="https://support.microsoft.com/en-us/kb/927392" target="_blank" rel="noopener">site</a> for more information.</p>
<p>You may refer to this <a href="http://technology-risk-management.com/blog/bootable-thumb-drives/" target="_blank" rel="noopener">link </a>to understand how to create a bootable Windows Recovery USB Thumb Drive.</p>
<p><span style="text-decoration: underline;"><strong>Using a Linux Live CD/DVD/Thumb Drive to resolve Linux Boot Issues</strong></span></p>
<p>Always keep a Linux LIve CD/DVD/Bootable USB Drive for troubleshooting issues.  You may refer to this <a href="http://technology-risk-management.com/blog/bootable-thumb-drives/" target="_blank" rel="noopener">link </a>to understand how to create a bootable Linux Live USB Thumb Drive. </p>
<p>Boot into the Live Linux OS.  Follow the instructions mentioned at this <a href="http://howtoubuntu.org/how-to-repair-restore-reinstall-grub-2-with-a-ubuntu-live-cd" target="_blank" rel="noopener">link</a>.  This helps to reinstall/correct the GRUB bootloader settings in the disk containing your active Linux installation.  GRUB even allows to list all the bootable OSes (including Windows) you have installed in the disks it can find in your computer and makes it possible to select booting into those OSes during startup.</p>
<p><u>References</u></p>
<p><a href="https://en.wikipedia.org/wiki/Boot_sector" target="_blank" rel="noopener">https://en.wikipedia.org/wiki/Boot_sector</a></p>
<p><a href="https://technet.microsoft.com/en-us/library/cc976796.aspx" target="_blank" rel="noopener">https://technet.microsoft.com/en-us/library/cc976796.aspx</a></p>
<p><a href="https://technet.microsoft.com/en-us/library/cc721886(v=ws.10).aspx" target="_blank" rel="noopener">https://technet.microsoft.com/en-us/library/cc721886(v=ws.10).aspx</a></p>
