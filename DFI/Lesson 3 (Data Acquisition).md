# Objectives  

List digital evidence storage formats  

Explain ways to determine the best acquisition method  

Describe contingency planning for data acquisitions  

Explain how to use acquisition tools  

Explain how to validate data acquisitions  

Explain how to use remote network acquisition tools  

List other forensic tools available for data acquisitions  

<br>

# Navigation  
* [Data Acquisition Recap...](#data-acquisition-recap)  

<br>

## Data Acquisition recap...  

Forensic Data Acquisition  
* Before we can analyse data, we have to secure it  
* The goal of forensic data acquisition is <b>to create a forensic copy of a piece of media that is suitable for use as evidence in a court of law</b>  

<br>

## Understanding <b>Storage Formats</b> for Digital Evidence  

Data in a forensics acquisition tool is stored as an <b>image file</b>  

<br>

Basically, the image file can be in 1 of 3 formats  
1. Raw format  
2. Proprietary formats  
3. Advanced Forensics Format (AFF) - Newer  

<br>

## Raw Format  

Makes it possible to write bit-stream data to files (Sequence flat file)  
* In the past we only do bit by bit copy to media same size or bigger to create evidence  

<br>

Advantages  
* Fast data transfers  
* Ignores minor data read errors on source drive  
* Most computer forensics tools can read raw format  

<br>

Disadvantages  
* Requires as much storage as original disk or data  
* Tools might not collect marginal (bad) sectors - due to low threshold of retry reads on weak media spots on a drive  

<br>

## Proprietary Formats  

Most forensics tools have their own formats  

<br>

Features offered  
* Option to compress or not compress image files - save space  
* Can split an image into smaller segmented files - provide integrity check for split data  
* Can integrate metadata into the image file  

<br>

Disadvantages  
* Inability to share an image between different tools/vendors  
* File size limitation for each segmented volume - typically 650MB, can adjust up or down at a limit of 2GB  

<br>

The Expert Witness format is unofficial standard - default for Guidance Software EnCase (i.e. ex01, e01)  

<br>

## Advanced Forensics Format (AFF)  

Developed by Dr. Simson L. Garfinkel as an open source acquisition format  

<br>

Design goals  
1. Provide compressed or uncompressed image files  
2. No size restriction for disk-to-image files  
3. Provide space in the image file or segmented files for metadata  
4. Simple design with extensibility  
5. Open source for multiple platforms and OSes  
6. Vendors will have no implementation restrictions on this format. Possibly the future standard  
7. Internal consistency checks for self-authentication  

<br>

File extensions include <b>.afd</b> for segmented image files and <b>.afm</b> for AFF metadata  

AFF is <b>open source</b>  

<br>

## Determining the <b>Best Acquisition Method</b>  

Types of acquisitions include <b>Static acquisitions</b> and <b>Live acquisitions</b>  

<br>

4 methods of data collection  
* Creating a disk-to-image file  
* Creating a disk-to-disk  
* Creating a logical disk-to-disk  
* Creating a sparse data copy of a file or folder  

<br>

<b>Determining the best method depends on the circumstances of the investigation</b>  

<br>

Creating a <b>disk-to-image file</b>  
* Most common method and offers most flexibility  
* Can make more than 1 copy  
* Copies are bit-for-bit replications of the original drive  
* ProDiscover, EnCase, FTK, SMART, Sleuth Kit, X-Ways, iLookIX - Tools that perform disk-to-image file copy. These programs read the disk-to-image file as though it were the original disk  

<br>

Creating a <b>disk-to-disk</b>  
* When disk-to-image copy is not possible  
* Tools can adjust disk's geometry (track, sectors, etc) configuration  
* EnCase, SnapCopy, SafeBack  

<br>

<b>Logical acquisition</b> or <b>sparse acquisition</b> (Collect evidence from a large device can take several hours). Reasons for using these acquisition methods:  
* Use when your time is limited as <b>Logical acquisition</b> captures only specific files of interest to the case (i.e. only want to investigate outlook email) and <b>Sparse acquisition</b> collects fragments of unallocated (deleted) data  
* For large disks  
* For PST or OST mail files, RAID servers (can be up to a several TBytes)  

<br>

When making a copy, consider:  
* Size of the source disk, lossless compression might be useful (does not permanently remove data, original data can be reconstructed) - Target does not need to be so big. Use digital signatures for verification  
* When working with large drives, an alternative <b>is using tape backup systems</b> (i.e. SDLT. Can be slow if data is large)  
* <b>Whether you can retain the disk</b>: Sometime after copy, the original disk may need to be return to their owners  

<br>

## <b>Contingency Planning</b> for Image Acquisitions  

Create a duplicate copy of your evidence image file  
* In case of failure but can be time consuming  

<br>

Make <b>at least 2 images</b> of digital evidence  
* Use different tools (Encase/Prodiscover) or techniques  

<br>

Copy <b>host protected area</b> (<b>HPA</b> - An area not visible for OS on drive) of a disk drive as well  
* Consider using a hardware acquisition tool that can access the drive at the BIOS level so as to access HPA  

<br>

Be prepared to deal with encrypted drives  
* <b>Whole disk encryption</b> feature in Windows called <b>BitLocker</b> makes static acquisitions more difficult  
* May require user to provide decryption key - suspect may not cooperate  

<br>

## Using Acquisition Tools  

### Acquisition tools for Windows  

Advantages  
* Make acquiring evidence from a suspect drive more <b>convenient</b>  
* Many tools developed for Windows platform  
* Especially when used with hot-swappable devices (i.e. USB, Fireware)  

<br>

Disadvantages  
* Must protect acquired data with a <b>well-tested write-blocking</b> hardware device  
* Tools can't acquire data from a disk's host protected area  
* Some countries haven't accepted the use of write-blocking devices for data acquisitions (Need to check with legal)  

<br>

## Capturing an Image with ProDiscover Basic  

Connecting the suspect's drive to your workstation  
* Document the chain of evidence for the drive  
* Remove the drive from the suspect's PC  
* Configure the suspect drive's jumpers as needed  
* Connect the suspect's drive to a write-blocker device  
* Create a storage folder on the target drive  

<br>

Using ProDiscover's Proprietary Acquisition Format  
* Refer to <b>"Guide to Computer and Forensics And Investigations"</b> for details to start ProDiscover Basic and configure settings for acquisition  
* ProDiscover creates image files with an <b>.eve</b> extension, a log file (<b>.log</b> extension), and a special inventory file (<b>.pds</b> extension)  
* If the compression option was selected, ProDiscover uses a <b>.cmp</b> rather than an .eve extension on all segmented volumes  

<br>

## Capturing an Image with AccessData <b>FTK</b> Imager Lite  

### Another New Forensic Tool  

FTK Imager is a Windows data acquisition tool that's included within the AccessData Forensic Toolkit  

Designed for viewing evidence disks and disk-to-image files  

<br>

Makes disk-to-image copies of evidence drives  
* At logical partition and physical drive level  
* Can segment the image file  

<br>

Evidence drive must have a hardware write-blocking device  
* Or run from a Live CD, such as Mini-WinFE  

<br>

FTK Imager can't acquire a drive's Host Protected Area (HPA)  

<br>

Use a write-blocking device and follow these steps  
* Boot to Windows  
* Connect evidence disk to a write-blocker  
* Connect target disk to write-blocker  
* Start FTK Imager Lite  
* Create Disk Image - use Physical Drive option  

<br>

## Validating Data Acquisitions  

Validating evidence may be the most critical aspect of PC forensics  

Requires using a <b>hashing algorithm utility</b>  

<br>

Validation techniques  
* CRC-32, MD5, and SHA-1 to SHA-512  

<br>

## Windows Validation Methods  

Windows has no built-in hashing algorithm tools for PC forensics  
* 3rd party utilities can be used: hexadecimal editors such as WinHex  

<br>

Commercial PC forensics programs have built-in validation features  
* Each program has its own validation technique  
* <b>ProDiscover's .eve files</b> contain <b>metadata</b> in the acquisition file or segmented files, including the hash value for the suspect drive or partition  

<br>

Raw format image files don't contain metadata  
* Separate manual validation is recommended for all raw acquisitions  

<br>

## Using Remote Network Acquisition Tools  

You can <b>remotely connect</b> to a suspect PC via a network connection and copy data from it  

<br>

Remote acquisition tools vary in configurations and capabilities  
* i.e. Some require manual intervention on remote suspect PCs to initiate the data copy  

<br>

Many tools such as EnCase, ProDiscover allow remote acquisition  

<br>

Drawbacks  
* Antivirus, antispyware, and firewall tools can be configured to ignore remote access programs - access could be blocked  
* Suspects could easily install their own security tools that trigger an alarm to notify them of remote access intrusions  

<br>

## Remote Acquisition Tool  

Other functions may include:  
1. Capture volatile system state info  
2. Analyse current running processes on a remote system  
3. Locate unseen files and processes on a remote system that might be running malware or spyware  
4. Remotely view and listen to IP ports on a compromised system  
5. Run hash comparisons on a remote system to search for known Trojans and rootkits  
6. Create a hash inventory of all files on a system remotely (a negative hash search capability) to establish a baseline if it gets attacked  

<br>

## Using Other Forensics-Acquisition Tools  

Other commercial acquisition tools  
* <b>Magnet Axiom</b>  
* <b>PassMark</b> Software ImageUSB  
* ASRData SMART  
* <b>Runtime</b> Software  
* ILookIX Investigator IXimager  
* <b>SourceForge Projects Repository</b>  

<br>

## Magnet Axiom  

Like many forensics tools, <b>MA is able to recover digital evidence from most sources, including smartphones, cloud services, PCs, IoT devices and 3rd party images</b>  

The examination tool helps forensics professionals find most relevant data and <b>visualize</b> it for better analysis  

This tool is gaining popularity as it's user base increases

<br>

## <b>PassMark Software</b> ImageUSB  

<b>PassMark Software</b> has an acquisition tool called <b>ImageUSB</b> for its <b>OSForensics analysis</b> product  

<b>ImageUSB</b> downloaded from the OSForensiccs Website  

<br>

<b>ImageUSB</b> is a free utility  
* You can write an image concurrently to multiple USB Flash Drives  

<br>

## <b>Runtime</b> Software  

