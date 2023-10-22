# Objectives  

Describe how to prepare a <b>digital forensics</b> investigation by taking a <b>systematic approach</b>  

Describe <b>procedures for private-sector</b> digital investigations  

Explain <b>requirements for data recovery</b> workstations and software  

Summarize <b>how to conduct an investigation</b> including critiquing a case  

<br>


# Navigation  
* [Taking a Systematic Approach](#taking-a-systematic-approach)  
* [Assessing the Case](#assessing-the-case)  
* [Planning Your Investigation](#planning-your-investigation)  
* [Securing Your Evidence](#securing-your-evidence)  
* [Procedures for Private-Sector High-Tech Investigations](#procedures-for-private-sector-high-tech-investigations)  
* [Example #1: Employee Termination Cases](#example-1-employee-termination-cases)
* [Example #2: Internet Abuse Investigations](#example-2-internet-abuse-investigations)  
* [Example #3: E-mail Abuse Investigations](#example-3-e-mail-abuse-investigations)  
* [Example #4: Industrial Espionage Investigations](#example-4-industrial-espionage-investigations)  
* [Interviews and Interrogations in High-Tech Investigations](#interviews-and-interrogations-in-high-tech-investigations)  
* [Understanding Data Recovery Workstations and Software](#understanding-data-recovery-workstations-and-software)  
* [Setting Up Your Workstation for Digital Forensics]()  

<br>


## Taking a Systematic Approach  

Steps for problem solving  
1. Make an initial assessment about the type of case you are investigating - <b>i.e interview people, decide on places to visit and ...etc</b>  
2. Determine a preliminary design or approach to the case. <b>i.e when to visit company employees</b>  
3. Create a detailed checklist. <b>Checklist helps you to stay on track</b>  
4. Determine the resources you need. <b>i.e. s/w n h/w</b>  
5. Obtain and copy an evidence drive  
6. Identify the risks. <b>i.e unable to access computer due to change of password</b>  
7. Mitigate or minimize the risks <b>to ensure original evidence is always available</b>
8. Test the design <b>like comparing the hash value</b>  
9. <b>Analyse and recover the digital evidence</b>  
10. <b>Investigate the data you recover</b>  
11. <b>Complete the case report</b>  
12. Critique the case <b>Self-evaluation to improve</b>  

<br>


## Assessing the Case  

Systematically <b>outline</b> the <b>case details</b> includes:
1. Situation: i.e. <b>employee abuse case</b>  
2. Nature of the case: <b>use email for personal matter</b>  
3. Specifics of the case: <b> detailed information of case</b>  
4. Type of evidence: <b> USB drive</b>
5. Known disk format: <b>FAT</b>
6. Location of evidence: <b>USB recovered from employee's desk</b>  

<br>

Based on these details, the case requirements can be determined  

<br>


## Planning Your Investigation  

A basic <b>investigation plan</b> should include the following activities:  
1. Acquire the evidence  
2. Complete an evidence form and establish a <b>chain of custody (helps show where the file came from, who created it, and the type of equipment that was used)</b>  
3. Transport the evidence to a computer forensics lab  
4. Secure evidence in an <b>approved secure container</b>  
5. Prepare your <b>forensics workstation</b>
6. Retrieve the evidence from the secure container <b>(5. To ensure info is confidential. Container should be locked, fireproof locker or cabinet that has limited access)</b>  
7. Make a <b>forensic copy of the evidence</b>  
8. Return the evidence to the secure container  
9. Process the copied evidence with computer forensic tools (i.e Encase)  

<br>

An <b>evidence custody form</b> helps you document what has been done with the original evidence and its forensics copies  
* Also called a <b>chain-of-evidence form</b>  

<br>

2 Types  
* Single-evidence form, lists each piece of evidence on a separate page  
* Multi-evidence form  

<br>

Examples:
* <b>Model number or serial number</b> - List the model number or serial number (if available) of the computer component  
* <b>Evidence recovered</b> by - the name of the investigator who recovered the evidence. The chain of custody starts with this info. The person placing his or her name on this line is responsible for preserving, transporting, and securing the evidence.  
* <b>Date and time</b> - The date and time the evidence was taken into custody  

<br>


## Securing Your Evidence  

Use <b>evidence bags</b> to secure and catalogue the evidence  

<br>

Use computer safe products when collecting computer evidence  
* Antistatic bags
* Antistatic pads  

<br>

Use well padded containers  

<br>

Use <b>evidence tape</b> to seal all openings  
* CD drive bays  
* Insertion slots for power supply electrical cords and USB cables  

<br>

<b>Write your initials on tape</b> to prove that evidence has not been tampered with  

<br>

Consider computer specific temperature and humidity ranges  
* Make sure you have a safe environment for transporting and storing it until a secure evidence container is available  

<br>


## Procedures for Private-Sector High-Tech Investigations  

As an investigator, you need to develop formal procedures and informal checklists  
* To cover all issues important to high-tech investigations  
* Ensures that correct techniques are used in an investigation  
* <b>Different case may have different procedure</b>  

<br>


## Example #1: Employee Termination Cases  

The majority of investigative work for termination cases involves employee abuse of corporate assets  

<br>

Incidents that create a hostile work environment are the predominant types of cases investigated  
* Viewing pornography in the workplace  
* Sending inappropriate e-mails  

<br>

Organizations must have appropriate policies in place - <b>consult HR department</b>  

<br>


## Example #2: Internet Abuse Investigations  

To conduct an investigation you need:
* Organization's <b>Internet proxy server logs</b>  
* Suspect computer's <b>IP address</b>  
* Suspect computer's disk drive  
* Your preferred computer forensics analysis tool  

<br>

Recommended steps
* Use standard forensic analysis techniques and procedures  
* Use appropriate tools to extract all Web page URL info  
* Contact the network firewall admin and request a proxy server log  
* Compare the data recovered from forensic analysis to the proxy server log  
* Continue analysing the computer's disk drive data  

<br>


## Example #3: E-mail Abuse Investigations  

To conduct an investigation you need:
* An electronic copy of the offending e-mail that contains message header data  
* If available, e-mail server log records  
* For e-mail systems that store user's messages on a central server, access to the server  
* Access to the computer so that you can perform a forensic analysis on it  
* Your preferred computer forensics analysis tool  

<br>

Recommended steps:  
* Use the standard forensic analysis techniques  
* Obtain an electronic copy of the suspect's and victim's e-mail folder or data  
* For Web-based e-mail investigations, use tools such as FTK's Internet Keyword Search option to extract all related e-mail address information  
* Examine header data of all messages of interest to the investigation  

<br>


## Example #4: Industrial Espionage Investigations  

All suspected <b>industrial espionage cases</b> should be treated as criminal investigations: <b>Very common</b>  

<br>

<b>Staff needed</b> include:
* <b>Computing investigator</b> who is responsible for disk forensic examinations  
* <b>Technology specialist</b> who is knowledgeable of the suspected compromised technical data  
* <b>Network specialist</b> who can perform log analysis and set up network sniffers  
* <b>Threat assessment specialist</b> (typically an attorney)  

<br>

<b>Guidelines</b> when initiating an investigation  
1. Determine whether this investigation involves a possible industrial espionage incident  
2. Consult with corporate attorneys and upper management  
3. Determine what info is needed to substantiate the allegation  
4. Generate a list of keywords for disk forensics and sniffer monitoring  
5. List and collect resources for the investigation  
6. Determine goal and scope of the investigation  
7. Initiate investigation after approval from management  

<br>

<b>Planning</b> considerations  
1. Examine all e-mail of suspected employees  
2. Search Internet newsgroups or message boards  
3. Initiate physical surveillance  
4. Examine facility physical access logs for sensitive areas  
5. Determine suspect location in relation to the vulnerable asset  
6. Study the suspect's work habits  
7. Collect all incoming and outgoing phone logs  

<br>

<b>Steps to conducting an industrial espionage case</b>  
1. Gather all personnel assigned to the investigation and brief them on the plan  
2. Gather resources to conduct the investigation  
3. Place surveillance systems at key locations  
4. Discreetly gather any additional evidence  
5. Collect all log data form networks and e-mail servers  
6. Report regularly to management and corporate attorneys  
7. Review the investigation's scope with management and corporate attorneys  

<br>


## Interviews and Interrogations in High-Tech Investigations  

Becoming a skilled <b>interviewer and interrogator</b> can take many years of experience  

<br>

Definitions  
* <b>Interview</b>, Usually conducted to collect info from a witness or suspect (About specific facts related to an investigation)  
* <b>Interrogation</b>, Process of trying to get a suspect to confess  

<br>

Role as a computing investigator  
* To instruct the investigator, who is conducting the interview on what questions to ask an what the answers should be  

<br>

Ingredients for a successful interview or interrogation  
* Being patient throughout the session  
* Repeating or rephrasing questions to zero in on specific facts from a reluctant witness or suspect  
* Being tenacious  

<br>


## Understanding <b>Data Recovery Workstations</b> and <b>Software</b>  

Investigations are conducted on a computer forensics lab (or data-recovery lab)  
* In data recovery, the customer or your company just wants the data back  

<br>

<b>Computer forensics workstation</b>
* A specifically configured PC  
* Loaded with additional bays and forensics software  

<br>

To avoid altering the evidence use:  
* <b>Write-blockers devices</b> enable you to boot to Windows without writing data to the evidence drive  

<br>


## Setting Up Your Workstation for Digital Forensics  

Basic requirements  
1. A workstation running Windows XP or later  
2. A write-blocker device: <b>prevents writes to storage devices</b>  
3. Digital forensics <b>acquisition tool</b>  
4. Digital forensics <b>analysis tool</b>  
5. Target drive to receive the source or suspect disk data  
6. Spare PATA (<b>parallel</b>) or SATA (<b>Serial</b>) ports  
7. USB ports  

<br>

Additional useful items  
1. Network interface card (NIC)  
2. Extra USB ports  
3. FireWire (<b>IEEE 1394</b>) 400/800 ports  
4. SCSI card  
5. Disk editor tool  
6. Text editor tool  
7. Graphics viewer program  
8. Other specialized viewing tools  

<br>


## <b>Conducting</b> an Investigation  

Gather resources identified in investigation plan  

<br>

Items needed  
1. Original storage media  
2. Evidence custody form  
3. Evidence container for the storage media  
4. Bit-stream imaging tool  
5. Forensic workstation to copy and examine your evidence  
6. Securable evidence locker, cabinet, or safe  

<br>


## <b>Gathering</b> the Evidence  

Avoid damaging the evidence: <b>Important</b>  

<br>

Steps  
1. Meet the IT manager to interview him  
2. Fill out the <b>evidence form</b>, have the IT manager sign  
3. Place the evidence in a secure container  
4. Carry the evidence to the computer forensics lab  
5. Complete the evidence <b>custody form</b>  
6. Secure evidence by locking the container  

<br>


## Understanding <b>Bit-Stream Copies</b>  

<b>Bit-stream copy</b>  
* Bit-by-bit copy of the original storage medium  
* <b>Exact copy</b> of the original disk  
* Different from a simple backup copy, backup software only copy known files. <b>Backup software cannot copy deleted files, e-mail messages or recover file fragments</b>  

<br>

<b>Bit-stream image</b>  
* File containing the bit-stream copy of all data on a disk or partition  
* Also known as "image" or "image file"  

<br>

Copy image file to a target disk that matches the original disk's manufacturer, size and model  

<br>


## Acquiring an Image of Evidence Media  

First rule of computer forensics  
* <b>Preserve the original evidence</b>  

<br>

Conduct your analysis only on a <b>copy</b> of the data  

<br>

Several vendors provide MS-DOS, Linux, and Windows acquisition tools  
* Windows tools require a write-blocking device when acquiring data from <b>FAT or NTFS</b> file systems  

<br>


## Completing the Case  

You need to produce a <b>final report</b>  
* State what you did and what you found  

<br>

<b>Repeatable findings</b>  
* Repeat the steps and produce the same results  

<br>

If required, use a report template  

<br>

Report should show conclusive evidence  
* Suspect did or did not commit a crime or violate a company policy  

<br>

Keep a written journal of everything you do  
* Your notes can be used in court  

<br>

Answer the six <b>W</b>s:  
* Who, what, when, where, why, and how  

<br>

You must also explain computer and network processes. (<b>good to identify who is your report reader and write something that is suitable for the reader</b>)  

<br>


## <b>Critiquing</b> the Case  

Ask yourself the following questions:  
1. How could you improve your performance in the case?  
2. Did you expect the results you found? Did the case develop in ways you did not expect?  
3. Was the documentation as thorough as it could have been?  
4. What feedback has been received from the requesting source?  
5. Did you discover any new problems? If so, what are they?  
6. Did you use new techniques during the case or during research?  

<br>


## Summary  

Digital forensics involves <b>systematically accumulating and analyzing digital information for use as evidence in civil, criminal, and administrative cases</b>  

Investigators need specialized workstations to examine digital evidence (<b>must always have the right tools!!</b>)  

Public-sector and private-sector investigations differ; public-sector typically require search warrants before seizing digital evidence  

Always use a <b>systematic approach</b> to your investigations  

Always <b>plan</b> a <b>case</b> taking into account the <b>nature of the case, case requirements, and gathering evidence techniques</b>  

Both criminal cases and corporate-policy violations can go to court  

Plan for <b>contingencies</b> for any problems you might encounter  

Keep track of the chain of custody of your evidence  

<b>Internet abuse investigations</b> require examining server log data  

For <b>attorney-client privilege cases</b>, all written communication should remain confidential  

A bit-stream copy is a bit-by-bit duplicate of the original disk  

Always maintain a journal to keep notes on exactly what you did - We always forget!  

You should always <b>critique</b> your own work – review is always necessary!
