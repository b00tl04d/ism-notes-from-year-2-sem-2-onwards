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

