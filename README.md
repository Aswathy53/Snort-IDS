# Network Intrusion Detection System (Snort IDS)

## 1. Project Overview

This project demonstrates the implementation of a Network Intrusion Detection System (NIDS) using Snort 2.9.20.

The lab was developed using Ubuntu Linux as the IDS machine and Kali Linux as the testing machine, running in Oracle VirtualBox.

Custom Snort detection rules were created and tested to monitor selected network traffic and generate alerts for security analysis.

## 2. Project Objectives

- Understand the fundamentals of Network Intrusion Detection Systems.
- Install and configure Snort.
- Develop custom detection rules.
- Monitor and analyse network traffic.
- Generate and interpret security alerts.
- Gain practical experience relevant to SOC Level 1 operations.

## 3. Lab Environment

The project was implemented in a virtual lab environment using the following technologies:

|     Component         |      Details    |
|-----------------------|------------------|
| IDS Machine           | Ubuntu 24.04 LTS |
| Testing Machine       | Kali Linux       |
| IDS Tool              | Snort 2.9.20     |
| Virtualization        | Oracle VirtualBox|
| Network Configuration | NAT Network      |
| Custom Rules          | Snort Local Rules|

### Network Setup

- Ubuntu VM was configured as the IDS monitoring machine.
- Kali Linux was used to generate test network traffic.
- Snort monitored traffic through the Ubuntu network interface.
- Custom rules were used to generate alerts for selected traffic patterns.

## 4. Custom Snort Detection Rules

Five custom detection rules were created and tested during the lab implementation.

| SID | Detection | Description |
|---|---|---|
| 1000001 | ICMP Traffic | Detects ICMP packets such as ping traffic. |
| 1000002 | HTTP Traffic | Detects traffic directed to HTTP port 80. |
| 1000003 | TCP SYN Traffic | Detects TCP SYN packets. |
| 1000004 | SYN Scan Detection | Uses thresholding to identify repeated SYN traffic. |
| 1000005 | UDP Port 53 Traffic | Detects UDP traffic directed to port 53. |

### Rule Testing

The custom rules were validated using Snort's configuration testing option.

```bash
sudo snort -T -c /home/aswathy/local.rules -i enp0s3
```

The configuration validation completed successfully.

### Testing Tools

- Kali Linux: Used to generate test traffic.
- Snort IDS: Monitored network traffic and generated alerts.

### Observed Results

- ICMP traffic detection was tested.
- HTTP traffic detection was tested.
- TCP SYN traffic detection was tested.
- Repeated TCP SYN traffic was tested for threshold-based detection.
- UDP traffic sent to destination port 53 successfully triggered the DNS traffic alert rule.

- ## Project Demonstration

The following screenshots demonstrate Snort IDS configuration, rule validation, and detection of different types of network traffic.

### 1. Snort Version
![Snort Version](screenshots/snort-version.png)

### 2. Rule Validation
![Rule Validation](screenshots/rule-validation.png)

### 3. ICMP Ping Detection
![ICMP Detection](screenshots/icmp-detection.png)

### 4. HTTP Detection
![HTTP Detection](screenshots/http-detection.png)

### 5. TCP SYN Detection
![TCP SYN Detection](screenshots/tcp-syn-detection.png)

### 6. UDP Port 53 Detection
![UDP Detection](screenshots/UDP_port53-detection.png)
