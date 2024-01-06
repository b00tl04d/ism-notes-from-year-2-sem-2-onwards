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

• Clusters and their addresses are specific to a logical disk drive, which is a
disk partition  

<br>

## Disk Partitions  

• A partition is a logical drive. i.e “C”, “D”, “E” and etc  

• Windows OSs can have three primary partitions followed by
an extended partition that can contain one or more logical
drives  

• Partition gap  
– Unused space between partitions  
– Can use to hide data!  

A partition table is a table maintained on disk by the operating system
describing the partitions on that disk.  

key hexadecimal codes is used by OS to identify and maintain the file system.  

