## Initial Access - Exploit Public-Facing Application (T1190)
An attacker might exploit vulnerabilities in web applications or APIs that utilize Amazon DynamoDB as a backend. By identifying and exploiting these weaknesses, adversaries can gain unauthorized access to the database or related resources. This could include exploiting code injection flaws or configuration errors to manipulate DynamoDB permissions and gain access to sensitive data stored within.

## Persistence - Create or Modify Cloud Instance (G0053)
Threat actors may attempt to persist within the environment by creating or modifying cloud instances that have access to Amazon DynamoDB. They might configure these instances with specific IAM roles or permissions that allow continued data retrieval or modification, ensuring a backdoor remains even if other vulnerabilities are remediated.

## Privilege Escalation - Valid Accounts (T1078)
Privilege escalation can occur when an attacker gains access to user accounts with permissive policies regarding DynamoDB resources. These accounts may have been overlooked or improperly secured, allowing malicious actors to escalate privileges and perform unauthorized read, write, or administrative actions on DynamoDB tables.

## Defense Evasion - Valid Accounts (T1078)
To evade detection, attackers could leverage compromised but legitimate AWS accounts to access DynamoDB tables. By not creating any new accounts or API keys that might trigger alarms, they blend into the normal activity and avoid detection by security monitoring systems that look for anomaly behaviors.

## Credential Access - Cloud Credential Dumping (T1552)
Attackers may attempt to extract credentials from AWS services, applications, or compromised local systems to gain access to DynamoDB. These credentials could be stored in configuration files, environment variables, or memory, and accessing them allows adversaries to interact with DynamoDB APIs directly, bypassing other security controls.

## Discovery - Cloud Service Discovery (T1580)
An adversary who gains initial access to a network may conduct reconnaissance to enumerate AWS resources, including DynamoDB. This involves using APIs to list available services and resources, determining table names, configurations, and access policies. Understanding the environment allows attackers to identify potential targets for further exploitation.

## Lateral Movement - Use Alternate Authentication Material (T1550)
Attackers could use stolen or procured IAM roles, session tokens, or access keys designed for authenticated access to perform lateral movements across DynamoDB instances. These materials offer alternative authentication mechanisms that evade conventional password protections and further the adversary's access across the cloud environment.

## Impact - Data Destruction (T1485)
Incidentally or intentionally, adversaries might employ malicious commands to destroy or severely disrupt data stored within DynamoDB. This could include deleting tables or items, or corrupting table data, resulting in significant operational disruptions or data loss that might require extensive recovery and auditing efforts.

## Impact - Data Manipulation (T1565)
Manipulating data within Amazon DynamoDB is a significant risk, where attackers target the integrity of data for malicious outcomes. They might insert, update, or delete database records illegitimately, affecting business operations, undermining data integrity, or facilitating further attacks like spreading misinformation based on falsified data records.

## Impact - Data Encrypted for Impact (T1486)
Utilizing compromised credentials, adversaries may encrypt tables or entire datasets stored in DynamoDB. Such encryption can be intended as part of extortion efforts to demand a ransom for decryption keys. If successful, this could prevent access to critical data required for business functions or analysis, placing additional pressure on victim organizations.
