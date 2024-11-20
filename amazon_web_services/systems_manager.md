## Initial Access

### [T1190] Exploit Public-Facing Application
AWS Systems Manager, particularly its automation and document services, can become a target if its API endpoints or AWS Management Console are exposed to the internet without proper security controls. Threat actors might exploit vulnerabilities inherent in the interface or the configuration, especially if security patches are not timely applied.

## Execution

### [T1059/002] Command and Scripting Interpreter: PowerShell
Since AWS Systems Manager integrates with on-premises systems via the Systems Manager Agent, an attacker who has gained access to these instances might leverage PowerShell scripts to execute malicious commands, particularly on Windows-based systems. With Systems Manager having the capability to execute scripts, improper access control could allow execution of malicious PowerShell commands.

## Persistence

### [T1547/001] Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder
Adversaries may aim to achieve persistence by placing malicious scripts or commands in the AWS Systems Manager, which is later distributed to multiple EC2 instances or on-prem machines, using the "State Manager" function. They could manipulate the SSM document contents to include persistence mechanisms that automatically execute at boot or logon.

## Privilege Escalation

### [T1548/002] Abuse Elevation Control Mechanism: Elevated Execution with Passed Access Token
AWS Systems Manager Run Command and State Manager can be configured to execute with elevated privileges. An attacker who has obtained valid API keys or access tokens can exploit this configuration to run commands as a privileged user, thereby escalating their privileges and potentially compromising the instance or associated resources.

## Defense Evasion

### [T1562/001] Impair Defenses: Disable or Modify Tools
An attacker with access to AWS Systems Manager could disable logging and auditing features within it or modify the CloudWatch alarms to evade detection. This could lead to unnoticed execution of malicious commands across target instances. By disabling SSM agent logs or interfering with the reporting mechanism of Systems Manager, adversaries can hide their tracks effectively.

## Credential Access

### [T1552/001] Unsecured Credentials: Credentials in Files
Misconfigured Systems Manager parameters or unsecured SSM documents might inadvertently lead to exposure of sensitive credentials. Attackers could scan for configuration files or document content distributed via Systems Manager that contains hardcoded credentials, gaining unauthorized access to other systems or services.

## Discovery

### [T1083] File and Directory Discovery
The Systems Manager Agent can be abused by adversaries to gather information about files and directories across managed instances. An attacker, leveraging AWS Systems Manager's access, could execute commands or scripts to list directories and files on EC2 instances, seeking sensitive information or system configurations.

## Lateral Movement

### [T1021] Remote Services
AWS Systems Manager can be used by an attacker to move laterally across instances in the same VPC or account by using the Run Command feature. If access controls are weak, this could allow an adversary to deploy scripts or commands to spread their presence across a network or execute ransomware.

## Collection

### [T1114] Email Collection
If AWS Systems Manager has been configured to collect or manage email notifications (for example, through automation scripts or state management targeting email-related services), adversaries could leverage this misconfiguration to collect sensitive email data by executing malicious scripts via the compromised Systems Manager.

## Command and Control

### [T1102] Web Service
In some scenarios, an attacker might set up a rogue instance or external service to act as a command and control server, utilizing AWS Systems Manager to send periodic instructions or scripts to "call home" and await further commands. This misuse of Systems Manager Run Command could facilitate continuous remote control over compromised resources. 

## Impact

### [T1489] Service Stop
An adversary might disrupt operations by using AWS Systems Manager to stop critical services across systems. They could craft commands or SSM documents that disable essential services, leveraging the automation features to cause widespread impact and impair business functions.
