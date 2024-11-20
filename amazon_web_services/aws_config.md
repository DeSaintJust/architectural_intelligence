### Credential Access - Valid Accounts (T1078)

A significant threat to AWS Config arises from the use of compromised credentials to gain unauthorized access. Attackers may obtain valid AWS credentials through phishing, brute force, or credential stuffing attacks. Once credentials are compromised, an attacker can use legitimate account access to manipulate or disable AWS Config, destroy logs, or change settings to cover their tracks. By regularly rotating credentials and using AWS Identity and Access Management (IAM) policies, organizations can mitigate these risks.

### Defense Evasion - Log Deletion (T1070.001)

AWS Config logs provide crucial insights into the configuration changes and compliance states of AWS resources. Threat actors might attempt to disable or tamper with these logs to evade detection of their malicious activities. By leveraging IAM policies with strict permissions and utilizing AWS Config's integration with services like AWS CloudTrail and Amazon CloudWatch, organizations can detect and respond quickly to suspicious activities involving log tampering.

### Discovery - Cloud Service Discovery (T1580)

Once inside an AWS environment, a threat actor might perform discovery actions to understand the cloud service architecture, including AWS Config's role within it. They may use APIs to list AWS Config rules and compliance status to identify security misconfigurations they can exploit. Implementing least privilege access and monitoring API calls through AWS CloudTrail can help mitigate these discovery activities.

### Persistence - Account Manipulation (T1098)

Attackers might attempt to manipulate AWS accounts by altering AWS IAM roles and policies associated with AWS Config to maintain persistence within an environment. They could create new IAM roles with privileged access permissions or modify existing roles to ensure continuous access. To proactively defend against such threats, regularly audit IAM configurations and roles, and employ multifactor authentication (MFA) for sensitive accounts.

### Impact - Data Destruction (T1485)

AWS Config's stored configuration history is valuable for security audits and compliance. Attackers may try to delete or alter this data to prevent security teams from understanding past misconfigurations or unauthorized changes. By ensuring that AWS Config data is backed up securely and only providing delete permissions to trusted accounts, organizations can minimize the likelihood and impact of such destructive actions.

### Collection - Data from Cloud Storage Object (T1530)

Adversaries may target AWS Config data stored in Amazon S3 buckets, where configuration snapshots and configuration history are typically kept. Through gained access, they might collect sensitive configuration data that can be exploited in further attacks. Encrypting data at rest and in transit, configuring strict bucket policies, and using Amazon Macie to detect and protect sensitive information can help prevent such data collection.

### Credential Access - Cloud Identity (T1528.001)

Compromising cloud identity services like AWS IAM can provide adversaries with access to AWS Config and other AWS services. Attackers may use these identities to launch further attacks or pivot within the cloud environment. Employing strict monitoring through AWS CloudTrail, auditing user access, and implementing automated incident response can help identify and mitigate the threat posed by cloud identity compromise.
