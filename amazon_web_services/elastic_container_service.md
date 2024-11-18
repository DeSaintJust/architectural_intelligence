## Initial Access - Phishing: Spearphishing Service
Adversaries may employ phishing through email or other electronic communication channels to harvest credentials or deliver malicious payloads. They could craft messages targeting ECS administrators or developers, enticing them to provide access credentials. Once the credentials are compromised, attackers can gain unauthorized access to ECS resources.

## Initial Access - Valid Accounts
If an attacker acquires valid user credentials, whether through credential stuffing, password spraying, or exploiting reused passwords, they can gain access to ECS resources. This unauthorized access can facilitate further malicious activities, including the deployment of rogue containers or tampering with existing services.

## Execution - Command and Scripting Interpreter
Adversaries can utilize command-line interfaces like AWS CLI, or scripts within compromised ECS environments to execute malicious commands. They might leverage these capabilities to alter configurations, deploy compromised container images, or manipulate ECS task definitions to enhance their control over the environment.

## Persistence - Create or Modify System Process
Attackers may achieve persistence in ECS by creating or modifying ECS Service configurations to ensure that malicious containers are launched upon service start or restart. By embedding backdoor images or manipulating container orchestration, adversaries can maintain their foothold within the infrastructure.

## Privilege Escalation - Container Administration Command
Malicious actors can escalate privileges by exploiting administrative commands within containers hosted on ECS. They may leverage misconfigured IAM roles that grant excessive permissions to escalate from container management to broader AWS account access.

## Defense Evasion - Obfuscated Files or Information
Attackers often obfuscate malicious scripts or contents within containers to avoid detection. On ECS, they might utilize encoded scripts or packages disguised within container images or employ unconventional file structures to hide their activities from monitoring tools.

## Credential Access - Container API
Exploitation of the ECS container API allows attackers to capture sensitive information such as environment variables, which often contain credentials. Misconfigured IAM roles or exposed metadata URLs can further facilitate the unauthorized retrieval of credentials critical to maintaining secure access to cloud resources.

## Discovery - Cloud Service Discovery
Adversaries might leverage discovery patterns to enumerate ECS services, tasks, and configurations. Given access to ECS management environments, attackers can map cloud architectures and understand ECS deployment structures to inform subsequent attacks and identify potential vulnerabilities.

## Lateral Movement - Remote Services
Compromise of network configurations or access permissions may enable attackers to move laterally through ECS environments. Exploitation of VPC connectivity, container-to-container communication, or IAM roles can facilitate unauthorized movement within distributed ECS architectures.

## Impact - Data Destruction
In ECS, adversaries with destructive intent may delete or alter ECS services, tasks, or associated resources to disrupt operations. This includes wiping container images, corrupting task definitions, or disrupting networking configurations that underpin application availability.

## Impact - Resource Hijacking
Attackers may hijack ECS resources for unauthorized activities, such as cryptocurrency mining or launching additional malicious containers. By exploiting ECS orchestration capabilities, they can redirect computational resources to malicious workloads, increasing operation costs and impacting legitimate application performance.
