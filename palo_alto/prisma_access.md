**Command and Scripting Interpreter (T1059)**  
Attackers may use scripting techniques to execute unauthorized commands in Palo Alto Prisma Access environments. By exploiting command-line interfaces or APIs, malicious actors can deploy scripts to automate actions such as configuring firewalls, altering network settings, or manipulating security rules. This technique can lead to service disruptions and security policy violations.

**Valid Accounts (T1078)**  
Compromise of valid accounts through phishing, credential stuffing, or brute force attacks can lead attackers to gain unauthorized access to Prisma Access. Utilizing legitimate credentials, threat actors can move laterally within the network, access restricted areas, and exfiltrate sensitive data under the guise of an authorized user, thereby going unnoticed.

**Phishing (T1566)**  
Prisma Access users and administrators may be targeted by phishing campaigns designed to harvest credentials or deliver malicious payloads. Successful phishing attacks can lead to unauthorized access, allowing attackers to bypass security controls and establish persistence within the cloud environment.

**Unsecured Credentials (T1552.001)**  
Exposure of credentials, often due to misconfigurations or insufficient security controls, poses a significant threat. Attackers can exploit exposed passwords or tokens to gain access to Prisma Access management interfaces and alter configurations, potentially leading to data breaches or service disruptions.

**Exploitation of Remote Services (T1210)**  
Attackers may exploit vulnerabilities in remote services to gain unauthorized access to the Prisma Access environment. By targeting application programming interfaces (APIs), VPN gateways, or remote management interfaces, adversaries can execute arbitrary commands, escalate privileges, or exfiltrate sensitive information.

**Application Layer Protocol (T1071)**  
Threat actors might abuse application layer protocols, such as HTTP or DNS, to exfiltrate data or establish command-and-control (C2) channels within a Prisma Access deployment. By embedding malicious traffic within legitimate protocol operations, attackers can evade detection from network monitoring tools.

**Ingress Tool Transfer (T1105)**  
Consider the risk of attackers transferring malicious tools and payloads into the Prisma Access environment. This might involve the use of legitimate channels, such as cloud storage services, to introduce software designed to exploit vulnerabilities or establish backdoors for persistent access.

**Data Encrypted for Impact (T1486)**  
The encryption of data by threat actors can be a disruptive tactic, leading to denial-of-service conditions or ransom scenarios. Attackers may target Prisma Access gateways or associated data stores to encrypt data at rest, coercing organizations into paying ransoms to recover access to their data.

**Network Sniffing (T1040)**  
Network sniffing techniques may be employed by adversaries to capture sensitive information traversing the Prisma Access environment. By intercepting unencrypted data or authentication tokens, attackers can gather intelligence on network traffic patterns, compromise communication confidentiality, and identify potential targets for further exploitation.

**Resource Hijacking (T1496)**  
Prisma Access resources may be targeted for hijacking by malicious actors seeking to exploit compute, storage, or networking resources for their purposes. This could involve deploying unauthorized workloads for mining cryptocurrencies, generating profit illicitly while degrading service performance for legitimate users.
