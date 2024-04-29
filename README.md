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
- Observe Entities and Incident Timelines (are they doing anything else?)
- "Investigate" the incident and continue trying to determine the scope
- Inspect the entities and see if there are any related issues.
- Determine legitimacy of the indident( True Positive, False Positive, etc.)
- If true positive, continue. If false positive, close the ticket.

## Step 3: Containment, Eredaction, and Recovery
- Use the Incident response play book ( SOP). AZURE has playbook functionality built in. 


## Step 4: Document findings/information, and close out the incident in Sentinel
  





## Detection & Analysis/ Observe the Activity Logs
To begin, I filtered Sentinel by severity. For this example, I addressed one of the few high severity alerts. I assigned the task to myself and statused the incident as "active".

![image](https://github.com/dbriones49/Incident-Response/assets/143753667/9d7bd041-616e-4970-a665-b78fa074d6e9)


![image](https://github.com/dbriones49/Incident-Response/assets/143753667/4329508a-8ba6-4194-8826-6f63c1f2ea4d)


## View Full Details.
The event details for each attempt can be viewed in Sentinel. From here I took notes to document the ticket at a later time(timeline, entities, etc.).


![image](https://github.com/dbriones49/Incident-Response/assets/143753667/54195b25-7ba8-43cb-98ee-195450d6fbd7)




## Investigate the incident.
By Reviewing the investigation screen, we can determine the scope of the attack. I could see that the attacker was involved in 17 total brute for attempts. I also inspected the host instance as well and determined that the host was involved in 17 other attacks. 


![image](https://github.com/dbriones49/Incident-Response/assets/143753667/60da6b6e-0698-41e8-8538-1e9f863c1f8e)


![image](https://github.com/dbriones49/Incident-Response/assets/143753667/17ec5de8-3621-42e4-b532-34b01f199451)



## Determine the legitimacy of the incident.
It is import to confirm if the incidents are true positives or false positives. You can confirm this by pulling the oringal alert query and then running specific variations of the query to determine itmes like IP origin, departmnet, etc. You can also confirm with your manager if there has been any recent testing that may have triggered the alerts. In this case, the Matching IP is tied to the attacker VM I created and therefore the incident is deemed as a false positive. 





![image](https://github.com/dbriones49/Incident-Response/assets/143753667/02e2adc0-a577-48cf-8cf6-7cc267b46325)


![image](https://github.com/dbriones49/Incident-Response/assets/143753667/10b872bb-252a-4b2d-b35d-9cd1cc5f2609)




## Containment, Eredaction, and Recovery.

For this phase, I relied on the IR playbook, specically assigned to the resource (Azure Active Directory) and type of incident. For this the actions needed will be to  Lockdown the NSG assigned to the VM, reset the user's password, and enable MFA. I deemed this as a false positive, so I did not change the password, nor did I isolate the machine. However, I did lock down the NSG firewalls. 




![image](https://github.com/dbriones49/Incident-Response/assets/143753667/3107dc02-b69b-4478-a8a9-9b8b7c159895)



![image](https://github.com/dbriones49/Incident-Response/assets/143753667/3a30bf1c-7245-4f3e-916d-99eff5468048)


Next, I enabled the built in firewall in the Key Vault and created a private endpoint for it, which will make it accessible only from the subnet. Public access to the Storage Accounts were also disabled.

![image](https://github.com/dbriones49/Incident-Response/assets/143753667/72d89802-7584-4c62-b24a-f905c3c51595)


![image](https://github.com/dbriones49/Incident-Response/assets/143753667/a8441724-037b-4be7-85d9-cbec10fbb154)




![image](https://github.com/dbriones49/Incident-Response/assets/143753667/abb81233-a5ed-45b6-9385-cd8621ca41ef)








Microsoft Defender also provides recommendations of key action items to take from a NIST 800-53 compliance standpoint, that will bring the environment back up to par.   



![image](https://github.com/dbriones49/Incident-Response/assets/143753667/e55419b7-5e64-47f4-b9fa-863e5c4f223f)











 ## Document Findings and Close out Incident
 Finally, I entered in my findings in Sentinel, and closed out the ticket.
 


![image](https://github.com/dbriones49/Incident-Response/assets/143753667/e2b57f17-1421-409a-9903-ea7a51b08aa1)










## Conclusion


