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
