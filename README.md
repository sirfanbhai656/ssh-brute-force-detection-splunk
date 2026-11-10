# SSH Brute-Force Detection Using Splunk

## Project Overview

This project demonstrates the detection and analysis of SSH brute-force login attempts using Splunk Enterprise. The investigation was conducted in a controlled virtual lab environment using Kali Linux virtual machines.

A controlled Hydra simulation was performed against a designated target machine to generate SSH authentication events. The target's `auth.log` was collected and analysed in Splunk to identify repeated failed login attempts, source IP addresses, attempted usernames, and event timelines.

## Objectives

- Understand SSH authentication logs.
- Identify failed SSH login attempts.
- Analyse authentication events using Splunk.
- Extract source IP addresses and usernames.
- Identify repeated login patterns.
- Develop basic detection logic for suspicious SSH activity.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Attacker and target virtual machines |
| Splunk Enterprise | Log analysis and security monitoring |
| Hydra | Controlled SSH login simulation |
| auth.log | Authentication log dataset |
| SPL | Security event investigation |

## Lab Environment

- Attacker VM: Kali Linux
- Target VM: Kali Linux
- Log Source: `/var/log/auth.log`
- SIEM Platform: Splunk Enterprise
- Environment: Controlled virtual lab

## Investigation Methodology

1. Prepared attacker and target virtual machines.
2. Verified SSH service and network connectivity.
3. Confirmed authentication log collection in Splunk.
4. Performed a controlled Hydra simulation.
5. Observed generated SSH authentication events.
6. Analysed failed login attempts using SPL.
7. Examined source IP addresses, usernames, and event timelines.
8. Documented investigation findings.

## SPL Queries

The following searches were used during the investigation:

- Search for failed SSH authentication events.
- Count failed authentication events.
- Group failed attempts by source IP.
- Group failed attempts by username.
- Examine authentication event timelines.

Complete queries are available in the `SPL-Queries` directory.

## Results and Findings

The investigation identified:

- Total matching failed authentication events: 4
- Source IP identified: 192.168.231.105
- Usernames observed: kali and irfan-attcker
- Analysis platform: Splunk Enterprise

The observed activity was consistent with repeated SSH login attempts during the controlled simulation. The findings do not independently establish successful unauthorized access or system compromise.

## Repository Structure

- `Project_Report.pdf` – Complete project documentation.
- `Dataset/` – SSH authentication log dataset.
- `SPL-Queries/` – Splunk detection and analysis queries.
- `Screenshots/` – Practical implementation evidence.

## Skills Demonstrated

- Security Information and Event Management (SIEM)
- Splunk Enterprise
- SPL Query Writing
- Linux Authentication Log Analysis
- SSH Security Monitoring
- Brute-Force Detection
- Security Event Investigation
- Basic SOC Analysis

## Conclusion

This project provided practical experience in analysing SSH authentication logs using Splunk. It demonstrated how SOC analysts can investigate repeated authentication failures and identify suspicious login patterns through log analysis.

## Disclaimer

This project was conducted in a controlled virtual lab environment for educational purposes. The SSH login simulation was performed only against a designated lab machine.
