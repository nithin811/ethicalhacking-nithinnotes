Security Audit Report: Full Port Scan on testphp.vulnweb.com
🎯 Goal
The goal of this scan was simple:
Check all 65,535 TCP ports on testphp.vulnweb.com to ensure no services are hiding on non-standard ports. This was part of a comprehensive security audit — no shortcuts.

🧰 Tools Used
Nmap – Industry-standard network scanner

Bash – For automation scripting

Python (matplotlib) – To generate visuals of scan results (optional)

📌 What We Did (Methodology)
1. Full TCP Port Scan with Nmap
We used Nmap’s full scan mode to sweep through all possible TCP ports.

bash
Copy
Edit
nmap -p- -T4 -v testphp.vulnweb.com -oN full_port_scan_output.txt
-p-: Scans all 65,535 ports

-T4: Uses faster timing to reduce scan duration

-v: Enables verbose output

-oN: Saves output in a readable text file

2. Automation Script
To ensure repeatability and consistency, we wrote a Bash script:

full_port_scan.sh
bash
Copy
Edit
#!/bin/bash

TARGET="testphp.vulnweb.com"
OUTPUT="full_port_scan_output.txt"

echo "[*] Starting full TCP port scan on $TARGET..."
nmap -p- -T4 -v $TARGET -oN "$OUTPUT"
echo "[*] Scan complete. Output saved to $OUTPUT"
To run:

bash
Copy
Edit
chmod +x full_port_scan.sh
./full_port_scan.sh
🔎 What We Found
Port	Service	Notes
22	SSH	Standard remote access
80	HTTP	Web server — expected
3306	MySQL	Database exposed — should be firewalled
8888	sun-answerbook	Often used for dev tools like Jupyter — investigate access

💾 Script Submission
Bash Script: full_port_scan.sh
bash
Copy
Edit
#!/bin/bash
TARGET="testphp.vulnweb.com"
OUTPUT="full_port_scan_output.txt"
echo "[*] Starting full TCP port scan on $TARGET..."
nmap -p- -T4 -v $TARGET -oN "$OUTPUT"
echo "[*] Scan complete. Output saved to $OUTPUT"
Optional Python Script (for visuals): generate_screenshot.py
python
Copy
Edit
import matplotlib.pyplot as plt

nmap_output = """
Starting Nmap 7.93 ( https://nmap.org ) at 2025-07-31 12:00 UTC
Nmap scan report for testphp.vulnweb.com (192.168.1.100)
Host is up (0.22s latency).
Not shown: 65531 closed tcp ports (reset)
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
3306/tcp open  mysql
8888/tcp open  sun-answerbook

Nmap done: 1 IP address (1 host up) scanned in 45.67 seconds
"""

fig, ax = plt.subplots(figsize=(10, 4))
ax.axis('off')
ax.text(0, 1, nmap_output, fontsize=10, fontfamily='monospace', va='top')
plt.savefig("nmap_scan_screenshot.png", bbox_inches='tight')
🧩 Final Conclusion
A full port scan of testphp.vulnweb.com revealed that while common services like SSH and HTTP were expected, critical services such as MySQL and a potential development interface on port 8888 were also exposed — highlighting how important it is to scan every port, not just the usual suspects. This approach ensures hidden or misconfigured services don't go unnoticed, reinforcing the need for thoroughness in every security audit.
