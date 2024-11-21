### Initial Access: Exploit Public-Facing Application (T1190)
Prisma Cloud, like any cloud-based service, may be vulnerable to initial access attacks through the exploitation of public-facing applications. Attackers may exploit vulnerabilities in web services, APIs, or other entry points exposed to the internet to gain unauthorized access. This exploitation can lead to unauthorized control over cloud environments, potentially allowing the attacker to execute further malicious activities.

### Persistence: Valid Accounts (T1078)
Attackers may seek persistence within the cloud environment by leveraging valid accounts. If user credentials are compromised through techniques such as phishing or brute force attacks, attackers can maintain access over an extended period. This can further be compounded if they are able to escalate privileges and maintain persistent access through legitimate user accounts.

### Privilege Escalation: Cloud Services (T1525)
Privilege escalation can occur when attackers exploit weaknesses in IAM policies, roles, or permissions within Prisma Cloud. By escalating privileges, attackers can perform unauthorized actions or access resources beyond their initial access level. Misconfigured roles and overly permissive IAM permissions are often targeted for this purpose.

### Defense Evasion: Disable Cloud Logs (T1562.008)
Attackers aiming to avoid detection may attempt to tamper with cloud logging and monitoring services. By disabling or altering log settings, they can evade detection by incident response teams, making it difficult to track changes or unauthorized activities in the cloud environment.

### Credential Access: Cloud Instance Metadata API (T1552.005)
Access to credential information via the cloud instance metadata API is a notable threat to Prisma Cloud environments. If an attacker gains access to an instance that trusts the metadata API, they can obtain temporary credentials or keys which can be used to access other parts of the cloud infrastructure.

### Discovery: Cloud Service Dashboard (T1538)
Attackers engage in discovery techniques to understand the cloud resources and services available. Accessing a cloud service dashboard, either through legitimate or compromised access, allows attackers to gather information about the environment, which can be used to identify further opportunities for exploitation.

### Impact: Data Destruction (T1485)
In the event of a breach, attackers may pursue destructive actions such as data destruction. This impact technique involves the deletion of critical data or backups within Prisma Cloud environments. Successful execution of this threat can lead to significant operational disruption and potential data loss.

### Impact: Resource Hijacking (T1496)
Resource hijacking involves the unauthorized usage of cloud resources, often for activities like cryptocurrency mining. Attackers exploit misconfigured or under-secured cloud environments, leading to increased resource consumption, degraded performance, and unexpected billing charges.
