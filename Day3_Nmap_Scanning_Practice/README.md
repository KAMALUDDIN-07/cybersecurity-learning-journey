 🔍 Day 3 – Nmap Scanning Practice (Metasploitable2)

 ✅ Target: <Your Metasploitable IP>  
 💻 Attacker: Kali Linux  
 🛠️ Tool Used: Nmap  

 🔹 1. Ping Scan – Check if Host is Alive
nmap -sn <Your Metasploitable IP>
📝 Result: Host is up

🔹 2. SYN Scan – Find Open Ports
nmap -sS <Your Metasploitable IP>
📝 Result:
Open Ports:
21/tcp – FTP
22/tcp – SSH
23/tcp – Telnet
80/tcp – HTTP
(Your output may show more)

🔹 3. Service Version Detection
nmap -sV <Your Metasploitable IP>
📝 Result:
FTP: vsftpd 2.3.4
SSH: OpenSSH 4.7p1
HTTP: Apache httpd 2.2.8

🔹 4. Aggressive Scan – Full Info
nmap -A <Your Metasploitable IP>
📝 Result:
OS Guess: Linux
Detected Services + Versions
Script Results (like HTTP titles, FTP info)

📁 Output Files (saved in Kali)
nmap -sS -oN syn-scan.txt <Your Metasploitable IP>
nmap -sV -oN version-scan.txt <Your Metasploitable IP>
nmap -A  -oN aggressive-scan.txt <Your Metasploitable IP>

📚 What I Learned Today:
How to scan with Nmap
Difference between Ping, SYN, Version, Aggressive scans
Saved outputs for report writing
