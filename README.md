# TASK-1 Basic Network Sniffer


## 📌 Features

- Captures live network traffic
- Extracts and displays:
  - Timestamp
  - Source and Destination IP addresses
  - Protocols: TCP, UDP, ICMP
  - Port numbers
  - First 50 bytes of payload data
- Runs on Windows using Npcap and Python
- CLI-based real-time output

##  Requirements

- Python 3.7 or higher
- Scapy
- Npcap

##  Setup Instructions

1.  Install Python  
   Download from: https://www.python.org/downloads/windows/  
   During installation, enable the option:  
    Add Python to PATH

2.  Install required Python package  
   Open Command Prompt and run:
   pip install scapy

3. Install Npcap
Download from: https://npcap.com/
Enable this option during install:
✅ Install Npcap in WinPcap API-compatible Mode

4.  Run the Script
Open Command Prompt as Administrator
Navigate to the directory containing network_sniffer.py

python network_sniffer.py

Example Output
csharp

Copy
[Time] 2025-06-08 14:35:22
[IP] 192.168.1.100 -> 142.250.191.78
[TCP] 52135 -> 443
[Payload] b'\\x16\\x03\\x01...'
Use Ctrl + C to stop capturing packets.
"""
