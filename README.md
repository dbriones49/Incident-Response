# Incident response (Live Traffic)

![image](https://github.com/dbriones49/Azure-SOC/assets/143753667/c278c18d-e192-4f6e-9ede-654f03a81479)


## Introduction
The Honeynet has now been constructed, and i then assigned a myself a brute force incident to respond to. I used the NIST 800-61 framework to complete the incident response. After the incident response is complete, I will apply controls 
to harden the resources and re pull maps to assess the before and after of the security controls implimented. 

## Incident Description:
- This incident involves observation of potential brute force attempts against an Windows virtual machine. Below are the action items taken. 

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



# Azure Instances
![image](https://github.com/dbriones49/Azure-SOC/assets/143753667/35fe6cdb-c3b7-4602-aa17-c68c8d91ac28)


# Configured windows registry
Once SQL server was installed, I configured windows registry to provide full permissions to the server. Configurations were made in Windows Registry. Once completed, audit access was configured using auditpol.

![image](https://github.com/dbriones49/Azure-SOC/assets/143753667/7326f527-5d12-45c8-93ca-a166269e6556)








## Conclusion

In this project, a mini honeynet was constructed in Microsoft Azure and log sources were integrated into a Log Analytics workspace. Microsoft Sentinel was employed to trigger alerts and create incidents based on the ingested logs. Additionally, metrics were measured in the insecure environment before security controls were applied, and then again after implementing security measures. It is noteworthy that the number of security events and incidents were drastically reduced after the security controls were applied, demonstrating their effectiveness.
