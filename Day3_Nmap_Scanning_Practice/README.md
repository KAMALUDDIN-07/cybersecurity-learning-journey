Day 3 – Nmap Scanning Practice (Target: Metasploitable2) 🔍

  ✅ Lab Setup
- 🖥️ **Attacker Machine**: Kali Linux  
- 🧪 **Target Machine**: Metasploitable2  
- 🛠️ **Tool Used**: Nmap

---

### 🔹 1. 🔍 Ping Scan – Check if Host is Alive

nmap -sn 192.168.172.129

📝 Result: Host is up

🔹 2. 🔓 SYN Scan – Discover Open Ports

nmap -sS 192.168.172.129

📝 Result:

Open Ports:
21/tcp – FTP  

22/tcp – SSH  

23/tcp – Telnet  

80/tcp – HTTP  

... (more may appear)

🔹 3. 🔎 Service Version Detection

nmap -sV 192.168.172.129

📝 Result:

FTP: vsftpd 2.3.4  

SSH: OpenSSH 4.7p1 
 
HTTP: Apache httpd 2.2.8

🔹 4. 🧠 Aggressive Scan – Deep Enumeration

nmap -A 192.168.172.129

📝 Result:

OS Detection: Linux (guess)

Services + Version info

Script results (e.g., HTTP title, FTP banner)

📁 Output Saved (in Kali)

nmap -sS -oN syn-scan.txt  192.168.172.129

nmap -sV -oN version-scan.txt  192.168.172.129

nmap -A -oN aggressive-scan.txt  192.168.172.129

📚 What I Learned Today

How to scan a host with different Nmap options

Difference between -sn, -sS, -sV, and -A scans

Saved output files for future documentation and reporting

“Enumeration is where hacking begins. Nmap is the first step to understanding your target.”
