## Initial Access - Phishing: Spearphishing Attachment (T1566.001)
Spearphishing is a prevalent method cyber adversaries might use to gain initial access to Azure SQL environments. By crafting emails containing malicious attachments, attackers can trick users into executing the attacker's payload. These payloads often deploy malware designed to harvest credentials or inject malicious code into trusted SQL environments.

## Initial Access - Cloud Account Compromise (T1078.004)
Attackers may use credential stuffing or phishing to compromise cloud accounts associated with Azure SQL. Once access is gained, they can explore and manipulate databases, steal sensitive information, or cause disruptions. Securing account credentials through strong password policies, multi-factor authentication, and anomaly detection is essential.

## Execution - SQL Injection (T1190)
SQL Injection is a direct threat to Azure SQL databases. This occurs when an attacker manipulates a SQL query's structure to execute arbitrary SQL code. Threat actors can exploit this to extract sensitive data, modify database contents, or perform remote code execution if combined with other vulnerabilities or misconfigurations in the application.

## Execution - Remote Services, PowerShell (T1569.002)
Attackers utilizing remote services might leverage PowerShell scripts to interact with Azure SQL databases. This method allows attackers to automate tasks or execute malicious code. PowerShell's powerful capabilities mean it can access Azure resources, manipulate database schemas, or run under privileged operations if not securely managed.

## Persistence - Valid Accounts (T1078)
Maintaining access through valid accounts is a common persistence technique attackers might use against Azure SQL environments. Once they gain control of a legitimate account, they can continuously access the database undetected, especially if the account has high-privilege access or its usage blends in with normal activities.

## Persistence - Database Backdoors (T1505.003)
Attackers may establish backdoors in the database, allowing them continued access for later exploitation. This could involve creating stored procedures that trigger upon specific events or loading malicious UDFs (User Defined Functions) to maintain persistence without easily noticeable alterations to standard procedures.

## Privilege Escalation - Exploitation for Privilege Escalation (T1068)
To gain privileged access to Azure SQL databases, attackers may exploit vulnerabilities within the SQL service or related components. These vulnerabilities could involve misconfigurations or unpatched flaws that allow attackers to elevate their privileges within the SQL environment, gaining broader access to sensitive data or administrative capabilities.

## Defense Evasion - Obfuscated Files or Information (T1027)
Threat actors targeting Azure SQL often obfuscate their code to evade detection. By employing techniques such as PowerShell obfuscation, encoding stored procedures, or encrypting command execution scripts, attackers can hide their actions from both endpoint detection systems and manual review processes, maintaining their foothold under the radar.

## Credential Access - Credentials in Files (T1552.001)
Azure SQL configurations or applications interacting with the database may inadvertently store credentials in files, such as configuration files or scripts. Attackers might exploit weaknesses to access these files, either through direct server access or exploiting application flaws, to harvest credentials and laterally move across the network or to elevate access.

## Discovery - Cloud Service Discovery (T1580)
Adversaries may perform discovery activities by enumerating Azure subscriptions, services, and resources to identify Azure SQL instances. Discovering specific configurations, database options, and linked services helps attackers understand the environment and identify potential attack vectors or misconfigurations they can exploit.

## Lateral Movement - Remote Services, RDP/SMB (T1021.001)
Attackers using remote services such as RDP or SMB can use stolen credentials or exploits to move laterally between systems interfacing with Azure SQL. This lateral movement could allow attackers to find and exfiltrate data directly from the database or pivot between systems to maintain undetected access or expand their control over the Azure environment.

## Impact - Data Destruction (T1485)
Threat actors may aim to destroy or corrupt data within Azure SQL databases, either as a direct goal or as part of a broader attack, such as ransomware. This can involve deleting tables, applying destructive queries, or encrypting data to disrupt business operations, leading to data loss and operational downtime.
