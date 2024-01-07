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

