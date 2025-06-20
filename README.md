# Snort - Network Intrusion Detection System


This project demonstrates a **Network Intrusion Detection System (NIDS)** built with **Snort** in a controlled, isolated lab environment. The goal is to configure and test Snort to detect and analyze malicious network traffic, simulating real-world cyber attacks to enhance understanding of intrusion detection. Hosted in **Oracle VirtualBox** on a **Host-Only network** (`192.168.56.0/24`). 

Key activities include:
- Simulating attacks to trigger Snort alerts, testing rules in `/etc/snort/rules/local.rules`.
- Troubleshooting setup and simulation issues like network configuration.
- Recording lab sessions with **OBS Studio** for documentation.
- Logging errors and fixes to build a comprehensive learning resource.



##  Project Structure

- **Environment:**
  - **Ubuntu 24.04 LTS** ("Voldemort", `192.168.56.103`): Runs Snort to monitor traffic and detect attacks using custom and Snort Community Rules.  
  - **Kali Linux** (`192.168.56.102`): Serves as the attacker, launching simulations such as FTP logins, HTTP directory traversal, and ping sweeps with tools like `netcat`, `scapy`, and `nmap`. 
  - **Metasploitable 2** (`192.168.56.104`): Acts as the vulnerable target, hosting exploitable services like FTP, HTTP, and SSH.


##  Tools Used

- **Snort** V 2.9
- **Vim** Text editor 
- **Snorpy** Web Rule builder
- **Wireshark** Packet analysis
- **Google Doc** For Documentation

##  File Included

- Full Project Pdf
- Tools and Installation Guide
- Screenshots

##  Author

- **Name:** Owolabi Ridwan Ishola
- **Date:** 20/06/2025

This repository contains Snort configurations, rules, attack scripts, screen recordings, and a detailed error log, serving as a practical guide for network security and IDS deployment.

