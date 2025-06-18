# TASK-1 Basic Network Sniffer

# Re-create README.md file after kernel reset

readme_content = """# 🕵️‍♂️ Network Packet Sniffer with Scapy (Windows)

This Python-based network sniffer captures and analyzes live network traffic using the Scapy library. It helps you understand how data flows through a network by printing essential information like IP addresses, protocols, ports, and packet payloads.

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
   ```bash
   pip install scapy
