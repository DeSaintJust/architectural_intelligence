### Initial Access: Exploit Public-Facing Application (T1190)
Attackers often target public-facing applications on Azure Virtual Machines to gain initial access. By exploiting vulnerabilities in web applications, APIs, or web servers, adversaries can infiltrate the VM. Common vulnerabilities include SQL injection, cross-site scripting (XSS), and remote code execution. Once compromised, attackers may execute malicious code, ultimately gaining control over the VM.

### Execution: Command and Scripting Interpreter (T1059)
Adversaries may use command-line interfaces or scripting environments available on Azure VMs, such as PowerShell or Bash, to execute arbitrary commands. This technique allows attackers to run scripts or binary code to manipulate system configurations, collect data, or deploy additional malicious tools. Successful execution often follows initial access techniques like exploiting vulnerable applications.

### Persistence: Create or Modify System Process (T1543)
To maintain persistence on compromised Azure VMs, adversaries can create or modify system-level processes or services. This can include establishing new services, editing startup scripts, or modifying legitimate services to automatically execute malicious payloads upon system reboot, ensuring their presence even after reboots or user logouts.

### Privilege Escalation: Exploitation for Privilege Escalation (T1068)
Attackers may exploit software vulnerabilities within the VM’s operating system or installed applications to gain elevated privileges. This step permits adversaries to execute privileged commands, install rootkits, or extract sensitive information, thus expanding their control over the VM and facilitating further lateral movement across the network.

### Defense Evasion: Impair Defenses (T1562)
To avoid detection, adversaries may impair or disable security functions within Azure VMs. This can involve disabling antivirus software, tampering with logging mechanisms, or manipulating system configurations to evade intrusion detection/prevention systems. Such actions allow malicious activities to persist undetected for longer periods.

### Credential Access: OS Credential Dumping (T1003)
Credential dumping involves extracting passwords or hashes from memory, the file system, or the registry within an Azure VM. Attackers often leverage tools like Mimikatz to access stored credentials, enabling lateral movement and facilitating further exploitation of additional resources within the same cloud environment.

### Discovery: Cloud Service Discovery (T1580)
Once inside a VM, adversaries may perform reconnaissance to gather information about the cloud environment. They may query Azure-specific services, configurations, or metadata available with the VM. Understanding the cloud setup aids attackers in identifying further attack vectors or valuable assets.

### Lateral Movement: Remote Services (T1021)
After gaining access to an Azure VM, attackers may use remote services, such as SSH or RDP, to move laterally within the network. By leveraging valid credentials or previously gathered information about network topology, they can pivot to other VMs or cloud resources, extending their reach and control.

### Collection: Data from Local System (T1005)
Adversaries often target data stored locally on compromised Azure VMs. This can include sensitive files, databases, or configuration files. Attackers may employ scripts to automate the extraction process, rapidly gathering valuable information which may then be exfiltrated or used to further the attack.

### Exfiltration: Exfiltration Over Network (T1041)
After collecting data from Azure VMs, attackers will typically exfiltrate it over the network. This may involve encrypting or obfuscating the data to avoid detection, then transmitting it to external servers through protocols like HTTP, HTTPS, or FTP. This step often marks the culmination of a successful breach.

### Impact: Data Encrypted for Impact (T1486)
To cause disruption, adversaries may deploy ransomware or encryption malware within Azure VMs, encrypting files and demanding ransom payments. This impact can serve both as an extortion method and as a cover to conceal further malicious activities within the network, posing significant risks to operational continuity and data availability.
