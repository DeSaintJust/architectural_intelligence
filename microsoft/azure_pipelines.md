### Initial Access - T1078: Valid Accounts
Threat actors might gain unauthorized access to Azure Pipelines by acquiring valid user credentials through phishing, credential stuffing, or brute force attacks. With valid credentials, attackers could perform actions and workflows as if they were legitimate users, potentially tampering with pipelines, stealing secrets from the environment, or deploying malicious code.

### Persistence - T1027: Obfuscated Files or Information
Attackers might utilize obfuscation techniques to hide their malicious scripts or artifacts within Azure Pipelines. By disguising their code, they can persist within the CI/CD environment undetected, allowing them to persistently affect build and deployment processes over time.

### Privilege Escalation - T1134: Access Token Manipulation
In Azure Pipelines, attackers can escalate privileges by manipulating access tokens. By acquiring and abusing tokens associated with service connections or identity providers, they can execute actions on higher-privileged resources, conduct lateral movement, or execute sensitive operations within the pipeline.

### Defense Evasion - T1070: Indicator Removal
An attacker may attempt to cover their tracks within Azure Pipelines by deleting logs or altering files that record pipeline activities. This can prevent security teams from detecting unauthorized access or modifications, allowing them to evade detection by obstructing forensic investigation efforts.

### Credential Access - T1552: Unsecured Credentials
Azure Pipelines that store secrets, keys, or tokens insecurely are vulnerable to credential theft. Attackers can access these sensitive credentials, potentially exfiltrating data, accessing sensitive resources, or integrating with other compromised services to facilitate larger attacks along the CI/CD chain.

### Discovery - T1082: System Information Discovery
Attackers often seek to gather system information and contextual data within Azure Pipelines, such as build configurations, environment variables, and connected resources. This reconnaissance helps them understand the pipeline architecture and identify how best to target the environment for further exploitation.

### Lateral Movement - T1021: Remote Services
Gaining access to Azure Pipelines might allow an attacker to use the service connections to communicate and move laterally across interconnected cloud resources. This movement can potentially expose additional systems to compromise and enable attackers to deploy malware or harvest more credentials on secondary targets.

### Collection - T1005: Data from Local System
Malicious actors may gather data stored within Azure Pipelines such as codebases, configuration files, and secrets. By collecting these data, attackers can exfiltrate valuable intellectual property or gain insights into vulnerabilities and capabilities in the victim's applications and infrastructure.

### Impact - T1496: Resource Hijacking
One impactful threat to Azure Pipelines is resource hijacking, where attackers exploit compute resources for their own purposes, such as cryptocurrency mining. This unauthorized use can lead to increased costs, reduced performance, and potential disruptions to legitimate pipeline operations.
