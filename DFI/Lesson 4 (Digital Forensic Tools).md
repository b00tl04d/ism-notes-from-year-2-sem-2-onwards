# Objectives  

Explain how to evaluate the needs for digital forensics tools  

List some considerations for digital forensics hardware tools  

Describe methods for validating and testing forensics tools  

<br>

# Navigation  

* [Evaluating Digital Forensics Tool Needs](#evaluating-digital-forensics-tool-needs)  
* [Types of Digital Forensics Tools](#types-of-digital-forensics-tools)  

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