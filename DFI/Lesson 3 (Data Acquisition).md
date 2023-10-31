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
* <b>Whether you can retain the disk</b>: