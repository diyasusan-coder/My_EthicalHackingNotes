🛡️ Cybersecurity Notes – Day 2
🗓 Topic: Kali Linux Setup on VirtualBox + Tool Overview
⚙️ 1. Setting Up Kali Linux in VirtualBox
🔧 Requirements
VirtualBox (installed)

Kali Linux ISO/OVA (download from: https://www.kali.org)

🖥️ Steps to Set Up
Launch VirtualBox

Click New to create a virtual machine.

VM Configuration

Name: Kali Linux

Type: Linux

Version: Debian (64-bit)

Memory Setup

Allocate at least 2 GB (2048 MB) RAM for smooth performance.

Create Virtual Hard Disk

Choose “Create a virtual hard disk now”

Recommended size: 20 GB or more

Type: Dynamically allocated

Mount Kali ISO

Go to Settings → Storage

Click the empty disk icon → Choose a disk file → Select Kali ISO

Start Kali VM

Click Start

Choose either Graphical Install or Live Boot

(Optional) Full Installation

Proceed through installation prompts if you want a full install.

Set up a username and password when prompted.

🧪 2. Overview of Kali Linux Tools
🔍 Tool Categories & Examples
Category	Sample Tools	Purpose
Information Gathering	nmap, whois, dnsenum	Collect target system/network details
Vulnerability Scanning	nikto, OpenVAS	Identify known vulnerabilities
Web App Testing	Burp Suite, OWASP ZAP	Inspect and modify web traffic
Exploitation Tools	Metasploit, msfvenom	Launch attacks on vulnerable systems
Password Cracking	Hydra, John the Ripper	Brute-force login/password credentials
Wireless Attacks	aircrack-ng, reaver	Test wireless network security

📝 Key Takeaways
Kali Linux was successfully launched within VirtualBox.

Core tool categories were introduced and demonstrated.

Hands-on exposure to basic scanning and attack simulations.

✅ Next Steps
Practice using terminal-based tools and experiment with GUI utilities (e.g., Burp Suite, Zenmap).

Build and test within isolated or legally sanctioned lab environments.

💡 Tip: Always conduct ethical hacking practices in secure, controlled environments such as virtual labs or private networks.

