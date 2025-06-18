# TASK-1 Basic Network Sniffer


##  Features

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
 Install Npcap in WinPcap API-compatible Mode

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
#
#




# TASK-2 Phishing Awareness Training

##  Task Objective

Create a presentation or online module that:

- Explains _what phishing is_ and _why it matters_
- Teaches how to _recognize phishing emails and fake websites_
- Covers _social engineering tactics_ used by attackers
- Shares _best practices_ to avoid falling victim
- Includes _real-world examples_
- Provides an _interactive quiz_ for engagement

##  Project Contents

-  Phishing-Awareness-Training-Dont-Get-Hooked.pptx – Main presentation file
-  README.md – Project documentation
-  (Optional) quiz_questions.md – List of interactive quiz questions (can be added later)

##  Key Topics Covered

- _Phishing Attacks Overview_
- _How to Spot Phishing Emails_
- _How to Identify Fake Websites_
- _Social Engineering Techniques_ (Pretexting, Baiting, Fear-Mongering)
- _Best Practices to Stay Safe_
- _Real Phishing Scenarios_ (Bank and Amazon scams)
- _Interactive Quiz_

##  Learning Outcomes

By going through this presentation, users will:

- Understand how phishing works
- Identify red flags in suspicious communications
- Learn actionable tips to enhance personal and organizational cybersecurity

##  How to Use

1. Open the PowerPoint file to view the training slides.
2. Review each section carefully and participate in the quiz at the end.
3. Share this with teammates or friends to spread awareness.
#
#




# TASk-3  Secure Coding Review

##  Task Objective

Conduct a **secure coding review** that includes:
- Identifying common coding vulnerabilities
- Using tools like **static analyzers** (e.g., Bandit)
- Recommending industry best practices for secure coding
- Providing a detailed report with **findings and remediation**
- Creating a mock project that demonstrates security issues

##  Project Structure



secure-coding-review/
│
├── vulnerable\_app.py              # Mock Python script with security issues
├── Secure\_Coding\_Review\_Report.docx  # Detailed review report with findings
├── secure\_app.py (optional)       # Improved version of the code (if added)
└── README.md                      # Project documentation



##   Vulnerabilities Demonstrated

-  Use of `eval()` (code injection risk)
-  SQL injection using raw string queries
-  Hardcoded credentials (poor secret management)
-  Lack of input validation (type safety issues)

##  Tools Used

-  **Bandit**: Python static code analyzer  
-  Manual code inspection  
-  `pip-audit` (for dependency security, optional)

##  Sample Fixes Implemented

- Replacing `eval()` with safe alternatives (e.g., `f-string`)
- Using parameterized SQL queries to prevent injection
- Moving credentials to environment variables
- Adding input validation for user inputs

##  Learning Outcomes

- Understand how to detect insecure code patterns
- Use security auditing tools to analyze code
- Apply secure coding principles in real-world scenarios
