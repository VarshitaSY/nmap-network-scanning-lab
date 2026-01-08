# Nmap Scan Analysis & Findings

## 🔓 Open Ports Identified
- 22/tcp – SSH (Secure Shell)
- 80/tcp – HTTP (Web Server)
- 9929/tcp – Nping Echo
- 31337/tcp – Elite (Back Orifice – historical significance)

## 🧠 Observations
- The target host exposes multiple open ports accessible from the internet.
- SSH and HTTP services indicate remote access and web hosting functionality.
- Port 31337 is commonly associated with backdoor services, though in this case it is part of the test environment.
- OS detection suggests the host is running a Linux-based operating system with high confidence.

## ⚠️ Potential Security Considerations
- Open SSH ports can be targeted by brute-force attacks if not properly secured.
- Web services must be kept updated to avoid known vulnerabilities.
- Exposed services increase the attack surface of the system.

## 📘 Learning Outcome
This project helped me understand how network scanning reveals exposed services and how attackers and defenders assess network security posture using Nmap.

## Port Scan Findings
Full port scans (`-p-`) may be rate-limited or blocked on public servers such as scanme.nmap.org. Therefore, a top-ports scan was used to efficiently identify commonly exposed services.
Command used:
nmap --top-ports 1000 -Pn scanme.nmap.org
