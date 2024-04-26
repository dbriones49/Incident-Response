# Incident response (Live Traffic)




## Introduction
The Honeynet has now been constructed, and I then assigned a myself a brute force incident to respond to. I used the NIST 800-61 framework to complete the incident response. After the incident response was complete, I applied controls 
to harden the resources and re pulled maps to assess the before and after of the security controls implimented. 

## Incident Description:
- This incident involved observation of potential brute force attempts against an Windows virtual machine. Below were the action items taken. 

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


