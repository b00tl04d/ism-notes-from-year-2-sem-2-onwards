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

