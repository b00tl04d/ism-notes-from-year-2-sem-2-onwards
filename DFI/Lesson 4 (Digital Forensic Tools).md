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

