### Initial Access - [T1078.003: Valid Accounts: Cloud Accounts](https://attack.mitre.org/techniques/T1078/003/)
Threat actors may attempt to gain unauthorized access to AWS CodePipeline by compromising valid cloud account credentials. This can occur through phishing, credential stuffing, or exploiting weak passwords. Once access is gained, attackers can manipulate pipeline configurations, inject malicious code into production environments, or exfiltrate sensitive build artifacts.

### Defense Evasion - [T1562.001: Impair Defenses: Disable or Modify Tools](https://attack.mitre.org/techniques/T1562/001/)
Attackers may attempt to evade detection by altering or disabling security logging and monitoring within AWS CodePipeline. They can modify CI/CD logging settings or configurations, hindering the ability of defenders to detect unauthorized activities, such as changes to pipeline executions or unauthorized access attempts.

### Execution - [T1059.006: Command and Scripting Interpreter: Python](https://attack.mitre.org/techniques/T1059/006/)
AWS CodePipeline supports various stages that might involve the execution of scripts (e.g., build or deploy scripts). Adversaries might exploit this capability to execute malicious Python scripts within custom actions or AWS Lambda functions integrated with the pipeline, potentially leading to further compromise of the environment.

### Persistence - [T1136.003: Create Account: Cloud Account](https://attack.mitre.org/techniques/T1136/003/)
To maintain long-term access, adversaries might create new IAM users, roles, or access keys in AWS that are used by AWS CodePipeline. By maintaining these persistent accounts, malicious actors can ensure continued access to the pipeline, even after initial compromise paths have been blocked or closed by defenders.

### Privilege Escalation - [T1078: Valid Accounts](https://attack.mitre.org/techniques/T1078/)
Threat actors who compromise lower-privileged accounts can attempt privilege escalation to gain higher-level access to AWS CodePipeline resources. This can involve exploiting API token leaks, misconfigured IAM policies, or vulnerabilities in connected services to elevate their privileges and perform actions reserved for administrative users.

### Discovery - [T1083: File and Directory Discovery](https://attack.mitre.org/techniques/T1083/)
Upon gaining access to AWS CodePipeline, attackers might list or examine specific files, directories, or repository artifacts to understand the pipeline configuration, source code repositories, or credentials stored as environment variables. This reconnaissance informs further malicious activities such as data exfiltration or sabotaging the build process.

### Credential Access - [T1552.001: Unsecured Credentials: Credentials In Files](https://attack.mitre.org/techniques/T1552/001/)
Adversaries could exploit poorly managed secrets, such as improperly secured API keys or credentials stored in plain text within the pipeline configuration files or environment variables. These credentials may grant unauthorized access to other AWS services or external systems that are integral to the CI/CD workflow.

### Collection - [T1114.003: Email Collection: Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003/)
In some setups, AWS CodePipeline notifications, error logs, or code review notifications may be sent via email. Adversaries could set up forwarding rules on compromised accounts to collect these emails, allowing them to gather intelligence on pipeline operations, errors, or sensitive information discussed in code reviews and logs.

### Impact - [T1486: Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486/)
An adversary with sufficient access could encrypt critical configuration files, deployment artifacts, or source code managed by AWS CodePipeline. This encryption can disrupt the CI/CD process, causing downtime and impacting the organization's ability to deploy or update applications effectively, potentially forcing the victim to pay a ransom to regain access.
