# Incident response (Live Traffic)

![image](https://github.com/dbriones49/Azure-SOC/assets/143753667/c278c18d-e192-4f6e-9ede-654f03a81479)


# Azure Instances
![image](https://github.com/dbriones49/Azure-SOC/assets/143753667/35fe6cdb-c3b7-4602-aa17-c68c8d91ac28)


# Configured windows registry
Once SQL server was installed, I configured windows registry to provide full permissions to the server. Configurations were made in Windows Registry. Once completed, audit access was configured using auditpol.

![image](https://github.com/dbriones49/Azure-SOC/assets/143753667/7326f527-5d12-45c8-93ca-a166269e6556)













## Metrics Before / Security Controls

The following table shows the metrics we measured in our insecure environment for 24 hours:
Start Time 2023-03-15 17:04:29
Stop Time 2023-03-16 17:04:29

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 19470
| Syslog                   | 3028
| SecurityAlert            | 10
| SecurityIncident         | 348
| AzureNetworkAnalytics_CL | 843




## Conclusion

In this project, a mini honeynet was constructed in Microsoft Azure and log sources were integrated into a Log Analytics workspace. Microsoft Sentinel was employed to trigger alerts and create incidents based on the ingested logs. Additionally, metrics were measured in the insecure environment before security controls were applied, and then again after implementing security measures. It is noteworthy that the number of security events and incidents were drastically reduced after the security controls were applied, demonstrating their effectiveness.
