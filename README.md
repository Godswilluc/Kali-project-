# Kali-project-
The process of setting up kali.

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
