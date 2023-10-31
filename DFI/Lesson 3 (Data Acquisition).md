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

