## Initial Access: Valid Accounts (T1078)
Threat actors may attempt to obtain valid account credentials through tactics such as phishing attacks, social engineering, or credential stuffing. These valid credentials can then be used to gain unauthorized access to GCP Compute Engine instances. Once inside, attackers can perform malicious activities without raising alarms as they are using legitimate user access methods.

## Execution: Command and Scripting Interpreter (T1059)
Attackers might utilize command and scripting interpreters like bash or PowerShell to execute unauthorized commands on GCP Compute Engine instances. These interpreters provide a flexible environment for executing malicious scripts that can compromise system integrity, exfiltrate data, or establish further persistence.

## Persistence: Create or Modify System Process (T1543)
An attacker who gains access to a GCP Compute Engine instance might establish persistence by creating or modifying system processes. This could involve inserting malicious startup scripts, altering legitimate system binaries, or adding new system services that execute upon system boot or at regular intervals.

## Privilege Escalation: Exploitation for Privilege Escalation (T1068)
A potential threat to GCP Compute Engine includes the exploitation of software vulnerabilities for privilege escalation. Attackers facing privilege restrictions may leverage unpatched exploits to gain higher-level privileges such as root or administrative access, thus extending their control over instances.

## Defense Evasion: Indicator Removal on Host (T1070)
Attackers might attempt to hide their tracks within GCP Compute Engine instances by deleting or modifying logs that could reveal their activities. Techniques such as clearing bash histories, editing log files, or disabling audit logging can be used to obscure evidence of unauthorized activities.

## Credential Access: Unsecured Credentials (T1552)
GCP Compute Engine instances may have credentials stored in unsecured formats such as environment variables, application configuration files, or instance metadata. Threat actors, once gaining access to an instance, can harvest these credentials to access further resources within the GCP environment.

## Discovery: Cloud Service Discovery (T1580)
An attacker with access to a GCP Compute Engine instance could conduct cloud service discovery to map the organization's cloud infrastructure. By querying the GCP environment, attackers can identify assets, services, configurations, and any potentially exploitable misconfigurations.

## Lateral Movement: Remote Services (T1021)
Threat actors may use legitimate remote service protocols supported by GCP Compute Engine, such as SSH or RDP, to move laterally within the cloud environment. By leveraging valid credentials and Open Network Ports, attackers can move between instances, escalating their control across the network.

## Collection: Data from Cloud Storage Object (T1530)
Once inside the GCP Compute Engine instance, attackers could attempt to access Google Cloud Storage to steal or corrupt stored data. By leveraging poor storage permissions or valid credentials, attackers can download, modify, or delete data hosted in cloud storage, affecting data confidentiality and availability.

## Exfiltration: Exfiltration Over Command and Control Channel (T1041)
Exfiltration of sensitive data might be performed over established command and control channels. By using protocols such as HTTP(S), DNS, or custom C2 mechanisms, attackers can stealthily transfer data from GCP Compute Engine instances to their external servers while avoiding detection.

## Impact: Data Destruction (T1485)
A significant threat to GCP Compute Engine instances includes data destruction, where attackers intentionally delete critical files or data stores. This could involve utilizing direct delete commands, disrupting backups, or deploying ransomware that encrypts and deletes data, leading to a denial of service and potential data loss.
