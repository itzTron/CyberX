markdown
# 🔒 CyberX (Toolkit)

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)

A robust CLI security suite offering military-grade file protection, activity monitoring, and password management.

![Terminal Demo](demo.gif)

## 🌟 Features

| Feature                | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **AES-256 Encryption** | Secure file/folder encryption with password protection                      |
| **Access Tracking**    | Logs all file operations with timestamps and geolocation (IP-based)         |
| **Integrity Checks**   | Verifies file authenticity using MD5/SHA-256 hashes                         |
| **Password Vault**     | Generates and stores strong passwords with strength analysis                |
| **Cross-Platform**     | Works on Windows, Linux, and macOS                                         |
| **Self-Contained**     | SQLite database stores all security data locally                            |

## 🛠️ Installation

### Prerequisites
- Python 3.8 or later
- [MaxMind GeoLite2 Account](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) (free)

### Step-by-Step Guide

#### Windows (PowerShell)
```powershell
# 1. Clone the repository
git clone https://github.com/yourusername/cyber-defence-toolkit.git
cd cyber-defence-toolkit

# 2. Create virtual environment
python -m venv venv
.\venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download GeoIP database (replace YOUR_LICENSE_KEY)
python scripts/download_geoip.py YOUR_LICENSE_KEY
Linux/macOS (Terminal)
bash
# 1. Clone the repository
git clone https://github.com/yourusername/cyber-defence-toolkit.git
cd cyber-defence-toolkit

# 2. Set up virtual environment
python3 -m venv venv
source venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt
sudo gem install lolcat  # For colorful headers (optional)

# 4. Get GeoIP database
chmod +x scripts/download_geoip.sh
./scripts/download_geoip.sh YOUR_LICENSE_KEY
⚙️ Configuration
Email Setup (for password recovery):

ini
# .env file
SMTP_SERVER=smtp.gmail.com
SMTP_PORT=587
EMAIL=your.email@gmail.com
PASSWORD=your_app_password  # Generate via Google Account > Security
First Run:

bash
python cyber_defence.py
Register a new user account

Set a master password and security hint

🖥️ Usage Guide
Main Menu
text
=== Cyber-Defence Toolkit ===
1. 🔐 File Encryptor
2. 📜 Log Checker
3. ✔️ Integrity Verifier
4. 🔑 Password Manager
5. 🔄 Reset Password
6. ❌ Exit
Common Operations
Encrypting a File
text
1. Select "File Encryptor" → "Encrypt File"
2. Enter path: /home/user/secret.docx
3. Set encryption password
4. Backup created at: /backups/secret.docx.bak
5. Encrypted file: /home/user/secret.docx.enc
Checking Access Logs
text
1. Select "Log Checker" → "View All Logs"
2. Sample Output:
   [2023-08-20 14:30] User: admin | File: secret.docx
   Action: ENCRYPT | IP: 192.168.1.10 | Location: Kolkata, IN
Verifying File Integrity
text
1. Select "Integrity Verifier" → "Check File"
2. Enter path: /downloads/important.zip
3. System compares current hashes with database records
4. Alerts if file has been modified
📂 Project Structure
text
cyber-defence-toolkit/
├── core/                  # Main application modules
│   ├── encryptor.py       # AES-256 implementation
│   ├── logger.py          # Access tracking system
│   └── ...                # Other core components
├── db/                    # Database files
├── backups/               # Encrypted file backups
├── scripts/               # Utility scripts
├── cyber_defence.py       # Main executable
├── requirements.txt       # Dependencies
└── README.md              # This file
🚨 Troubleshooting
Issue	Solution
"ModuleNotFoundError"	Run pip install -r requirements.txt
GeoIP database not found	Re-run download script with valid license
SMTP connection failed	Enable "Less Secure Apps" in email provider
Password recovery not working	Check .env file configuration
🤝 Contributing
Fork the repository

Create a new branch (git checkout -b feature/your-feature)

Commit changes (git commit -m 'Add awesome feature')

Push to branch (git push origin feature/your-feature)

Open a Pull Request

📜 License
This project is licensed under the MIT License - see LICENSE for details.
