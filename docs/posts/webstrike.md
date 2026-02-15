---
draft: false
date: 2026-02-15
categories:
  - Cyber Defenders
  - Network Forensics
---

# Webstrike Lab

**Scenario:** A suspicious file was identified on a company web server, raising alarms within the intranet. The Development team flagged the anomaly, suspecting potential malicious activity. To address the issue, the network team captured critical network traffic and prepared a PCAP file for review.

The task was to analyze the provided PCAP file to uncover how the file appeared and determine the extent of any unauthorized activity.

**Tools Used:**
- WireShark
- AbuseIPDB

## Analysis

### Question 1
Identifying the geographical origin of the attack facilitates the implementation of geo-blocking measures and the analysis of threat intelligence. From which city did the attack originate?

The packet capture contains a total of two IPv4 addresses: `117.11.88.124` & `24.49.63.79`.

![tesst](../assets/Pasted image 20260208223750.png)

Using the `HTTP` filter I was able to determine that the attacker was using IP address `117.11.88.124`. 

![alt text](<Pasted image 20260208224425.png>)

A quick search of this IP address on AbuseIPDB reveals that it is based in China and has a number of reports for suspicious behaviour.