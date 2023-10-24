# Navigation  


## Cyber Incident Response Life Cycle  

![image](../images/Pasted%20image%2020231022191801.png)  

<br>


## Life Cycle - Preparation  

Main goal of preparation phase is to prevent incidents by ensuring that systems, networks, and applications are <u>sufficiently secure in-advance</u>  

Designing the systems securely  

Implementing defence mechanisms  

Proactively looking for threats  

<br>


## Life Cycle - Detection  

Collection and processing data from the system sources (SIEM, IDPSs, Antivirus software and log analysers)  

Classification of cyber incidents by types  

Prioritising cyber incidents  

Managing incidents investigation  

Incident documentation  

<br>


## Sign of incidents  

A <u>precursor</u> is a sign that an incident may occur in the future  

An <u>indication</u> is a sign that an incident may have occurred or may be occurring now  


## Indications of Incident  

The network intrusion detection sensor alerts when a buffer overflow attempt occurs against an FTP server  

The antivirus software alerts when it detects that a host is infected with a worm  

The Web server crashes  

Users complain of slow access to hosts on the Internet  

The application logs multiple failed login attempts from an unfamiliar remote system  

The email admin sees a large number of bounced emails with suspicious content  

The network admin notices an unusual deviation from typical network traffic flows  

.....etc  

<br>


## Incident detection techniques  

Feedback from customers  

Feedback from staff  

System logs and application logs  

Security events log  

Anti-virus, anti-spyware alerts  

File integrity checking software  

Network-based Intrusion detection system  

Host-based Intrusion detection system  

Third-party monitoring service  

<br>


## Life Cycle - Analysis  

Inspecting alerts, raw events, application and system logs  

Working quickly to analyse and validate each incident, following a pre-defined process and documenting each step taken  

Identifying the attacker and targets  

Assessing the risk to business processes  

Escalating to relevant personnel for further analysis, analyse if it is a targeted attack or an in-the-wild threat (stay silent?)  

<br>

Analysis steps:

* Correlation, identify if the detected activity is a characteristic of an intrusion attempt  
* Structural Analysis, identify if the detected activity is a characteristic of a known intrusion path  
* Intrusion Path Analysis, identify if the intended target is vulnerable to the detected activity  
* Behaviour analysis, identify if the detected ability is permitted by security policy  

<br>


## Life Cycle - Containment / Eradication  

Contain the threat  

If it is of a spreading nature, prevent it from spreading further  

Prevent data leakage to the attacker (block communication, disable accounts....)  

Elimination of incident components  

Clean infected machines  

Disable breached accounts  

Evidence should be collected according to procedures that meet all applicable law and regulations  

If the alert is of a known issue, act of predefined knowledge base and decision support  

<br>


## Life Cycle - Recovery  

Restore systems to normal operation  

Revert any limitations that were used for isolation (fw)  

Confirm that the systems are functioning normally  

If needed, restoring systems and/or files from clean backups  

<br>


## Life Cycle - Post-Incident Activity (AR)  

AR meetings with all involved parties after a major incident
* Chain of events (events and times)  
* Findings - what actually happened (unauthorized access)  
* Conclusions - what is the problem that allowed it (open port, weak password...)  
* Recommendations - what needs to be done (action items. Close ports, stronger password...) / Proactive updates (security policy update, training, new product)  

<br>

Updating the knowledge base with the specific incident details for the next time handling  

Recognize security weaknesses and threats  

Identifying and mitigating all vulnerabilities that were exploited  

