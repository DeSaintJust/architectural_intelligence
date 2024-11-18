## Initial Access: Valid Accounts [T1078]
Threat actors may gain initial access to EC2 instances by compromising valid AWS credentials through methods such as phishing, credential stuffing, or brute-force attacks. Once they possess legitimate credentials, adversaries can initiate and manipulate EC2 instances, potentially gaining further access to sensitive data or additional resources within the AWS environment.

## Execution: Command and Scripting Interpreter [T1059]
Threat actors often execute malicious scripts or commands on EC2 instances, leveraging built-in interpreters like bash, PowerShell, or Python. These scripts can be used to download additional payloads, establish persistence, or alter security configurations, effectively leading to further stages of an attack.

## Persistence: Boot or Logon Initialization Scripts [T1037]
After gaining access to an EC2 instance, attackers can establish persistence by modifying startup scripts. By inserting malicious code into these scripts, adversaries ensure that their payloads are executed automatically on system boot, allowing them to maintain a foothold on the compromised environment.

## Privilege Escalation: Sudo and Sudo Caching [T1548]
Attackers with low-privileged accounts may exploit misconfigured sudo permissions to escalate their privileges on EC2 instances. This often involves accessing the sudoers file to execute commands as root or utilizing cached credentials to perform unauthorized administrative actions.

## Defense Evasion: Disable Security Tools [T1562]
Adversaries may attempt to disable or tamper with security tools installed on EC2 instances, such as host-based intrusion detection systems or anti-malware solutions. This technique enables attackers to conduct malicious activities without being detected, extending the duration and impact of their operations.

## Credential Access: Unsecured Credentials [T1552]
Threat actors frequently target unsecured credentials stored on EC2 instances, such as API keys, SSH keys, or IAM instance profile credentials. Such credentials can be leveraged to access additional AWS services or escalate privileges within the environment, facilitating broader access to critical resources.

## Discovery: Cloud Service Dashboard [T1538]
Attackers may use stolen credentials to access Amazon's Management Console and explore AWS service dashboards, gathering information about the victim's infrastructure. This can lead to a better understanding of the environment, allowing adversaries to identify potential targets and plan further exploitation.

## Lateral Movement: Use Alternate Authentication Material [T1550]
Adversaries can move laterally within AWS environments by using newly acquired credentials, such as session tokens or temporary security credentials, acquired via compromised EC2 instances. This lateral movement can facilitate access to additional EC2 instances or other AWS services, broadening the attack surface.

## Collection: Data from Local System [T1005]
Attackers aim to collect sensitive data from EC2 instances by accessing local files or capturing data streams. They may exfiltrate credentials, configuration files, or intellectual property, which can be further abused or sold in underground markets.

## Exfiltration: Exfiltration Over Web Service [T1567]
Using EC2 instances, adversaries can exfiltrate data by leveraging web services such as HTTP/S to avoid detection through standard network monitoring tools. This can involve concealing data within legitimate traffic or employing steganographic techniques to further mask exfiltration efforts.

## Impact: Resource Hijacking [T1496]
EC2 instances can be targeted for resource hijacking, where attackers harness compute resources for their purposes, such as cryptocurrency mining. This unauthorized use of resources leads to increased service costs and potential performance degradation, impacting legitimate operations within the AWS environment.
