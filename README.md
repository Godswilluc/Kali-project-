# Kali-project-
The process of setting up kali.

# Virtual Cybersecurity Lab Setup
This project sets up a virtual environment to simulate offensive and defensive cybersecurity tasks using Kali Linux (attacker) and Windows 10 (target) in an isolated network.
##  Features
- Type 2 Hypervisor: Oracle VirtualBox
- Virtual Machines:
&nbsp; - Kali Linux (Attacker)
&nbsp; - Windows 10 (Target)
\- Internal virtual network (no internet)
\- Verified connectivity using ping, shared folder access, and service scans
\## 📁 Folder Structure
\- steps.txt: Step-by-step lab setup
\- Virtual screenshots/: Images of VM config and testing
\## 👤 Author
Godswill uc
DSA Project
‎VIRTUAL LAB SET/Steps.txt
+58
Lines changed: 58 additions & 0 deletions
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,58 @@
Virtual Cybersecurity Lab Setup
===============================
Objective:
----------
To simulate a secure, real-world environment for offensive and defensive testing using Kali Linux and Windows 10 virtual machines.
Tools Used:
-----------
- VirtualBox (Type 2 hypervisor)
- Kali Linux ISO
- Windows 10 ISO 
Steps:
------
1. *Installed VirtualBox* on host system (Windows/Linux)
2. *Created and configured Kali VM:*
   - OS: Kali Linux (latest)
   - RAM: 2 GB
   - Storage: 20 GB dynamically allocated
   - Network: Internal Network (named "LabNet")
3. *Created and configured Windows 10 VM:*
   - OS: Windows 10 Pro or Home
   - RAM: 2 GB
   - Storage: 20 GB dynamically allocated
   - Network: Internal Network (same name as Kali)
4. *Verified network isolation:*
   - No internet access
   - Both VMs connected only to each other
5. *Set static IPs:*
   - Kali: 192.168.1.101
   - Windows: 192.168.56.103
   - Subnet mask: 255.255.222.2
6. *Ping Test:*
   - Successfully pinged Windows from Kali
   - Successfully pinged Kali from Windows
7. *Tested Shared Folder Access:*
   - Enabled guest additions on Kali
   - Created shared folder to exchange files (optional)
8. *Service Enumeration (Optional):*
   - From Kali, used nmap 192.168.56.1 to scan Windows open ports
Result:
--------
A fully isolated and connected cybersecurity test lab ready for penetration testing and malware simulation.
Author:Godswill uc

ANDROID FORENSIC READ ME
ANDRIOD FORENSICS/README.md
+40
Lines changed: 40 additions & 0 deletions


Original file line number	Diff line number	Diff line change
@@ -0,0 +1,40 @@
\# Android Forensics Analysis
This project involves analyzing a mock Android forensic image using Autopsy to extract digital evidence such as call logs, SMS messages, application usage, and deleted content.
\## 🔍 Objectives
\- Analyze Android image with Autopsy
\- Extract key evidence: SMS, calls, contacts, app data, images, browser history, and deleted files
\- Create a professional forensic report with screenshots and findings
\## 🧰 Tools Used
\- Autopsy (Digital Forensics Platform)
\- Provided Android image file (.tar.gz and data)
\## 📁 Folder Structure
\- steps.txt: Forensics methodology and investigation process
\- Project screenshots/: Collected evidence and tool outputs
\## 👤 Author
Godswill uc
DSA Project
‎ANDRIOD FORENSICS/Report.pdf
76 KB
Binary file not shown.
‎ANDRIOD FORENSICS/file-report.txt
+6,738
Lines changed: 6738 additions & 0 deletions
Large diffs are not rendered by default.

FIREWALL PROJECT READ ME
FIREWALL PROJECT/README.md
+40
Lines changed: 40 additions & 0 deletions


