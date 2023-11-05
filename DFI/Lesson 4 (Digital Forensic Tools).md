# Objectives  

Explain how to evaluate the needs for digital forensics tools  

List some considerations for digital forensics hardware tools  

Describe methods for validating and testing forensics tools  

<br>

# Navigation  

* [Evaluating Digital Forensics Tool Needs](#evaluating-digital-forensics-tool-needs)  
* [Types of Digital Forensics Tools](#types-of-digital-forensics-tools)  
* [Tasks Performed by Digital Forensics Tools](#tasks-performed-by-digital-forensics-tools)  
* [Considerations for Tools](#considerations-for-tools)  
* [GUI Forensics Tools](#gui-forensics-tools)

<br>

## Evaluating Digital Forensics Tool Needs  

Consider open-source tools; the best value for as many features as possible  

<br>

Questions to ask when evaluating tools  
* On which OS does the forensics tool run  
* What file systems can the tool analyse?  
* Can a scripting language be used with the tool to automate repetitive functions?  
* Does it have automated features?  
* What is the vendor's reputation for providing support?  

<br>

## Types of Digital Forensics Tools  

Hardware forensics tools  
* Range from single-purpose components to complete PC systems and servers  

<br>

Software forensic tools  
* Range from $300 up  
* 2 Types, CLI and GUI apps  
* Commonly used to copy data from a suspect's disk drive to an image file  

<br>

## Tasks Performed by Digital Forensics Tools  

Follow guidelines set up by NIST's PC Forensics Tool Testing (CFTT) program  

ISO standard 27037 states: Digital Evidence First Responders (DEFRs) should use validated tools  

<br>

All PC forensics tools, both hardware and software, perform specific functions. These functions can be grouped into 5 major categories  
* Acquisition  
* Validation and verification  
* Extraction  
* Reconstruction  
* Reporting  

<br>

Acquisition  
* Making a copy of the original drive  
* 2 types of data-copying methods used in software acquisitions, Physical copying of entire drive, and Logical copying of disk partition  
* Formats for disk acquisitions vary from raw data to vendor-specific proprietary  
* Creating smaller <b>segmented files</b> is a typical feature in vendor acquisition tools - segmented files are smaller and therefore can be be stored in smaller media  
* Remote acquisition of files is common in larger organisations, popular tools such as AccessData and EnCase can do remote acquisitions of forensics drive images on a network  

<br>

Acquisition subfunctions  
* Physical data copy  
* Logical data copy - logical partition  
* Data acquisition format - raw data format  
* GUI acquisition  
* Remote, live (login), and memory acquisitions  

<br>

You can view the contents of a raw image file with any hexadecimal editor  

<br>

Validation  
* A way to confirm that a tool is functioning as intended, ensuring the integrity of data being copied  

<br>

Verification  
* <b>Proves that 2 sets of data are identical</b> by calculating hash values or using similar methods  
* A related process is filtering, which involves sorting and searching through investigation findings to separate good data and suspicious data  

<br>

Subfunctions of validation and verification  
* <b>Hashing - ensure that data hasn't been changed</b>, e.g. CRC-32, MD5, SHA-1  
* <b>Filtering - To separate good files and files that need to be investigated</b>, based on hash value sets  
* <b>Analysing file headers - To check on change file type</b>, discriminate files based on their types  
* National Software Reference Library (NSRL) has compiled a list of known file hashes, for a variety of OSes, apps, and images  
* Many PC forensics programs include a list of common header values, with this info, you can see whether a file extension is incorrect for the file type  
* Most forensics tools can identify header values  

<br>

Extraction  
* Recovery task in a digital investigation  
* <b>Most challenging of all tasks to master!!</b>  
* Recovering data is the 1st step in analysing an investigation's data  
* <b>Keyword search</b> speeds up analysis for investigators  
* From an investigation perspective, encrypted files and systems are a problem  
* Many password recovery tools have a feature for generating <b>potential password lists</b> for a <b>password dictionary attack</b>  
* If a password dictionary attack fails, you can run a <b>brute-force attack</b>  

<br>

Subfunctions of extraction  
* Data viewing - different tools provide different ways of viewing data  
* Keyword searching - A good function but if wrong key word is used, it may produce "noise"  
* Decompressing or uncompressing  
* Carving - Reconstructing fragments of files  
* Decrypting - Can be a potential problem for investigation  
* Bookmarking or tagging  

<br>

Reconstruction  
* Re-create a suspect drive to show what happened during a crime or an incident - Another reason is to create a copy of suspect drive for other investigators  
* To re-create an image of a suspect drive, copy an image to another location, such as a partition, a physical disk, or a VM. <b>Simplest method is to use a tool that makes a direct disk-to-image copy</b>  

<br>

Methods of reconstruction  
* Disk-to-disk copy  
* Partition-to-partition copy  
* Image-to-disk copy  
* Image-to-partition copy  
* Rebuilding files from data runs and carving  

<br>

Examples of disk-to-image copy tools  
* Linux dd command  
* ProDiscover  
* Voom Technologies Shadow Drive  

<br>

Reporting  
* To perform a forensics disk analysis and examination, you need to create a report  

<br>

Subfunctions of reporting  
* Bookmarks or tagging  
* Log reports - document investigation steps  
* Report generator  

<br>

Use this info when producing a final report for an investigation  

<br>

## Considerations for Tools  

Considerations  
* Flexibility  
* Reliability  
* Future expandability  

<br>

Create a software library containing older versions of forensics utilities, OSes, and other programs  

<br>

## GUI Forensics Tools  

GUI forensics tools can simplify digital forensics investigations  

Have also simplified training for beginner examiners  

Most of them are put together as suites of tools  

<br>

Advantages  
* Ease of use  
* Multitasking  
* No need for learning older OSes  

<br>

Disadvantages  
* Excessive resource requirements - i.e. PC RAM  
* Produce inconsistent results - Because of the type of OS used. 32 bits OS vs 64 bits OS  
* Create tool dependencies, investigators may want to use only 1 tool - Refuse to change. Should be familiar with more than 1 type of tool  

<br>

## Digital Forensics <b>Hardware Tools</b>  

Technology changes rapidly  

Hardware eventually fails  

Schedule equipment replacements periodically  

<br>

When planning your budget consider  
* Amount of time you expect the forensic workstation to be running  
* Failures - <b>how often does it fail?</b>  
* Consultant and vendor fees - <b>support the h/w</b>  
* Anticipate equipment replacement - the more you use the more the equipment will breakdown  

<br>

## Forensic Workstations  

Carefully consider what you need  

<br>

Categories  
* Stationary workstation  
* Portable workstation  
* Lightweight workstation  

<br>

Balance what you need and what your system can handle  
* Remember that RAM and storage need updating as technology advances  

<br>

Police agency labs  
* Need many options  
* Use several PC configurations  - due to diverse investigations  

<br>

Keep a hardware library in addition to your software library  

<br>

Private corporation labs  
* Handle only system types used in the organisation  

<br>

Building a forensic workstation is not as difficult as it sounds  

<br>

Custom forensic workstation advantages  
* Customized to your needs  
* Save money  

<br>

Custom forensic workstation disadvantages  
* <b>Hard to find support for problems</b>  
* Can become expensive if careless  

<br>

Also need to identify what you intend to analyse  

<br>

## Recommendations for a Forensic Workstation  

Some vendors offer workstations designed for digital forensics  

Having vendor support can save you time and frustration when you have problems  

Can mix and match components to get the capabilities you need for your forensic workstation  

Determine where data acquisitions will take place. i.e. acquire data in the field, may want to carry something light  

<br>

Recommendations when choosing a stationary or lightweight workstation  
* Full tower to allow for expansion devices  
* As much memory and processor power as budget allows  
* Different sizes of hard drives  
* 400-watt or better power supply with battery backup  
* External FireWire and USB 2.0 ports  
* Assortment of drive adapter bridges  
* <b>Ergonomic keyboard</b> and mouse  
* A good video card with at least a 17-inch monitor  
* High-end video card and dual monitors  

<br>

If you have a limited budget, 1 option for outfitting your lab is to use high-end game PCs - can perform well with modifications  

<br>

## Using a Write-Blocker  

Write-blocker prevents data writes to a hard disk  
* A write blocker is any tool that permits read-only access to data storage devices without compromising the integrity of the data  

<br>

Software-enabled blockers  
* Typically run in a shell mode (Windows CLI)  
* Example: PDBlock from Digital Intelligence  

<br>

Hardware options  
* Ideal for GUI forensic tools as they prevent Windows or Linux from writing data to the blocked device  
* Act as a bridge between the suspect drive and the forensic workstation  

<br>

You can navigate to the blocked drive with any app - no problem accessing the blocked drive's apps after write-blocker is installed  

Discards the written data, for the OS the data copy is successful  

<br>

Connecting technologies  
* FireWire  
* USB 2.0 and 3.0  
* SATA, PATA, and SCSI controllers  

<br>

## Validating and Testing Forensic Software  

It is important to make sure the <b>evidence</b> you recover and analyse <b>can be admitted in court</b>  

You must <b>test and validate</b> your software to prevent damaging the evidence  

<br>

## Using National Institute of Standards and Technology Tools  

NIST publishes articles, provides tools, and creates procedures for testing/validating forensics software  

Computer Forensics Tool Testing (CFTT) project manages research on PC forensics tools  

<br>

NIST has created criteria for testing PC forensics tools based on  
* Standard testing methods  
* ISO 17025 criteria for testing items that have no current standards  

<br>

Your lab must meet the following criteria for tool testing  
* Establish categories for digital forensics tools  
* Identify forensics category requirements  
* Develop test assertions based on the requirements, create tests to test tool's capability  
* Identify test cases  
* Establish a test method  
* Report test results  

<br>

<b>ISO 5725</b> - specifies results must be repeatable and reproducible  

<br>

NIST created the National Software Reference Library (NSRL) project  
* Collects all known hash values for commercial software apps and OS files  
* Uses SHA-1 to generate a known set of digital signatures called the Reference Data Set (RDS)  
* Helps filtering known info that could help speed up investigation time  
* Can use RDS to locate and identify known bad files  

<br>

## Using Validation Protocols  

Always verify your results by performing the same tasks with other similar forensics tools  

<br>

<b>Use at least 2 tools</b>  
* Retrieving and examination  
* Verification  

<br>

Understand how forensics tools work  

<br>

1 way to compare results and verify a new tool is by using a <b>disk editor</b>, such as Hex Workshop or WinHex  
* <b>Disk editor</b> can be used to view data on a disk in its raw format  

<br>

<b>Disk editors</b> do not have a flashy interface, however they  
* Are reliable tools  
* Can access raw data  

<br>

Computer Forensics Examination Protocol  
* Perform the investigation with a GUI tool  
* Verify your results with a disk editor  
* Compare hash values obtained with both tools  

<br>

<b>Digital Forensics Tool Upgrade Protocol</b> - To ensure evidence data will not be corrupted  
* Test new releases for tools, and test OS patches and upgrades  
* If a problem is found, report it to the forensics tool vendor and do not use the forensics tool until the problem has been fixed  
* Use a test hard disk for validation purposes  
* Check the Web for new editions, updates, patches, and validation tests for your tools  

<br>

## Summary  

Consult business plan to get the best hardware and software  

<br>

PC forensics tools and their functions  
* Acquisition  
* Validation and verification  
* Extraction  
* Reconstruction  
* Reporting  

<br>

Maintain a software library on your lab  

<br>

PC Forensics tools types  
* Software  
* Hardware  

<br>

Forensics software, GUI

<br>

Forensics hardware  
* Customized equipment - Make 1 yourself  
* Commercial options - Buy off the shelf  
* Include workstations and write-blockers  

<br>

Always run a validation test when upgrading your forensics tools  