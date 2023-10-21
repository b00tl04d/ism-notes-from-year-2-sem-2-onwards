# Navigation
* [Key Definitions](#key-definitions)  
* [Incident Lifecycle](#incident-lifecycle)  
* [Purpose and Objectives](#purpose-and-objectives)  
* [Value to business](#value-to-business)  
* [Incident Priority](#incident-priority)  
* [Incident Priority and Target resolution times](#incident-priority-and-target-resolution-times)  
* [Major Incidents](#major-incidents)  
* [Escalations - Hierarchical & Functional](#escalations---hierarchical--functional)  
* [Standard Incident Models](#standard-incident-models)  
* [Process Workflow](#process-workflow)  
* [Process Interfaces](#process-interfaces)  
* [Challenges](#challenges)  
* [Risks](#risks)  
* [Critical success factors (CSF) & Key Performance Indicators (KPI)](#critical-success-factors-csf--key-performance-indicators-kpi)  
* [Roles and Responsibilities](#roles)  

<br>

## Key Definitions  

Incident (generally a negative event. In the case of IT and cyber security, listed below are a few examples)  
* Unplanned interruption to an IT service  
* Reduction in the quality of an IT service  
* Failure of a CI that has not yet impacted an IT service  

<br>

Service Request (formal request from a user for something to be provided)  
* Request for info or advice; to reset a password; or to install a workstation for a new user  
* NOT a disruption to the agreed service  
* Request Fulfilment process. Manages lifecycle of Service Requests  

<br>

Workaround (Method of bypassing an Incident or Problem, a temporary fix)  
* It is <b>not a permanent solution</b> but something used to get the service up and running till the real solution is found  

<br>


## Incident Lifecycle  

Status codes to indicate where incidents are in relation to their lifecycle/status  

Incident management is the process responsible for managing the lifecycle of all incidents  

5 of them:  

* Open  
* In progress  
* Resolved  
* Closed  
* (Pending)  

<br>


## Purpose and Objectives  

Purpose  
* <b>Restore normal service operations as quickly as possible</b>  
* Minimize the adverse impact on business  
* Ensuring best possible levels of service quality and availability are maintained according to SLA's (Service Level Agreements or Terms and Conditions)  

<br>

Objectives  
* Standardized methods and procedures  
* Increased visibility and better communication  
* Priorities aligned with business  
* User satisfaction with the quality of IT services  

<br>


## Value to business  

* Reducing service downtime  
* Reducing Incident impact to business  
* Aligning IT to business priority  
* Identify possible improvements to service  
* Identification of additional requirements (e.g. training, new service) as a result of handling multiple incidents  

<br>

Note: Value of IM is highly visible to the business. For this reason, IM is often one of the first processes to be implemented in Service Management projects  

<br>


## Incident Priority  

* Assigned, to ensure that the support groups will pay the required attention to the incident  
* Based on the Urgency and Impact  

<br>

General formula is...  
Impact + Urgency = Priority  

Impact: How much damage, if not fixed soon?

Urgency: How fast does it need to be fixed  

<br>


## Incident Priority & Timescales  

Must be agreed for all incident-handling stages  

Based upon the overall incident response and resolution targets within SLAs  

Captured as targets within OLAs and Underpinning Contracts (UCs)  

Support groups should be made aware of these timescales  

Service Management tools automate and escalate as required  

<br>

Example of priority coding system  
![image](../images/Pasted%20image%2020231021153015.png)  

<br>


## Major Incidents  

<b>Major Incident</b> = High Impact + High Urgency  

Highest category of impact for an incident  

Results in significant disruption to the business  

Should have separate procedure  

<br>

<b>A separate procedure (for major incidents)</b>
* Shorter timescales and greater urgency  
* Separate major incident team under the direct leadership of the incident manager  
* Informing Management and Customer  
* Service Desk ensures that all activities are recorded and users are kept fully informed of the progress  

<br>


## Escalations - Hierarchical & Functional  

<b>Escalation</b> is the mechanism that assists timely resolution of an Incident  

<b>Hierarchical Escalation</b> can take place at any moment during resolution  

Possible reasons
* SLA threat  
* Extra resources required  
* Need to inform higher management  

<br>

<b>Functional Escalation</b> means involving more specialist personnel or access privileges to solve the incident. Departmental boundaries may be exceeded  

![image](../images/Pasted%20image%2020231021154107.png)  

<br>


## Standard Incident models  

Designed and implemented for handling standard (reoccurring) incidents more efficiently  

An Incident Model should including the following:
* Steps required to handle the incident and their order  
* Responsibilities  
* Timescales and thresholds for completion  
* Any escalation procedure  
* Any evidence prevention activities  

<b>Support tools can then be used to automate handling of standard incidents</b>  

<br>


## Process Workflow  

Overall diagram  
![image](../images/Pasted%20image%2020231021162118.png)  

<br>

### Incident Identification  

![image](../images/Pasted%20image%2020231021162641.png)  

TRIGGERS: Incidents ... from Event Mgmt, from web interface, from Users, from suppliers, from technical Stuff  

<br>

Incident Identification:  
* Usually it's unacceptable to wait until a user logs an incident  

<br>

Monitoring assures:
* Early detection of Failure/potential failure  
* Quick start of Incident Management  

<br>

IDEAL SITUATION: <b>Incident is resolved before it had an influence on users</b>

<br>

### Incident Logging  

![image](../images/Pasted%20image%2020231021162716.png)  

<b>All incidents</b> must be
* Fully logged (INC. NO., DATE, TIME, OWNER, CONTACT... )  
* and date/time stamped;  
* Full historical record of all incidents must be maintained  

<br>

"Opportunity fixes" must also be logged (ALL must be logged)  

Incident is logged -> <b>Resolution time count starts</b>  

<br>

### Incident Categorization  

![image](../images/Pasted%20image%2020231021162949.png)  

Categorization indicates the <b>type of incident</b> being logged  

Category is often related to team that will handle the incident from the Service Desk  

Categories are often multi-level  
For Example:  
- Hardware – Server – Memory Board – Card Failure  
- Software – Application – Finance Suite – Purchase Order System 

It's useful if incident and problem categories are alike  

<br>

### Service Request?  

![image](../images/Pasted%20image%2020231021163305.png)  

A part of categorisation will be to <b>check if it's a Service Request</b>
* If it is -> It will be transferred to Request Fulfilment process  

Requests are not incidents and should be handled differently  

<br>

### Incident Prioritization  

![image](../images/Pasted%20image%2020231021163432.png)  

Prioritisation determines how the incident will be handled by support staff and by support tools  

Remember: <b>PRIORITY = Urgency + Impact (+ SLA)</b>  

High &nbsp;&nbsp; Medium &nbsp;&nbsp; Low &nbsp;&nbsp; Priority code &nbsp;&nbsp; Description &nbsp;&nbsp; Target Resolution Time  

<br>

### Major Incident?  

![image](../images/Pasted%20image%2020231021163732.png)  

If priority indicates Major Incident it must be handled by following the Major Incident Procedure  

Staff must be familiar with the procedure  

<br>

### Incident Diagnosis  

![image](../images/Pasted%20image%2020231021164304.png)  

Service Desk Analyst will determine with the user
* Full symptoms (what has gone wrong)  
* How to correct it?

<br>

(Correcting methods) using
* Diagnostic scripts  
* Known Error information  

If the incident is resolved -> it will be closed (after informing the user)  

<br>

### Functional Escalation  

![image](../images/Pasted%20image%2020231021164339.png)  

If the incident is NOT resolved -> it will be escalated (and informed to the user)  

<b>Functional Escalation</b> (to the next level of support) occurs when
* Current level of support <b>can't resolve the incident</b>
* Current level of support has <b>reached time scales</b> for resolving the incident  

<br>

Ownership of the incident stays with the Service Desk  

Service Desk will track and monitor progress  

<br>

### Hierarchical Escalation  

![image](../images/Pasted%20image%2020231021164639.png)  

If the incident is NOT resolved -> it will be escalated (and informed to the user)  

<b>Hierarchic Escalation</b> (up the management chain) occurs when  
* SLA breaches are threatened  
* Extra resources are needed to resolved the incident  
* Senior Management needs to be aware/ approve the steps required  

May also be initiated by the customer/user if they see it necessary  

<br>

### Investigation & Diagnosis  

![image](../images/Pasted%20image%2020231021165339.png)  

More information might be collected on
* Exactly what has gone wrong  
* Understanding the chronological order of events  
* Confirming the full impact  
* Identifying events that may have triggered the incident  
* Knowledge searches  
* Previous incidents  
* Changes made  

<br>

All actions and findings must be recorded  

As much actions as possible should be performed in parallel to save time  

<br>

### Resolution and Recovery  

![image](../images/Pasted%20image%2020231021165544.png)  

When the resolution has been identified it should be applied and tested  

If satisfactory, a time / date stamp is recorded as this is the end of downtime  

The incident record must be updated with the details of actions taken  

The incident should be returned to the Service Desk for closure action  

<br>

### Incident Closure  

![image](../images/Pasted%20image%2020231021165756.png)  

Before closing the incident the SD Analyst must
* Make sure the user is informed and happy with the solution  
* The assigned incident category is the correct one (if not, correct it)  
* The incident documentation is complete  

<br>

The incident is closed by Service Desk  

<b>Re-opening incidents</b> - strict rules must exist for this action  

<br>


## Process Interfaces

Event Mgmt  
* Event can (automatically) raise incident  

<br>

Request Fulfilment  
* Request handling can also be handled by IM process  

<br>

Problem Management  
* Incidents (repeated) often point to problems  
* Solving the problems should reduce the number of incidents  

<br>

Asset & Configuration Mgmt  
* Provides data used to identify and progress incidents  
* IM assists in verification of CMS  

<br>

Change Management  
* Changes are often reasons why incidents occur  
* Incidents can lead to changes required for resolutions/workarounds  

<br>

Service Level Management  
* IM must restore service as agreed in SLAs - thus, targets for IM are determined considering SLM and vice-versa  

<br>

Service Catalogue Management  
* Service Desk will consult Service Catalogue in handling incidents  

<br>

Capacity Management  
* IM may trigger monitoring of a system or service performed by Capacity Management  
* Workarounds used by Incident Management can come from Capacity Management  

<br>

Availability Management  
* Incident data is important in determining availability  

<br>


## Challenges  

Ability to <b>detect incidents as early as possible</b>  

Convincing all staff that <b>ALL incidents must be logged</b>  

Making <b>information available about known errors</b> to ensure staff learn from previous incidents  

<b>Configuration Management System integration</b>  

<b>Integration into the Service Level Management processes</b> in order to correctly assess the impact and priority of incidents  

Defining <b>escalation procedures</b>  

<br>


## Risks  

Incidents not being handled in appropriate timescales  

Insufficient incident backlog  

Poor information availability (for resolving/escalating...)  

<br>

Mismatch in objectives/expectations for Incident Management  
* Due to a lack of or inappropriate training?  
* Due to inadequate support tools?  
* Due to lack of support tools integration?  
* Due to poorly-aligned or non-existent OLAs or UCs/SLAs?  
* or due to other reasons...  

<br>


## Critical Success Factors (CSF) & Key performance Indicators (KPI)  

Examples  

<b>CSF Resolve incidents as quickly as possible minimizing impacts to the business</b>
* <b>KPI</b> mean elapsed time to achieve incident resolution or circumvention, broken down by impact code  
* <b>KPI</b> breakdown of incidents at each stage (e.g. logged, work in progress, closed, ....etc)  
* <b>KPI</b> percentage of incidents closed by the service desk without reference to other levels of support (often referred to as 'first point of contact')  
* <b>KPI</b> number and percentage of incidents resolved remotely, without the need for a visit  

<br>

<b>CSF Maintain quality of IT services</b>  
* <b>KPI</b> total numbers of incidents (as a control measure)  
* <b>KPI</b> size of current incident backlog for each IT service  
* <b>KPI</b> number and percentage of major incidents for each IT service  

<br>

<b>CSF Maintain user satisfaction with IT services</b>  
* <b>KPI</b> Average user/customer survey score (total and by question category)  
* <b>KPI</b> Percentage of satisfaction surveys answered versus total number of satisfaction surveys sent  

<br>


## Roles  

Incident Management Process Owner
* accountable for the process  

<br>

Incident Manager, manages the work of Incident Support Staff
* Developing and maintaining IM process and procedures (driving efficiency and effectiveness)  
* Managing the work of incident support staff (first and second-line)  
* Managing Major Incidents  
* Monitoring the effectiveness of IM ... recommending improvement  
* Developing and maintaining the IM systems  
* Producing management information  

<br>

1st line support (normally the service desk)  
* Identify, log, categorize, prioritize, diagnose, resolve/escalate and close an incident  

<br>

2nd line support (generally Technical/Application Management)  
* Investigate, diagnose, resolve (recover) an incident  

<br>

3rd line support (External experts or Internal ones)  
* Investigate, diagnose, resolve (recover) an incident  


