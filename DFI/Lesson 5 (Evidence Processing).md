# Objectives  

Explain the purpose and structure of file systems  

Describe Microsoft file structures  

Explain the structure of NTFS disks  

List some options for decrypting drives encrypted with whole disk encryption  

Explain how the Windows Registry works  

Describe Microsoft startup tasks  

Explain the purpose of a virtual machine  

<br>  

# Navigation  

* [Understanding File Systems](#understanding-file-systems)  
* [Understanding the Boot Sequence](#understanding-the-boot-sequence)  
* [Understanding Disk Drives](#understanding-disk-drives)  

<br>

## Understanding File Systems  

File system  
* Gives OS a road map to data on a disk  

<br>

Type of file system an OS uses determines how data is stored on the disk  

When you need to access a suspect's PC to acquire or inspect data (You should be familiar with both the PC OS and its file system)  

<br>

## Understanding the Boot Sequence  

Complementary Metal Oxide Semiconductor (CMOS)  
* PC stores system config, date and time info in the CMOS  

<br>

Basic Input/Output System (BIOS) or Extensible Firmware Interface (EFI)  
* Contains programs that perform input and output at the hardware level  

<br>

Bootstrap process  
* Contained in ROM, tells the PC how to proceed  
* Displays the key or keys to press to open the CMOS setup screen (Besides date and time, BIOS settings are stored in CMOS)  

<br>

CMOS should be modified to boot from a forensic floppy disk or CD to prevent evidence from hard disk being overwritten  

<br>

BIOS can configure:  
* System Time/Date  
* Boot Sequence  
* Plug and Play  
* Mouse/Keyboard  
* Drive Configuration  
* Security  
* Power Management  
* ..etc  

<br>

## Understanding Disk Drives  

Disk drives are made up of 1 or more platters coated with magnetic material  

<br>

Disk drive components:  
* Geometry (how data is structured)  
* Head  
* Tracks  
* Cylinders  
* Sectors (1 sector usually has 512 bytes)  

<br>  

Properties handled at the drive's hardware or firmware level include:  
* Zone bit recording (ZBR), grouping tracks by zones ensures that all tracks hold the same amount of data  
* Track density, space between each track, the smaller the space, the more track on the platter  
* Areal density, number of bits in 1 square inch of a disk platter  
* Head and cylinder skew, improves disk performance by minimizing the movement of read/write head  

<br>

## Solid-State Storage Devices  

All flash memory devices have a feature called wear-leveling  
* An internal firmware feature used in solid-state drives that ensures even wear of read/writes for all memory cells, in general, memory cells can perform 10k - 100k reads/writes  

<br>

When dealing with solid-state devices, making a full forensic copy as soon as possible is crucial  
* In case you need to recover data from unallocated disk space, wear-leveling feature auto overwrites the unallocated space  

<br>

## Exploring Microsoft File Structures  

• In Microsoft file structures, sectors are grouped to form clusters
– Storage allocation units of one or more sectors  

• Clusters can have one sector or more  

• Combining sectors minimizes the overhead of writing or reading files to a
disk  

• Clusters are numbered sequentially starting at 0 in NTFS and 2 in FAT  
– First sector of all disks contains a system area, the boot record, and a file
structure database  

• OS assigns these cluster numbers, called logical addresses  
– Address point to relative position  

• Sector numbers are called physical addresses  
– From address 0 to last sector on disk  

• Clusters and their addresses are specific to a logical disk drive, which is a disk partition  

<br>

## Disk Partitions  

• A partition is a logical drive. i.e “C”, “D”, “E” and etc  

• Windows OSs can have three primary partitions followed by an extended partition that can contain one or more logical drives  

• Partition gap  
– Unused space between partitions  
– Can use to hide data!  

A partition table is a table maintained on disk by the operating system
describing the partitions on that disk.  

key hexadecimal codes is used by OS to identify and maintain the file system.  

• The partition table is in the Master Boot Record (MBR)  
– Located at sector 0 of the disk drive, preceding the first partition.  

• MBR stores information about partitions on a disk and their locations, size, and other important items  

• In a hexadecimal editor, such as WinHex, you can find the first partition at offset 0x1BE  
– File system’s hexadecimal code is offset 3 bytes from 0x1BE for the first partition  
– Sector address of where this partition starts on the drive is offset 8 bytes from 0x1BE.  
– The number of sectors assigned to the partition are offset 12 bytes from position 0x1BE.  

<br>

## Examining FAT Disks  

• File Allocation Table (FAT)  
– File structure database that Microsoft originally designed for
floppy disks  

• FAT database is typically written to a disk’s outermost track and contains:  
– Filenames, directory names, date and time stamps, the starting cluster number, and file attributes  

• Four current FAT versions  
– FAT12, FAT16, FAT32, and exFAT (used by Xbox game systems)  

• Cluster sizes vary according to disk drive size and file system  

• Microsoft OSs allocate disk space for files by clusters  
– Results in drive slack  

• Unused space in a cluster between the end of an active file and the end of the cluster  

• Drive slack includes:  
– RAM slack (portion of the last sector used in the last assigned cluster) and 
– File slack (unused space allocated for a file)  

• An unintentional side effect of FAT16 having large clusters was that it reduced fragmentation  
– As cluster size increased  

![image](../images/ram_slack_file_slack.png)  

• When you run out of room for an allocated cluster  
– OS allocates another cluster for your file, which creates more slack space on the disk  

• As files grow and require more disk space, assigned clusters are chained together  
– The chain can be broken or fragmented due to deleted files or expansion files  

• When the OS stores data in a FAT file system, it assigns a starting cluster position to a file  
– Data for the file is written to the first sector of the first assigned cluster  
– When this first assigned cluster is filled and runs out of room, FAT assigns the next available cluster to the file  

<br>

## Deleting FAT Files  

• In Microsoft OSs, when a file is deleted  
– Directory entry is marked as a deleted file  

• With the hex E5 character replacing the first letter of the filename  

• FAT chain for that file is set to 0  

• Data in the file remains on the disk drive  

• Area of the disk where the deleted file resides becomes unallocated disk space  
– Available to receive new data from newly created files or other files needing more space  
<br>

## Examining NTFS Disks  

• NT File System (NTFS)  
– Introduced with Windows NT  
– Primary file system for Windows 8 or later  

• Improvements over FAT file systems  
– NTFS provides more information about a file  
– NTFS gives more control over files and folders  

• NTFS was Microsoft’s move toward a journaling file system  
– It records a transaction before the system carries it out. i.e deleting a file  

• In NTFS, everything written to the disk is considered a file  

• On an NTFS disk  
– First data set is the Partition Boot Sector  
– Next is Master File Table (MFT)  

• NTFS results in much less file slack space  

• Clusters are smaller for smaller disk drives  

• NTFS also uses Unicode – An international data format  

Note : sector size = 512 bytes (For DFI material)  

<br>

## NTFS System Files  

• Master File Table (MFT) contains information about all files on the disk  
– Including the system files OS uses  

• In the MFT, the first 15 records are reserved for system files  

• Records in the MFT are called metadata  

<br>

## MFT and File Attributes  

• In the NTFS MFT  
– All files and folders are stored in separate records of 1024 bytes each  

• Each record contains file or folder information  
– This information is divided into record fields containing metadata  

• A record field is referred to as an attribute ID  

• File or folder information is typically stored in one of two ways in an MFT record:  
– Resident and nonresident  

• Each MFT record starts with a header identifying it as a resident or nonresident attribute  

• Files larger than 512 bytes (nonresident) are stored outside the MFT  
– MFT record provides cluster addresses where the file is stored on the drive’s partition  

• Referred to as data runs  

• For very small files, about 512 bytes or less (resident), all file metadata and data are stored in the MFT record.  

Basic information of a file in MFT starts at 0x10  

• When a disk is created as an NTFS file structure  
– OS assigns logical clusters to the entire disk partition  

• These assigned clusters are called logical cluster numbers (LCNs)  
– Become the addresses that allow the MFT to link to nonresident files on the disk’s partition  

• When data is first written to nonresident files, an LCN address is assigned to the file  
– This LCN becomes the file’s virtual cluster number (VCN)  

<br>

## MFT Structures for File Data  

• For the header of all MFT records, the record fields of interest are as follows:  
– At offset 0x00 - the MFT record identifier FILE  
– At offset 0x14 - length of the header (indicates where the next attribute starts) 38 00 &rarr; 00 38 = 56 bytes!!  
– At offset 0x1C to 0x1F - size of the MFT record  
– At offset 0x32 and 0x33 - the update sequence array, which stores the last 2 bytes of the first sector of the MFT record  

• The update sequence array is used as a checksum for record integrity validation  

Standard Information attribute –  
• Create date and time  
• Last modified date and time  
• Last access date and time  
• Record update date and time  

<br>

## NTFS Alternate Data Streams  

• Alternate data streams  
– Ways data can be appended to existing files  
– Can obscure valuable evidentiary data, intentionally or by coincidence  

• In NTFS, an alternate data stream becomes an additional file attribute  
– Allows the file to be associated with different applications  

• You can only tell whether a file has a data stream attached by examining that file’s MFT entry  

<br>

## NTFS Compressed Files  

• NTFS provides compression similar to FAT  

• Under NTFS, files, folders, or entire volumes can be compressed  

• Most computer forensics tools can uncompress and analyze compressed Windows data  

<br>

## NTFS Encrypting File System (EFS)  

• Encrypting File System (EFS)  
– Introduced with Windows 2000  
– Implements a public key and private key method of encrypting files, folders, or disk volumes  

• When EFS is used in Windows 2000 and later  
– A recovery certificate is generated and sent to the local Windows administrator account  

• Recovery certificate is required if there is a problem  

• Users can apply EFS to files stored on their local workstations or a remote server  

<br>

## EFS Recovery Key Agent  

• Recovery Key Agent implements the recovery certificate  
– Which is in the Windows administrator account  

• Windows administrators can recover a key in two ways: through Windows or from an MS-DOS command prompt  

• MS-DOS commands  
– Cipher (for NTSF only)  
– copy  
– efsrecvr (used to decrypt EFS files. For NTSF only)  
– Use /? to find out more  

<br>

## Deleting NTFS Files  

• When a file is deleted in Windows NT and later  
– The OS renames it and moves it to the Recycle Bin  

• Can use the Del (delete) MS-DOS command to delete file too  
– This method does not rename and move deleted file to recycle bin but eliminates the file from the MFT listing in the same way FAT does  

<br>

## Understanding Whole Disk Encryption (WDE)  

• In recent years, there has been more concern about loss of  
– Personal identity information (PII) and trade secrets caused by computer theft  

• Of particular concern is the theft of laptop computers and other handheld devices  

• To help prevent loss of information, software vendors now provide whole disk encryption  

• Current whole disk encryption tools offer the following features:  
– Preboot authentication  
• single sign-on password, fingerprint scan  
– Full or partial disk encryption with secure hibernation  
• Password protected screen saver  
– Advanced encryption algorithms  
• i.e AES or IDEA  
– Key management function  
• Passphrase to reset password  

• Whole disk encryption tools encrypt each sector of a drive separately  

• Many of these tools encrypt the drive’s boot sector  
– To prevent any efforts to bypass the secured drive’s partition  

• To examine an encrypted drive, decrypt it first!!  
– Run a vendor-specific program to decrypt the drive  
– Many vendors use a bootable CD or USB drive that prompts for a one-time passphrase  

• Note : Without the necessary credentials to unlock an encrypted drive, it is not possible to view any logical level information.  

<br>

## Examining Microsoft BitLocker (Example)  

• Available Vista Enterprise/Ultimate, Windows 7 and 8 Professional/Enterprise, and Server 2008, 2012 and 2016.  

• Hardware and software requirements  
– A computer capable of running Windows Vista or later  
– The Trusted Platform Module(TPM) microchip, version 1.2 or newer  
• stores RSA encryption keys specific to the host system for hardware authentication.  
– A computer BIOS compliant with Trusted Computing Group (TCG)  
– Two NTFS partitions  
– The BIOS configured so that the hard drive boots first before checking other bootable peripherals  

<br>

## Understanding Windows Registry  

• Registry  
– A database that stores hardware and software configuration information, network connections, user preferences, and setup information  

• To view the Registry, you can use:  
– Regedit (Registry Editor) program for Windows 9x systems  
– Regedt32 for Windows 2000, XP, and Vista  
– Both utilities can be used for Windows 7 and later.  

<br>

## Exploring the Organization of the Windows Registry  

• Registry terminology:  
– Registry  
– Registry Editor  
– HKEY  
– Key  
– Subkey  
– Branch  
– Value  
– Default value  
– Hives  

![image](../images/win_reg_file_locations_and_purposes.png)  

![image](../images/hkeys_and_funcs.png)  

<br>

## Understanding Microsoft Startup Tasks  

• Learn what files are accessed when Windows starts  

• This information helps you determine when a suspect’s computer was last accessed  
– Important with computers that might have been used after an incident was reported  

<br>

## Startup in Windows 7 and Windows 8  

• Windows 7/8 is a multiplatform OS  
– Can run on desktops, laptops, tablets, and smartphones  

• The boot process uses a boot configuration data (BCD) store  

• The BCD contains the boot loader that initiates the system’s bootstrap process  
– Press F8 or F12 when the system starts to access the Advanced Boot Options, ie. Start in Safe Mode  

<br>

## Startup in Windows NT and Later  

• All NTFS computers perform the following steps when the computer is turned on:  
– Power-on self test (POST)  
– Initial startup  
– Boot loader  
– Hardware detection and configuration  
– Kernel loading  
– User logon  

• Startup Files for Windows Vista:  
– The Ntldr (NT Loader) program in Windows XP used to load the OS has been replaced with these three boot utilities:  
• Bootmgr.exe  
• Winload.exe  
• Winresume.exe  
– Windows Vista includes the BCD editor for modifying boot options and updating the BCD registry file  
– The BCD store (Namespace container for BCD Objects) replaces the Windows XP boot.ini file  
• Old Windows uses boot.ini to configure boot sequences  

• Startup Files for Windows XP: 
– NT Loader (NTLDR)  
– Boot.ini  
– Ntoskrnl.exe  
– Bootvid.dll  
– Hal.dll  
– BootSect.dos  
– NTDetect.com  
– NTBootdd.sys  
– Pagefile.sys  

Why need to know the start up process?  

• Contamination Concerns with Windows XP  
– When you start a Windows XP NTFS workstation, several files are accessed immediately  
• The last access date and time stamp for the files change to the current date and time  
• Destroys any potential evidence that shows when a Windows XP workstation was last used  

<br>

## Understanding Virtual Machines  

• Virtual machine  
– Allows you to create a representation of another computer on an existing physical computer  

• A virtual machine is just a few files on your hard drive  
– Must allocate space to it  

• A virtual machine recognizes components of the physical machine it’s loaded on  
– Virtual OS is limited by the physical machine’s OS as behaviour of virtual OS could be affected by physical machine’s OS (i.e certain operations may be blocked)  

