🔒 Vulnerability Assessment using Nessus Essentials


📌 Project Summary

This project involves performing a full vulnerability assessment on a local Windows machine using Tenable Nessus Essentials. It includes installation, target setup, scanning, result analysis, and documentation of key vulnerabilities found. The results are recorded for educational and auditing purposes.


🔒 Important Notes that i considered Before Scanning:

To make the scan work effectively on a Windows machine (especially your own):


Run Nessus as Administrator

Make sure Nessus is running with admin privileges.

Enable File and Printer Sharing

Control Panel → Network and Sharing Center → Change advanced sharing settings → Turn on File and Printer Sharing.

Enable Remote Registry Service

Open services.msc → Find Remote Registry → Set to Automatic and Start it.

Temporarily disable Windows Defender Firewall (optional for test purposes)

Or configure it to allow incoming connections for common scan ports.



🧰 Tools Used

Nessus Essentials (by Tenable)

Windows 11 (local machine)

Command Prompt (for IP discovery)



✅ Steps Performed

1. Installed Nessus Essentials

Downloaded Nessus Essentials from tenable.com.

Registered with email to get an activation code.

Completed installation and activated the product.



2. Identified Local Machine IP Address

Used the following command to get IP address:

ipconfig

Selected the Wi-Fi adapter IP: 192.168.127.40



3. Launched Nessus and Created a New Scan

Opened browser as Administrator.

Accessed Nessus on: https://localhost:8834

Created a Basic Network Scan.

Set the target as: 192.168.127.40

Did not provide credentials (non-authenticated scan).



4. Ran the Scan

Start time: 7:43 PM

Completed around: 8:33 PM

Duration: ~50 minutes



5. Scan Results Summary

Total Vulnerabilities Found: 53

Severity Breakdown:

Critical: 1

High: 1

Medium: 6

Info: 45



6. 🔍 Key Vulnerabilities Found

🔴 1. Oracle Database Unsupported Version

Plugin ID: 55786

Severity: Critical (CVSS v3.0 = 10.0)

Impact: Unpatched software is exploitable

Fix: Upgrade to a supported Oracle DB version

🔴 2. Oracle TNS Listener Remote Poisoning

Plugin ID: 69552

Severity: High (CVSS v3.0 = 7.3)

Impact: Remote attackers can redirect DB traffic

Fix: Apply latest Oracle patches and restrict listener access

🟠 3. SSL Certificate Issues

Self-signed, untrusted, and expired certificates found

Plugins: 51192, 57582, 15901

Fix: Replace with valid SSL certificates issued by a trusted CA

🟠 4. SMB Signing Not Required

Plugin ID: 57608

Impact: Susceptible to man-in-the-middle attacks

Fix: Enable SMB signing via group policy

🛠️ Simple Mitigations Suggested

Upgrade legacy Oracle components

Use trusted, updated SSL certificates

Enable SMB signing

Implement HSTS for web servers



🖼️ Screenshots Included

Nessus Dashboard

Target IP Scan Results

Vulnerability Summary

Critical & High Details


✅ Conclusion

This project demonstrated a complete vulnerability scan using Nessus Essentials on a Windows machine. It identified multiple issues including critical Oracle DB exposure and certificate weaknesses. The exercise reinforced key cybersecurity concepts including threat detection, prioritization, and mitigation.

📌 Author

Saswat Kumar Cybersecurity StudentGitHub: Swaggyop

Feel free to fork, clone, or suggest improvements!

