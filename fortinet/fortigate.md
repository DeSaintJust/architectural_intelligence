### Initial Access - Exploit Public-Facing Application

Fortinet FortiGate firewalls, like any other exposed application, may be vulnerable to exploitation through public-facing components. Attackers often seek to exploit known vulnerabilities in web applications to gain initial access. For instance, exploiting unpatched CVEs (Common Vulnerabilities and Exposures) can allow threat actors to bypass authentication mechanisms or execute arbitrary code. Such attack vectors rely on identifying weaknesses in improperly configured services or outdated software versions. Maintaining up-to-date patches and regular vulnerability assessments are critical to mitigating these threats.

### Initial Access - Supply Chain Compromise

Threat actors can also exploit Fortinet FortiGate devices through supply chain compromises. This vector involves inserting malicious components into the hardware or software supply chain before it reaches the end-user. Attackers can potentially gain unauthorized access or inject malicious code into the FortiGate system. Organizations can mitigate this threat by procuring equipment from reputable vendors, verifying integrity through digital signatures, and ensuring rigorous security checks on all updates and patches.

### Execution - Command and Scripting Interpreter

Once inside the FortiGate environment, attackers may seek to execute commands or scripts to further their control over the system. This is often done by exploiting scripting interfaces or command execution features that are either misconfigured or improperly secured. These actions can include running scripts or commands that manipulate the firewall rules, extract sensitive data, or create backdoors for persistent access. Organizations should ensure command execution features are restricted, monitored, and logged to mitigate such risks.

### Persistence - Implant Internal Scripts

Threat actors may establish persistence by implanting internal scripts on Fortinet FortiGate devices. By embedding malicious scripts within the device's firmware or configuration, adversaries ensure their activities continue across reboots and firmware updates. This can be particularly destructive as it provides long-term access without needing re-infection. Regular integrity checks and verifying configurations against baselines can help detect and prevent such persistence techniques.

### Defense Evasion - Process Injection

Adversaries might attempt to evade detection by using process injection techniques within the FortiGate environment. Process injection involves inserting code into legitimate processes on the device in order to obfuscate malicious activity. This can be used to mask the execution of unauthorized commands or tools under the guise of legitimate processes. Mitigating this threat requires robust monitoring of process behavior and anomaly detection systems.

### Credential Access - Brute Force

Fortinet FortiGate devices may be targeted through brute force attacks, where adversaries systematically attempt various passwords until gaining unauthorized access. Default or weak credentials are often targeted, highlighting the importance of enforcing strong password policies. Implementing account lockout mechanisms, using multi-factor authentication, and monitoring login attempts are effective strategies to guard against brute force attacks.

### Discovery - Network Service Scanning

Attackers often engage in network service scanning to map FortiGate firewall configurations and services. By identifying open ports and accessible services, adversaries can tailor their subsequent actions, such as exploiting vulnerabilities or conducting lateral movements. Network service scanning is generally the precursor to more targeted attacks. Protection against these threats involves using intrusion detection systems and ensuring that unnecessary services and ports are closed.

### Lateral Movement - Exploitation of Remote Services

Once attackers have a foothold in the network, they may attempt lateral movement by exploiting remote services on Fortinet FortiGate devices. This involves using exploits to gain access to other network devices or services, potentially compromising more of the network infrastructure. Network segmentation, proper configuration management, and vulnerability patching are critical to preventing such lateral movements.

### Command and Control - Web Service

Adversaries can establish command and control (C2) channels through web services on compromised FortiGate devices. By embedding C2 instructions within normal web traffic, attackers maintain communication with compromised devices without raising suspicion. Encryption and tunneling techniques are often used to evade detection. Monitoring web traffic for anomalies, considering the implementation of network traffic analysis tools, and employing data loss prevention mechanisms can mitigate this threat.

### Exfiltration - Exfiltration Over C2 Channel

After gaining access to sensitive information, threat actors might exfiltrate data over established command and control channels. Fortinet FortiGate devices can be used as pivot points to route exfiltrated data, often masking it within legitimate network traffic. This makes detection challenging, as normal traffic patterns are mimicked. Continuous monitoring of data flows, combined with anomaly detection and data leakage prevention technologies, can help in identifying and stopping data exfiltration attempts.
