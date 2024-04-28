# Incident response (Live Traffic)




## Introduction
I used the NIST 800-61 to respsond to and mitigate the noted brute force attacks that the honeynet produced.   Using NIST 800-61 is important when completing an incident response on a cyber attack because it provides a comprehensive framework for effectively responding to and mitigating the impact of security indidents. By following the guidelines outline in NIST 800-61, organization can ensure a strucuted and systematic appraoch to indident resonse, leading to quicker detection, containement, and recover from cyber attacks. Additionally, utilizing NIST 800-61 can help organizations improve thier overall cybersecurity posture and better protect their sensitive data and systems from future attacks. 


## Incident Description:
- This incident involved observation of potential brute force attempts against an Windows virtual machine. Below were the action items taken.



![image](https://github.com/dbriones49/Incident-Response/assets/143753667/1ae97c06-4065-4122-8323-3377aae59d06)



## Step 1: Preperation
- ( I initially completed this earlier by ingesting all logs into the Log Analytics Workspace and Sentinel, and configured the alert rules)


## Step 2: Detection & Analysis
- Set Severity, Status, Owner
- View Full Details( New Experieince)
- Observe the Activity Logs( For history of incident)
- Observe Entities and Incident Timelines ( are they doing anything else?)
- "Investigate" the incident and continue trying to determine the scope
- Inspect the entities and see if there are any related issues.
- Determine legitimacy of the indident( True Positive, Fals Positive, etc.)
- If true positive, continue. If false positive, close the ticket.

## Step 3: Cpontainment, Eredaction, and Recovery
- Use the Incident response play book


## Step 4: Document findings/information, and close out the incident in Sentinel
  







## Initial Response Actions
- Verify the authenticity of the alert or report
- Immediately isolate the machine and change the password of the affected user
- Identity the orgin of the attacks and determine if they are attacking or involved with anything else
- Determine how and when the attack occured( are the NSGS not being locked down? If so, check the other NSGs
- Assess the potential impact of the incident( what type of account was it? Permissions?)

## Containment and Recovery
- Lock down the NSG asssigned to the VM/Subnet, either entirely, or to allow only necessary traffic.
- Reset thh affected user's password
- Enable MFA

 ## Document Findings and Close out Incident












## Conclusion


