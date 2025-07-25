🛡️ Cybersecurity Notes – Day 3
🗓️ Topics: Git Basics, Malware Analysis, Linux Commands
📁 Introduction to Git & Cloning
Git is a version control system that enables developers to track changes in code and collaborate efficiently on projects.

🔧 Cloning a Repository
To copy a remote repository (e.g., from GitHub) to your local system:

bash
Copy
Edit
git clone <repository-URL>
This command creates a local copy of the remote repository, allowing you to work offline.

🦠 Types of Malware Analysis
1️⃣ Static Analysis
Involves examining a file without executing it

Common focus areas:

File type (e.g., .exe, .apk)

Metadata

Embedded strings

Code structure (using disassemblers)

Considered safe, as the malware is not actively running

2️⃣ Dynamic (Runtime) Analysis
Executes the file in a controlled environment

Observes behavior such as:

File and system modifications

Network communication

Resource consumption

Requires careful isolation to avoid spreading threats

🏝️ Sandbox Environment
A sandbox is a secure, isolated virtual environment used for dynamic malware analysis. It allows analysts to safely execute suspicious files (like .exe or .apk) without risking the main system.

⚙️ ATS (Advanced Threat Simulation) Software
ATS tools are designed to:

Identify complex and evasive threats

Simulate real-world attack scenarios

Monitor and evaluate malware behavior

Primarily used in enterprise-grade security setups for advanced threat detection.

🐧 Essential Linux Commands for Cybersecurity
📂 File & Directory Operations
Command	Description
ls	List directory contents
cd	Change directory
pwd	Show current directory path
mkdir	Create a new directory
rmdir	Delete an empty directory
cp	Copy files or directories
mv	Move or rename files/directories
man	View manual for any command
echo	Display a line of text
chmod	Modify file permissions
clear	Clear the terminal screen

🔸 Note: Linux is case-sensitive (File.txt ≠ file.txt)

📜 Creating and Managing Files
To create an empty file:

bash
Copy
Edit
touch hacker.txt
View file details with:

bash
Copy
Edit
ls -lh
-l: Displays long listing format (includes permissions, owners, timestamps)

-h: Shows file sizes in a human-readable format (e.g., KB, MB)

🔐 File Permission Overview
Every file in Linux has permissions for three categories:

Owner (file creator)

Group (users in the same group)

Others (all other users)

🔧 Changing Permissions
Use the chmod command:

bash
Copy
Edit
chmod 755 hacker.txt
This assigns:

Owner: Read, Write, Execute

Group: Read, Execute

Others: Read, Execute

