## Network Sniffing (T1040)
Azure Virtual WAN could be susceptible to network sniffing if cyber adversaries gain access to the network between users and the WAN or within the cloud infrastructure. Attackers may leverage packet capture tools to intercept and analyze network traffic traversing through the Virtual WAN, potentially exposing sensitive information such as authentication tokens or unencrypted data. To mitigate this threat, ensure that encryption is enforced end-to-end and monitor for unusual packet capture activities.

## Man-in-the-Middle (MitM) (T1557)
A Man-in-the-Middle attack in an Azure Virtual WAN environment might occur when an attacker positions themselves between two network endpoints to intercept, alter, or inject communications. This threat could lead to data manipulation or credential theft. Utilizing TLS encryption for transport security and multi-factor authentication can reduce the risk posed by MitM attacks.

## Exploit Public-Facing Application (T1190)
If any public-facing services are mistakenly exposed through Azure Virtual WAN configurations, attackers could exploit vulnerabilities within those services to launch attacks on the WAN infrastructure. Ensuring all software and services are kept up-to-date with security patches, employing Web Application Firewalls (WAFs), and conducting regular security assessments can help prevent such exploits.

## Account Manipulation (T1098)
In Azure Virtual WAN, unauthorized account manipulation might occur if attackers gain access to privileged accounts. This could involve altering roles or permissions to facilitate further attacks. Employing Identity and Access Management (IAM) best practices, like least privilege access, role-based access controls, and regular audit logging of account activity, can help safeguard against account manipulation.

## Credential Access via Password Spraying (T1110.003)
Attackers may attempt password spraying against accounts associated with Azure Virtual WAN to gain unauthorized access using a list of common passwords. This technique can lead to account compromise and subsequent misuse of WAN resources. To defend against this threat, implement account lockout policies, multi-factor authentication, and monitor login attempts for patterns indicative of password spraying.

## Creation of Cloud Accounts (T1136.003)
An attacker who gains partial access to Azure resources may attempt to create additional cloud accounts within the Virtual WAN configuration to establish persistent access. These accounts might be used for launching attacks or exfiltrating data. Regularly reviewing users, groups, and roles for unnecessary or unexpected accounts, and revoking unauthorized accounts promptly, can prevent this threat.

## Data Encrypted for Impact (T1486)
In a malicious scenario involving Azure Virtual WAN, attackers could encrypt data being transmitted over the WAN to disrupt availability and demand ransom. Encryption at this level could disrupt operations severely. Countermeasures include ensuring comprehensive data backups, maintaining incident response plans, and monitoring network traffic for signs of large-scale encryption activities that could indicate a ransomware attempt.

## Traffic Duplication (T1020)
Azure Virtual WAN could be targeted for traffic duplication, where attackers redirect traffic to monitor, capture, or manipulate the data without authorization. This could involve changing route tables or employing compromised network devices. Employing network access controls, conducting regular audits of network configurations, and maintaining integrity of routing policies help to prevent traffic duplication attacks.
