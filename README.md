# Dynamic-ARP-Inspection-Module

## Overview
This repository contains the implementation for **Dynamic ARP Inspection (DAI)**. The project focuses on monitoring network flows at the link layer to detect abnormalities in ARP (Address Resolution Protocol) request-response patterns, such as ARP spoofing and other malicious activities. 

## ARP Overview
The **Address Resolution Protocol (ARP)** bridges the network and link layers, allowing hosts to map IP addresses to MAC addresses on a local network. However, ARP is vulnerable to spoofing, where an attacker sends malicious ARP packets to mislead hosts about the correct MAC addresses associated with IP addresses. This can lead to man-in-the-middle (MITM) attacks, packet interception, and other malicious activities.

## Implementation Details
### Technologies Used:
- **libpcap**: For packet capture and analysis.
- **C Programming**: The implementation is written in C for low-level network packet processing.
- **Scapy**: Used for generating test ARP packets and pcap files for testing.

### Key Features:
- **ARP Packet Parsing**: Parsing ARP packets to extract source/destination IPs and MAC addresses.
- **Dynamic ARP Inspection**: Detecting abnormal ARP packets based on predefined valid mappings.
- **Alert Mechanism**: Logging errors and notices when abnormal ARP traffic is detected.
- **Database for ARP Mappings**: Storing IP-MAC bindings to compare and detect violations.

## Configuration
The DAI module uses a configuration file for specifying valid IP-MAC bindings, including high-availability setups where multiple MAC addresses may be associated with a single IP address. The configuration allows flexible monitoring and detection of abnormal ARP behavior.

## Conclusion
The **Dynamic ARP Inspection (DAI)** module is an essential part of an Intrusion Prevention System (IPS) aimed at preventing ARP spoofing attacks. By analyzing ARP traffic and detecting abnormal behavior, it helps safeguard network integrity and security.

