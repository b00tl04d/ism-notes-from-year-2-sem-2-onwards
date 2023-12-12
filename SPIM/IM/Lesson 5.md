■ SEARC  
H  
© Copyright 2017  
NETMONASTERY Inc 8  
6  
Outbound packets from  
known infected sources  
MODEL BUILD  
Complex regression DGN (relearnt)  
- days active, known registrar,  
availability + frequency of  
outbounds  
+ variance of domains  
1. AV Detects a file virus, soon turns to  
be an outbreak with 30% of hosts  
2. First instance 4 months back  
3. Cold trail - similar variant but no  
clues ■  
4. VT match triage with a domain  
5. Exfil packets detected on the  
domain  
6. Domains were being switched  
Threat Intel MATCH!  
LOOKING BACK IN TIME FINDING A DORMANT  
VIRUS  
ACTIONS ON OBJECTIVES  
- EXFIL  
-

Automation  
27

Cyber Threat Hunting  
The what and the why  
Constant Stress About -  
What is that we do not know..  
Did we miss something  
important Do we have a false  
negative?  
■ Constant “churn” of events in the cyber space  
■ Burden of a static rule set in a dynamic world  
■ Overload of information pouring out of the fire  
hose  
“Actively going out to hunt for a security breach or asymptom of attack or vectors of the latest threat”  
Dail  
y  
© Copyright2017 NETMONASTERY  
Inc 8  
8  
Weekl  
y  
Monthl  
y

■ New rules for the SIEM  
■ Validation procedures  
■ Response process  
■ SOC Training /  
Upgrade  
■ Posture review  
Outcome of Threat  
Hunting  
What to expect from a threat hunting  
exercise  
Cyber Threat  
Hunting  
Typical  
Expectations 8  
9

Looking for inbound infections (cnc, infected downloads) - maybe  
malware  
Sample Threat Hunting  
The sequence of events...  
last 10  
days  
Get outbound access from proxy with threat intell hits --  
Wow - we have a 12k hits, need to narrow down  
Get only ones with allowed access - ignore the denied (safe) -- last 10 days  
Yikes - we still have 4k hits, have to pull it down  
further last 10 daysLet’s look for the ones with file downloads only --  
OK - we have 6 hits… good place to start  
Let’s check if these were picked by the AV -- lookups 9  
0

Damn - I have no matches on the AV, look somewhere  
else  
Sample Threat Hunting……… …. …  
contd.  
The sequence of events...  
Look for file / content / hash match on Virustotal --  
9  
1  
Lookup  
I have one confirmed match - yay, where did this come  
fromLook for failures - share, auth etc -- X minus 60 days  
Now - let’s figure out to automate detection for this -- process update  
14 queries later...  
Bingo - it was spoofed email from the team lead - clicked…  
infected

RESOURCES  
Outsourced resource - partner  
3 - 5hrs of hunting per week  
Handoff meetings with the  
SOC Training of operations  
staff  
TOOLS  
Avg  
231  
Queries in a hunting  
session  
2.47s Avg Response time per  
query  
Equals = Lost thought for the  
analyst  
Equals = Death of your logger  
SOAR to the  
rescue  
Tools / Resources  
What do we need

Enrichment - GeoData, Threat Intelligence, Local Context  
Validation - Third Party Validators (Symantec / VirusTotal), UEBA  
Automation - Endpoint (Choke), Proxy, Firewall, Feedforward,  
ITMS