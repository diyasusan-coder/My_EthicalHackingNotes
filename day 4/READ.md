🛡️ Cybersecurity Notes – Day 4

🗓️ Topics: Networking Basics, IP Concepts, Attack Timeline, Recon, Kali Linux Post-Boot, Breach Checking, and Nmap Flags

🌐 Networking Basics

🔹 What is a Network?
A network is a group of devices connected together to exchange data and resources.

🔹 Subnet
A subnet is a smaller division within a larger network, used to improve performance, security, and organization.

🔄 TCP vs UDP

Feature	TCP	UDP
Type	Connection-oriented	Connectionless
Reliability	Reliable (ensures delivery)	Unreliable (no guarantee)
Speed	Slower (more overhead)	Faster (low latency)
Use Cases	Web, file transfer (HTTP, FTP)	Streaming, gaming, VoIP

🧭 IP Addressing Concepts

🔹 What is an IP Address?
A unique identifier for each device on a network.

🔹 Static vs Dynamic IP

Static IP: Manually assigned, fixed

Dynamic IP: Automatically assigned by DHCP, can change

🔹 IPv4 vs IPv6

IPv4	IPv6
32-bit (e.g., 192.168.1.1)	128-bit (e.g., 2001:0db8::1)
~4.3 billion addresses	Virtually unlimited addresses
Widely used	Increasing adoption

⚔️ Attack Timeline – Phishing Scenario

🕵️‍♂️ Adversary Action:

Sends phishing email with a malicious attachment

🧑‍💻 Employee/Victim Workflow:

Views email content

Downloads ZIP attachment

Extracts ZIP file

Runs malicious script (e.g., PowerShell)

🛠️ Technical Elements:

Attachment: Often disguised malware

ZIP File: Used to evade filters

PowerShell: Executes scripts

UAC (User Account Control): May ask for elevated permissions

🔍 Reconnaissance (Information Gathering)

Reconnaissance is the first stage of an attack to gather information.

🔸 Types:

Passive Recon: No direct contact (e.g., WHOIS, Google, DNS records)

Active Recon: Direct probing (e.g., ping, Nmap scans)

🐧 First Things to Do After Booting Kali Linux

✅ Update system:

bash

sudo apt update && sudo apt upgrade
🔐 Set root/user password if needed

⚙️ Check key tools (e.g., nmap, burpsuite)

🌐 Ensure internet connection via NAT/Bridged mode

📦 Install any missing tools:

bash

sudo apt install <toolname>
🔍 View IP address and hostname:

bash
ip a && hostnamectl
🧰 Set up working directories for projects, payloads, etc.

🌐 Have I Been Pwned
Website: https://haveibeenpwned.com

Free tool to check if your email or password has been exposed in a known data breach

Helps users stay aware and take action if credentials are compromised

📡 Nmap Command Flags Explained

If you see a complex string like:

css

-Pn -A -sV -O -oN --script -vv -p -sS -sT
Here’s what each part means:

Flag	Description
-Pn	Treat all hosts as online (skip ping)
-A	Aggressive scan (OS detection, version, scripts, traceroute)
-sV	Detect service versions on open ports
-O	Attempt to identify the operating system
-oN	Save output in normal text format (must specify filename, e.g., -oN scan.txt)
--script	Run specific NSE scripts (e.g., --script default, --script vuln)
-vv	Very verbose output
-p	Specify port(s) (e.g., -p 80,443 or -p- for all ports)
-sS	SYN (stealth) scan
-sT	TCP connect scan (used without root privileges)

⚠️ Note:

-sS and -sT should not be used together — choose one.

-oN and --script must be followed by a filename or script name.

Combine wisely for a working command.

✅ Example of proper usage:

nmap -Pn -A -sV -O -p 80,443 -oN scan.txt --script default -vv

ad
🔧 Why Subnetting Is Useful:
Reduces network congestion by limiting broadcast traffic

Enhances security by isolating network segments

Improves performance by keeping traffic local

Allows better IP address management in large networks

📏 Subnet Mask
A subnet mask determines which part of an IP address refers to the network and which part refers to the host.

🔸 Example:
IP Address: 192.168.1.10
Subnet Mask: 255.255.255.0

Network portion: 192.168.1

Host portion: .10

🧮 CIDR Notation
Classless Inter-Domain Routing (CIDR) is a shorthand for subnet masks.

Example: 192.168.1.0/24

/24 means the first 24 bits are for the network, remaining 8 bits for hosts

📊 Common Subnet Sizes:
CIDR	Subnet Mask	Hosts per Subnet
/30	255.255.255.252	2 usable
/29	255.255.255.248	6 usable
/24	255.255.255.0	254 usable
/16	255.255.0.0	65,534 usable
/8	255.0.0.0	16,777,214 usable

