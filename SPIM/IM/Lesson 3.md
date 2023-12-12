Log rotation  
Log rotation  
– an active log file is moved to an archive copy, and  
– a new empty file is created for an application to begin writing to  
2 basic types of mechanisms  
•Log rotation scripts  
•The application itself handles log rotation duties  
– Handled by custom-written application code  
– Built-in features of a third-party logging library  
•Application does not need to know that log rotation has  
occurred

Log rotation schemes  
• Time based  
– Hourly, daily, weekly, etc  
• Size based  
– 10 MB, 10 MB, etc  
• Size and time based  
– Log file is archived based on time but each log file  
is also capped at some size

Logback example on log rotation

Logback example on log rotation  
(con’d)  
• Rotate the log  
file each day OR  
when it reaches  
100 MB  
– Manageable  
chunk of log  
data

Logging policy on log retention /  
storage  
• Retention / storage  
– Log storage, accessibility and log destruction  
– Never use a syslog server as a log retention system  
– Storage size per day:  
– Log records (in bytes) per second * 86400 seconds  
– General rule of thumb is to add 25% to your log  
retention capacity needs  
– Distributed storage

High level concerns on planning  
• Accuracy – free from defects or misleading  
information  
– Reduce false positives, e.g.  
– IDS to consult a vulnerability database  
– IDS to implement a policy scheme whereby user  
and group profiles are used to create acceptable  
network usage of individuals

High level concerns on planning  
• Accuracy – free from defects or misleading information  
(cont’d)  
– Timestamp  
– Different vendors use different formats  
– e.g.  
– ISO 8601 standard  
– YYYY-MM-DDTHH:MM:SS.SSS +/-H

High level concerns on planning  
• Integrity  
– Authenticate client and server, encrypt data  
– Send data in clear, but use dedicated network  
– Digital signature  
• Confidence  
– Priority or severity  
– E.g. cisco devices use a scale from 0 through 7  
– Take input from many disjoint areas, and deriving a more  
mature and accurate fact from the set of all inputs

High level concerns on planning  
• Preservation  
• Sanitization  
– Remove or replace the attributes you want sanitized  
• IP address becomes xxx.xxx.xxx.xxx  
– Sanitized log data is extracted and placed into a  
secure file, can be reconstructed at some later point  
• Normalization – translate to a well known log  
event format  
• Challenges with time synchronization