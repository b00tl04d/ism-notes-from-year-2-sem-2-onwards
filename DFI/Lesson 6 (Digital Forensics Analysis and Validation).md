# Objectives  

• Determine what data to analyse in a digital forensics investigation  

• Explain tools used to validate data  

• Explain common data-hiding techniques  

<br>

# Navigation


<br>

## Determining What Data to Collect and Analyse  

• Examining and analyzing digital evidence depend on the nature of the investigation And  
– the amount of data to process  
– Corporate investigators often locating and recovering a few specific items, such as emails, which simplifies and speeds processing  

• Scope creep - when an investigation expands beyond the original description  
– Because of unexpected evidence found  
– Attorneys may ask investigators to examine other areas to recover more evidence  
– Increases the time and resources needed to extract, analyze, and present evidence  
– Need to document additional time spend on recovering additional evidences!!  

• Scope creep has become more common  
– Criminal investigations require more detailed examination of evidence just before trial  
– To help prosecutors fend off attacks from defense attorneys  

• New evidence discovered often isn’t revealed to prosecution  
– It’s become more important for prosecution teams to ensure they have analyzed the evidence exhaustively before trial  

<br>

## Approaching Digital Forensics Cases  

• Begin a case by creating an investigation plan that defines the:  
– Goal and scope of investigation  
– Materials needed  
– Tasks to perform  

• The approach you take depends largely on the type of case you’re investigating  
– Corporate, civil, or criminal  
• Corporate case tends to be easier due to easy access to evidence  
• Criminal case is more difficult because of scope. i.e need to contact ISP to gather evidence  

• Follow these basic steps for all digital forensics investigations:  
– 1. For target drives, use recently wiped media that have been reformatted and inspected for viruses  
– 2. Inventory the hardware on the suspect’s computer, and note condition of seized computer  
– 3. For static acquisitions, remove original drive and check the date and time values in system’s CMOS  
– 4. Record how you acquired data from the suspect drive  
– 5. Process drive’s contents methodically and logically. i.e emails &rarr; JPG &rarr; spreadsheet &rarr; word  
– 6. List all folders and files on the image or drive. Note where a file/picture is found  
– 7. Examine contents of all data files in all folders. Starting from root directory  
– 8. Recover file contents for all password-protected files. Use password recovery tools  
– 9. Identify function of every executable file (exe) that doesn’t match known hash values. If required run file to find out more  
– 10. Maintain control of all evidence and findings  

• Refining and Modifying the Investigation Plan  
– Even if initial plan is sound, at times you may need to deviate from it and follow evidence  
– Knowing the types of data to look for helps you make the best use of your time  
– The key is to start with a plan but remain flexible in the face of new evidence  

<br>

## Using OSForensics to Analyse Data  

• OSForensics can perform forensics analysis on the following file systems:  
– Microsoft FAT12, FAT16, and FAT32  
– Microsoft NTFS – Mac HFS+ and HFSX  
– Linux Ext2fs, and Ext4fs  

• OSForensics can analyze data from several sources  
– Including image files from other vendors  

<br>

## Validating Forensic Data  

• Ensuring the integrity of data collected is essential for presenting evidence in court  

• Most forensic tools offer hashing of image files  
– Example - when ProDiscover loads an image file:  
• It runs a hash and compares the value with the original hash calculated when the image was first acquired  

<br>

## Validating with Hexadecimal Editors  

• Some digital forensics tools may have some limitations in performing hashing, so using advanced hexadecimal editors is necessary to ensure data integrity.  

• Advanced hex editors offer features not available in digital forensics tools, such as:  
– Hashing specific files or sectors  

• With the hash value in hand  
– You can use a forensics tool to search for a suspicious file that might have had its name changed to look like an innocuous file  

• WinHex provides MD5 and SHA-1 hashing algorithms  

• Using Hash Values to Discriminate Data  
– AccessData has its own hashing database, is known as Known File Filter (KFF)  
– KFF filters known program files from view and contains hash values of known illegal files  
– It compares known file hash values with files on your evidence drive to see if they contain suspicious data  
– Other digital forensics tools can import the NSRL database and run hash comparisons  

<br>

## Validating with Digital Forensics Tools  

• ProDiscover  
– .eve files contain metadata that includes hash value  
– Has a preference you can enable for using the Auto Verify Image Checksum feature when image files are loaded  
– If the Auto Verify Image Checksum and the hashes in the .eve file’s metadata don’t match  
• ProDiscover will notify that the acquisition is corrupt and can’t be considered reliable evidence  

• Raw format image files don’t contain metadata  
– You must validate them manually to ensure integrity  

• In AccessData FTK Imager, when selecting the Expert Witness (.e01) or SMART (.s01) format:  
– Additional options for validating the acquisition are available  
– Validation report lists MD5 and SHA-1 hash values  

<br>

## Addressing Data-Hiding Techniques  

• Data hiding - changing or manipulating a file to conceal information  

• Techniques:  
– Hiding entire partitions  
• Use Disk Management  
– Changing file extensions  
– Setting file attributes to hidden  
• Change file signature  
– Bit-shifting  
• Shift 1 bit to left  
– Using encryption  
– Setting up password protection  

<br>

## Hiding Files by Using the OS  

• One of the first techniques to hide data:  
– Changing file extensions  

• Advanced digital forensics tools check file headers  
– Compare the file extension to verify that it’s correct  
– If there’s a discrepancy, the tool flags the file as a possible altered file  

• Another hiding technique  
– Selecting the Hidden attribute in a file’s Properties dialog box (windows)  

<br>

## Hiding Partitions  

• By using the Windows diskpart remove letter command  
– You can unassign the partition’s letter, which hides it from view in File Explorer  

• To unhide, use the diskpart assign letter command  

• Other disk management tools:  
– Partition Magic, Partition Master, and Linux Grand Unified Bootloader (GRUB)  

• To detect whether a partition has been hidden  
– Account for all disk space when examining an evidence drive  
– Analyze any disk areas containing space you can’t account for  

• In ProDiscover, a hidden partition appears as the highest available drive letter set in the BIOS  
– Other forensics tools have their own methods of assigning drive letters to hidden partitions  

<br>

