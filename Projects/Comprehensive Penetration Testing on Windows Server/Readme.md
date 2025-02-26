# Comprehensive Penetration Testing on Windows Server

## 📌 Project Overview
This project involved conducting a **penetration test on a Windows Server 2019 system** to identify security vulnerabilities and exploit misconfigurations. The test simulated an attack using **Kali Linux** to assess system weaknesses and propose mitigation strategies.

## 👨‍💻 Role & Responsibilities
As the **team lead**, I managed the penetration testing process, including reconnaissance, exploitation, and reporting. I ensured that vulnerabilities were documented and mitigation strategies were clearly outlined for improving the system’s security posture.

## 🛠 Tools & Technologies
- **Penetration Testing Tools:** Kali Linux, Nmap, Nikto, Metasploit, Enum4linux, Smbclient, WhatWeb
- **Target System:** Windows Server 2019
- **Exploitation Methods:** FTP Misconfiguration, Weak Credentials, Privilege Escalation
- **Security Frameworks:** OWASP Secure Configuration Guidelines

## 🔍 Key Findings
### 1. FTP Misconfiguration
- **Issue:** Anonymous login was enabled, exposing sensitive files.
- **Exploit:** Gained access to system files using anonymous FTP login.
- **Mitigation:** Disable anonymous FTP access and use **FTPS/SFTP**.

### 2. Weak Credentials
- **Issue:** Password hints stored in plaintext allowed attackers to guess passwords.
- **Exploit:** Used password hints to log into a user account with administrative privileges.
- **Mitigation:** Implement **strong password policies** and avoid storing plaintext hints.

### 3. Improper Access Control
- **Issue:** A compromised user account was part of the Administrators group.
- **Exploit:** Escalated privileges to reset the **Administrator password**.
- **Mitigation:** Restrict administrative privileges and perform regular access audits.

## 🛠 Exploitation Process
1. **Scanning:** Used **Nmap** to identify open ports (FTP, HTTP, SMB, RDP).  
2. **FTP Exploitation:** Logged in as **anonymous**, accessed restricted files.  
3. **Credential Discovery:** Extracted a password hint (**coffee1**) leading to **espresso** user account.  
4. **Privilege Escalation:** The **espresso** account was part of the Administrators group, allowing execution of:  
   ```bash
   net user Administrator admin123  # Reset Administrator password
   ```
5. **Full System Access:** Gained complete control over the system.

## 🔐 Mitigation Strategies
- **Disable Anonymous FTP Login** – Use secure file transfer protocols like **FTPS/SFTP**.
- **Enforce Strong Password Policies** – Implement **complex passwords** and avoid plaintext hints.
- **Limit Administrative Privileges** – Grant admin access only where necessary.
- **Enable Logging & Monitoring** – Track login attempts and detect unauthorized access.
- **Patch Vulnerabilities** – Apply security updates and follow **secure configuration guidelines**.

## 📊 Results & Impact
- **Identified and exploited critical vulnerabilities** in Windows Server 2019.
- **Provided security recommendations** to strengthen access control.
- **Demonstrated risk mitigation strategies** to prevent privilege escalation attacks.

## 🔗 References
- **Tools Used:** Kali Linux, Nmap, Nikto, Metasploit, Enum4linux, Smbclient, WhatWeb
- **Security Frameworks:** OWASP Secure Configuration Guidelines

## 📬 Contact
- **LinkedIn:** [linkedin.com/in/saravanan-vijayamurugan](https://linkedin.com/in/saravanan-vijayamurugan)
- **Email:** saravanan.vijayamurugan@outlook.com

> *This penetration test highlights the importance of securing misconfigured services and enforcing strong access controls.* 🚀
