### Initial Access: Cloud Credential Access (T1552.004)

In AWS environments, attackers can obtain initial access by compromising IAM credentials. This can occur through various means such as phishing attacks, credential stuffing, or brute force attacks that target AWS IAM users. Once credentials are compromised, attackers can authenticate into the AWS Management Console or via AWS CLI, gaining the ability to perform actions allowed by the compromised credentials. Key mitigation strategies include enforcing strong password policies, using multi-factor authentication (MFA), and regularly rotating credentials.

### Credential Access: Access Token Manipulation (T1550.001)

Attackers may manipulate access tokens to impersonate legitimate users or escalate privileges within an AWS account. This is especially critical in scenarios involving AWS IAM roles and temporary security credentials issued through AWS Security Token Service (STS). By intercepting or forging these tokens, attackers can bypass authentication controls and gain unauthorized access. Continuous monitoring of AWS CloudTrail logs for API calls involving 'AssumeRole' and suspicious access patterns is essential for detection.

### Privilege Escalation: Abuse Elevation Control Mechanism (T1548)

AWS IAM policies and associated permission sets are prime targets for privilege escalation attacks. Attackers with sufficient privileges may modify policies to grant themselves or their malicious 'IAM entities' broader access. Techniques include exploiting overly permissive "wildcard" policies, direct role assumption, or modification of trust policies for cross-account access. Regular audits of IAM policies and implementation of least privilege principles are crucial countermeasures.

### Defense Evasion: Permissions Modification (T1222)

Attackers may attempt to modify IAM policies to evade detection and persist within an AWS environment. This involves altering resource-based policies, identity-based policies, or SCPs (Service Control Policies) to mask unauthorized activities or prevent logging. Detecting these modifications requires comprehensive logging and alerting through AWS CloudTrail and AWS Config to notify security teams of unexpected changes to IAM configurations.

### Credential Access: Brute Force (T1110)

A brute force attack against AWS IAM involves systematically attempting various password combinations to gain access to user accounts. Attackers typically target accounts without MFA, leveraging exposed usernames possibly obtained through previous data breaches. To defend against brute force attacks, implementing account lockout policies, MFA, and monitoring of IAM login attempts can prove effective.

### Collection: Cloud Service Dashboard (T1538)

After obtaining access to AWS IAM credentials, adversaries may leverage the AWS Management Console (Service Dashboard) to explore and collect data about the cloud environment, configurations, and sensitive information. Techniques deployed on the console include exploring resource allocations, peeking into Amazon S3 storage listings, and examining deployed IAM roles and permissions. Employing role-based access control and cloud-native monitoring solutions can mitigate unauthorized access to sensitive information.

### Persistence: Cloud Account (T1098)

To maintain persistence, attackers may create new IAM users, policies, or access keys surreptitiously within the targeted AWS environment. These new entities are then used to maintain access despite defensive efforts like credential rotation or account lockdowns. Regular audits of IAM accounts and usage patterns, combined with vigilant IAM access reviews, can help identify and dismantle such persistence efforts.

### Impact: Resource Hijacking (T1496)

AWS IAM misconfigurations or previously obtained credentials can enable attackers to hijack compute resources, engaging them for illicit activities such as cryptocurrency mining. These activities result in escalated billing and operational disruptions. AWS CloudWatch and Budget Alerts provide mechanisms to detect abnormal resource utilization, which can be correlated with IAM activities to detect and respond to potential resource hijacking.
