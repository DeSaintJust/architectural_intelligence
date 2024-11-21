## Initial Access

### T1190: Exploit Public-Facing Application
Knative applications often expose public APIs and web interfaces which are potential targets for attackers looking to exploit software vulnerabilities. This can include leveraging unpatched zero-day vulnerabilities or commonly known bugs in the software stack used by the application, enabling unauthorized access or execution of malicious code.

## Execution

### T1059: Command and Scripting Interpreter
Once an attacker gains access, they might use scripting capabilities within Knative pods to execute malicious commands or scripts. For example, attackers might leverage environments like bash or PowerShell for command execution, potentially achieving privilege escalation or lateral movement within the cloud environment.

## Persistence

### T1543: Create or Modify System Process
Attackers may modify existing Kubernetes resources, such as Knative Services, to maintain persistence. By deploying backdoors within the container images or embedded scripts, attackers ensure their presence even after restarting services or deploying new application versions.

## Privilege Escalation

### T1068: Exploitation for Privilege Escalation
Attackers may exploit vulnerabilities in the underlying Kubernetes platform or cloud infrastructure supporting Knative to escalate privileges. By gaining elevated permissions, attackers can escape container boundaries, alter service configurations, or gain broader access to cloud resources.

## Defense Evasion

### T1070: Indicator Removal on Host
To avoid detection, attackers might remove logs or disable audit logging within the Knative environment. This action, often achievable via command-line scripts, erases traces of malicious activities and complicates forensic analysis during incident response.

## Credential Access

### T1552: Unsecured Credentials
Misconfigured or exposed credentials in Knative configurations, secrets, or through poor version control practices pose a risk. Attackers accessing these credentials can authenticate with higher privileges, potentially accessing sensitive data or altering application behavior maliciously.

## Discovery

### T1613: Container and Resource Discovery
Attackers conducting reconnaissance may explore the Kubernetes cluster hosting Knative, seeking information about services, configurations, and permissions. This includes querying for container metadata or environmental variables to plan further exploitation activities.

## Lateral Movement

### T1021: Remote Services
Compromised credentials or misconfigured access controls can be exploited by attackers to move laterally within a Kubernetes cluster or across different GCP services. This lateral movement allows attackers to access additional resources and data beyond the initially compromised application.

## Collection

### T1114: Email Collection
Knative services that process or store sensitive information like emails can be targeted by attackers for data collection. By intercepting or redirecting email traffic, attackers could exfiltrate sensitive communication, leading to potential leaks of confidential information.

## Impact

### T1485: Data Destruction
Attackers might exploit vulnerabilities to perform destructive operations within a Knative environment. This can include deleting or corrupting data, impairing application functionalities, or triggering application downtime, significantly impacting business operations.
