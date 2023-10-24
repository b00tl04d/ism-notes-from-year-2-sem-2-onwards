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

<br>


## Incident Handling Boundaries  

Department Manager suspects an employee is using the company's official email to lend credibility to himself, so that he can conduct a profit making businesses  

<br>

Department Manager puts up a request to:  
* Access a staff member's email  
* Track a staff members activities  
* Copy a staff member's hard drive when he is away  

<br>

Should we do that?  

<br>


## OODA loop  

Concepts developed by USAF <b>Colonel John Boyd</b> for air-to-air combat, later extended to organizations  

Decision-making occurs in a recurring cycle of <b>observe-orient-decide-act</b>  

An entity (whether an individual or an organization) that can process this cycle quickly, observing and reacting to unfolding events more rapidly than an opponent can thereby "get inside" the opponent's decision cycle and gain the advantage  

<br>

Diagram of the OODA loop (source: https://commons.wikimedia.org/w/index.php?curid=3904554)  
![image](../images/Pasted%20image%2020231024172124.png)  

<br>


## Conflict in Incident Handling  

![image](../images/Pasted%20image%2020231024172207.png)  

<br>


## Real Example of Detection, Analysis and Response - Silicon SOC  

Example  
```
Detection :Silicon SOC received an corelated alert on Exploit.url.MVX – Host IP: 10.67.25.197 Date: 26 Feb 2016 10.22:06 SGT  

These behaviours were observed: Suspicious JS Activity, Exploit Code Generic Detection, Evasion Behaviour, Exploit code Activity  

Analysis: The incident was analysed and the compromised site that was surfed by the user is summarised as such  

• GET Request: hxxp://super.koumas.net/boards/viewforum.php? f=a87&sid=59_huz5pl0p9v1d4a07t7zyzgp7g7tklnwawie7lofiwwz9xsb3- 5txyiettf5k23nn2sqs3_36eujtvflqgx4z3nfl5lgj2q  

• Referrer: hxxp://news.geltuihameleon.info/hellomylittlepiggy/search/? keyword=84190  

• Malicious Host: hxxp://super.koumas.net  
```

<br>

Further analysis shows that the user is browsing the website "hxxp\[://\]www\[.\]acetraining\[.\]com\[.\]sg/index\[.\]php/course/photoshop-cc-camera-raw/"  

Which causes the first redirect to an encoded URL of "hxxp\[://\]news\[.\]geltuihameleon\[.\]info/hellomylittlepiggy/?tLEYlnzXlL=mOgjKAPr&Xyatnm=fuObOsjP&keyword=269d169903fd859965d8673c54354c75&ARumlXdxCbVUns=sbSfsvHL&TmxBJHkoPDGfcO=suBKPjPgciz&JQkHhCEwi=EYOgToHPvYlPfpeY&pXfiYXbpSuoPlkJRkKQ=LkiqOynEXw&aruMGr=BpkBhIRsugmGyV&muOdlOBZeP=SZGZaHy&aMzXzkZpcsAAueRtE=KgZimbmwemCXpS" being served to the user  

From the first redirect URL, it goes to the second redirect URL "hxxp\[://\]news\[.\]geltuihameleon\[.\]info/hellomylittlepiggy/search/?keyword=84190"  

After which, it redirects again to the infected URL "hxxp\[://\]super[.]koumas[.]net/boards/viewforum[.]php?f=a87&sid=59_huz5pl0p9v1d4a07t7zyzgp7g7tklnwawie7lofiwwz9xsb3-5txyiettf5k23nn2sqs3_36eujtvflqgx4z3nfl5lgj2q"
"hxxp[://]super[.]koumas[.]net/to[.]jss?go=nJmE29EALJ&suppose=&game=N1-W&eye=&rule=NvZw&watch=rpLPWf3YFCQXH__XX3XOnL9HnU9vxn"
"hxxp[://]super[.]koumas[.]net/change[.]wrf?out=&ask=lhOwwlz&drive=&respect=JDTia&literature=spKn&direct=txIdT&however=&close=fjWaE&meeting=kcs8umaaGXwD3xtMwpXeX