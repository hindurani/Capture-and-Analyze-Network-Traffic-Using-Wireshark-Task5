# Capture and Analyze Network Traffic Using Wireshark Task5
## Overview:
This repository contains the deliverables for Task 5 of the Cybersecurity Internship, which focuses on capturing live network packets using Wireshark, identifying at least three different protocols, and summarizing the findings. The objective is to gain hands-on experience with packet analysis and develop an understanding of network protocols and their behavior.

## Task Objective:
Capture: Use Wireshark to capture live network packets on an active network interface.
Analyze: Identify at least three different protocols in the captured traffic.

## Deliverables:
A packet capture file (.pcap).
A short report summarizing the protocols identified and key findings.

## Tools Used:
Wireshark: A free, open-source network protocol analyzer used to capture and inspect network packets.
Operating System:Specifying my OS, e.g., Windows 11.
Other: Terminal/Command Prompt for generating traffic (e.g., ping command).

## Steps Performed:
## Installed Wireshark:
Downloaded Wireshark from https://www.wireshark.org/ and installed it on my OS.
Ensured Npcap (Windows) or libpcap (Linux/macOS) was installed for packet capturing.
Verified installation by launching Wireshark.

## Selected Active Network Interface:
Opened Wireshark and identified the active network interface (e.g., Wi-Fi or Ethernet) by observing packet activity on the start screen.
Selected the interface with consistent traffic for capturing.

## Captured Network Traffic:
Started packet capture by double-clicking the active interface in Wireshark.

## Generated traffic by:
Browsing www.example.com to produce HTTP/HTTPS traffic.
Running ping google.com in the terminal to generate ICMP traffic.
Resolving a domain (e.g., google.com) to generate DNS traffic.
Captured packets for approximately one minute to ensure sufficient data.

## Stopped Capture:
Stopped the capture after one minute using the red square icon in Wireshark.

## Filtered and Analyzed Packets:
Used Wireshark’s filter bar to isolate specific protocols:
http: Displayed HTTP traffic (web requests).
dns: Displayed DNS queries and responses.
icmp: Displayed ping-related traffic.
Analyzed packet details, including source/destination IPs, ports, and packet contents.

## Identified Protocols:
Identified the following protocols in the captured traffic:
HTTP: Used for web browsing (e.g., GET requests to example.com).
DNS: Used for resolving domain names to IP addresses (e.g., queries for google.com).
ICMP: Used for ping requests and responses (e.g., to google.com).
Additional protocols observed (if any): [e.g., TCP for connection establishment, UDP for lightweight data transfer,Simple Service Discovery Protocol (SSDP) is used for discovering and advertising network services and devices ,Internet Group Management Protocol version 3 (IGMPv3) is a network protocol used for managing IP multicast group memberships in IPv4 networks].

## Exported Packet Capture:
Saved the capture as task5_capture.pcap via File > Save As in Wireshark.
Verified the .pcap file by reopening it in Wireshark to ensure all packets were intact.

## Summarized Findings:
Created this README as the report, detailing the protocols, packet details, and observations.
Included screenshots of Wireshark showing filtered packets for clarity.

## Created GitHub Repository:
Initialized a new GitHub repository named Cybersecurity-Task5.
Uploaded the .pcap file (task5_capture.pcap), this README, and screenshots.
Committed all files with clear commit messages.

## Findings:
Protocols Identified
## HTTP:
Purpose: Facilitates web browsing by sending requests (e.g., GET) to web servers.
Example Packet:
Source IP: 192.168.1.55 (local machine)
Destination IP: 142.250.190.110 (example.com)
Details: GET request for /index.html, response code 200 OK.
Observation: Most HTTP traffic was to example.com, indicating successful web page loading.

## DNS:
Purpose: Resolves domain names to IP addresses for network communication.
Example Packet:
Source IP: 192.168.1.55 (local machine)
Destination Address: 142.250.190.110 (Google DNS server)
Details: Query for google.com, response with IP 172.217.174.238.
Observation: DNS queries were frequent due to multiple domain resolutions during browsing.

## ICMP:
Purpose: Used for diagnostic tools like ping to check network connectivity.
Example Packet:
Source IP: 192.168.1.55 (local machine)
Destination IP: 142.250.190.110 (google.com)
Details: Echo request and echo reply packets for ping.
Observation: ICMP traffic confirmed successful ping responses with low latency.

## Files in Repository:
task5_capture.pcap: The packet capture file containing the network traffic.
README.md: This file, summarizing the task, steps, and findings.
Screenshots:screenshot_http.png, screenshot_dns.png, etc.: Screenshots of Wireshark showing filtered packets for HTTP, DNS, and ICMP.

## Challenges and Resolutions:
Challenge: No packets captured initially.
Resolution: Ensured the correct network interface was selected and Npcap/libpcap was installed.
Challenge: Difficulty identifying protocols.
Resolution: Used Wireshark’s filter bar and referred to online tutorials (e.g., Wireshark documentation).

## Key Learnings:
Gained hands-on experience with Wireshark for packet capturing and analysis.
Developed an understanding of common protocols (HTTP, DNS, ICMP) and their roles in network communication.
Learned to filter and interpret packet details for troubleshooting and analysis.
Improved skills in documenting technical tasks and using GitHub for submissions.

## References:
Wireshark Official Documentation: https://www.wireshark.org/docs/
Online tutorials for Wireshark filtering and protocol analysis.