Original file line number	Diff line number	Diff line change
@@ -0,0 +1,40 @@
\# Virtual Firewall Lab (pfSense)
This lab simulates a basic firewall using pfSense to route and filter traffic between Kali Linux and Windows 10 virtual machines. It includes network configuration, DHCP setup, firewall rules, and logging.
\##  Features
\- pfSense virtual firewall with WAN and LAN interfaces
\- DHCP server enabled on LAN
\- ICMP firewall rule for ping testing
\- Verified routing between Kali ↔ Windows
\- Screenshots are included
\## 📁 Folder Structure
\- steps.txt – Step-by-step setup and explanation
\- firewall screent/ – Images showing GUI, rules, and ping results
\## 👤 Author
Godswill uc
My DSA project
‎FIREWALL PROJECT/Steps.txt
+56
Lines changed: 56 additions & 0 deletions
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,56 @@
Virtual Firewall Lab – pfSense Setup and Testing
Objective:
-----------
To simulate a secure virtual firewall setup using pfSense to route and inspect network traffic between Kali Linux (attacker) and Windows 10 (target).
Tools Used:
------------
- VirtualBox
- pfSense ISO
- Kali Linux VM
- Windows 10 VM
- Firefox
Steps Taken:
-------------
1. *Created a new pfSense VM in VirtualBox*
   - Added two network adapters:
     • Adapter 1 (WAN): Attached to NAT
     • Adapter 2 (LAN): Attached to Internal Network (named "LabNet")
2. *Installed pfSense using default options*
   - Set LAN IP: 192.168.56.1/24
   - Skipped WAN setup in the browser interface
3. *Accessed pfSense GUI from Kali*
   - Assigned Kali IP: 192.168.100.101
   - Opened browser and visited https://192.168.56.103
4. *Enabled DHCP on pfSense LAN interface*
   - Range: 192.168.100.50 – 192.168.100.100
5. *Connected Windows 10 VM to the same Internal Network*
   - Received IP via DHCP: 192.168.100.53
6. *Created a firewall rule in pfSense*
   - Allowed ICMP protocol to enable ping between machines
7. *Tested communication*
   - Kali pinged Windows and pfSense successfully
   - Windows pinged pfSense and Kali successfully
8. *Monitored logs*
   - Went to Status > System Logs > Firewall
   - Verified that ping (ICMP) traffic was being logged
Result:
--------
The pfSense firewall successfully controlled and monitored traffic between Kali and Windows, simulating a real-world network security layer.
Author:
--------
Godswill uc
DSA Project
‎VIRTUAL LAB SET/README.md
+40
Lines changed: 40 additions & 0 deletions


Original file line number	Diff line number	Diff line change
@@ -0,0 +1,40 @@
\# Virtual Cybersecurity Lab Setup
This project sets up a virtual environment to simulate offensive and defensive cybersecurity tasks using Kali Linux (attacker) and Windows 10 (target) in an isolated network.
\##  Features
\- Type 2 Hypervisor: Oracle VirtualBox
\- Virtual Machines:
&nbsp; - Kali Linux (Attacker)
&nbsp; - Windows 10 (Target)
\- Internal virtual network (no internet)
\- Verified connectivity using ping, shared folder access, and service scans
\## 📁 Folder Structure
\- steps.txt: Step-by-step lab setup
\- Virtual screenshots/: Images of VM config and testing
\## 👤 Author
Godswill uc
DSA Project
‎VIRTUAL LAB SET/Steps.txt
+58
Lines changed: 58 additions & 0 deletions
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,58 @@
Virtual Cybersecurity Lab Setup
===============================
Objective:
----------
To simulate a secure, real-world environment for offensive and defensive testing using Kali Linux and Windows 10 virtual machines.
Tools Used:
-----------
- VirtualBox (Type 2 hypervisor)
- Kali Linux ISO
- Windows 10 ISO 
Steps:
------
1. *Installed VirtualBox* on host system (Windows/Linux)
2. *Created and configured Kali VM:*
   - OS: Kali Linux (latest)
   - RAM: 2 GB
   - Storage: 20 GB dynamically allocated
   - Network: Internal Network (named "LabNet")
3. *Created and configured Windows 10 VM:*
   - OS: Windows 10 Pro or Home
   - RAM: 2 GB
   - Storage: 20 GB dynamically allocated
   - Network: Internal Network (same name as Kali)
4. *Verified network isolation:*
   - No internet access
   - Both VMs connected only to each other
5. *Set static IPs:*
   - Kali: 192.168.56.101
   - Windows: 192.168.56.103
   - Subnet mask: 255.255.222.2
6. *Ping Test:*
   - Successfully pinged Windows from Kali
   - Successfully pinged Kali from Windows
7. *Tested Shared Folder Access:*
   - Enabled guest additions on Kali
   - Created shared folder to exchange files (optional)
8. *Service Enumeration (Optional):*
   - From Kali, used nmap 192.168.56.103 to scan Windows open ports
Result:
--------
A fully isolated and connected cybersecurity test lab ready for penetration testing and malware simulation.
Author:
--------
Godswill uc
DSA Project
