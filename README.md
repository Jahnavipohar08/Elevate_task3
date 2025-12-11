🔒 Basic Vulnerability Assessment Report – README
📌 Project Overview

This repository contains a Basic Vulnerability Assessment performed on the target host 10.153.242.222.
The assessment focuses on identifying exposed services, misconfigurations, insecure network behaviors, and potential attack surfaces using scan outputs and manual analysis.

The goal of this project is to demonstrate the ability to:

Analyze raw vulnerability scan data

Identify high-risk and medium-risk exposures

Document vulnerabilities professionally

Provide mitigation recommendations

Generate a formal security report (PDF)

📁 Contents of This Repository
📂 Vulnerability-Assessment/
│── 📄 vulnerability_report.pdf        # Final professional PDF report
│── 📄 README.md                       # Project documentation
│── 📁 scan-files/                     # Raw scan output files (Nessus-style logs)
│── 📄 analysis_notes.txt              # Additional observation notes (if applicable)

🛑 Key Findings (Summary)

The analysis revealed the following major vulnerabilities:

1. SMB Service Exposure (Ports 445 & 139)

High-risk, commonly exploited in ransomware attacks

NTLM domain information exposed

2. Multiple DCE-RPC Services Running (Ports 49664–49691)

Creates a large attack surface

Can enable remote enumeration or exploitation

3. Unresponsive / Misconfigured Web Services

Port 80/443 inconsistencies

Possible abandoned or broken services

4. SSL Certificate Chain Issues on Port 8834

Broken CA chain

Clients cannot validate authenticity

5. SNMP Default Community String (“public”)

Highly insecure

Leaks internal system information

6. Excessive Open & Listening Ports

Increases exposure

May indicate unnecessary services running

📊 Overall Risk Rating
Category	Rating
SMB Exposure	🔴 High
RPC Surface	🟠 Medium
SSL Issues	🟠 Medium
SNMP Weakness	🔴 High
Overall System Security	🟠 Medium–High
🛠 Recommendations

To reduce the attack surface and improve security posture:

Disable SMBv1, restrict SMB service access

Limit RPC communication and close unused ports

Fix SSL certificate chain configuration

Remove or secure SNMP using SNMPv3

Disable unresponsive HTTP/HTTPS services

Follow the principle of least privilege for network services

📄 Report

The full professional vulnerability assessment report is available in PDF format:

👉 vulnerability_report.pdf

It includes:

Detailed findings

Evidence citations

Screenshots (if added)

Technical explanations

Prioritized remediation guidelines

👩‍💻 Tools & Technologies Used

Nmap / Nessus-style scan output

Python (PDF generation)

VS Code for code and report creation

Security analysis methodologies (CVE/CWE best practices)

🙋 Author

Jahanavi Pohar
Cybersecurity Intern | Vulnerability Assessment & Analysis
