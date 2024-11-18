## T1078.004 - Cloud Accounts
Unauthorized access through compromised cloud accounts can pose a significant threat to Azure Blueprints. Adversaries may exploit stolen credentials or poorly managed access controls to gain unauthorized access and potentially manipulate or corrupt blueprint configurations. This can lead to the provisioning of insecure resources or unauthorized modification of compliance baselines, ultimately compromising the security posture of the entire cloud environment.

## T1098 - Account Manipulation
Adversaries may attempt to manipulate Azure Blueprints access controls, granting themselves or removing others' permissions to secure or critical resources. Using compromised or manipulated accounts, they can alter blueprint definitions and assignments, potentially leading to infrastructure misconfigurations, data exposure, or disruption of compliance measures.

## T1070.006 - Indicator Removal on Host: Clear Cloud Logs
After successful exploitation or blueprint manipulation, adversaries might attempt to clear or alter cloud logs to cover their tracks. This technique aims to delete traces of unauthorized blueprint activities, making detection and forensic analysis difficult. Consequently, investigation efforts are hindered, allowing the adversary to maintain persistence in the environment while avoiding detection.

## T1496 - Resource Hijacking
Resource hijacking involves unauthorized use of cloud resources for purposes that may not align with organizational intents. Adversaries who gain access to Azure Blueprints may alter deployment settings to divert resources for nefarious activities like cryptocurrency mining or the establishment of infrastructure for further attacks. Resource hijacking can lead to excessive costs and degrade service performance.

## T1195.003 - Supply Chain Compromise: Compromise Application
Supply chain compromises can affect Azure Blueprints by introducing vulnerabilities into blueprint artifacts or dependencies used in blueprint assignments. An attacker could tamper with underlying templates or artifacts that blueprints rely on, injecting malicious code or misconfigurations which could subsequently affect multiple resources and deployments across different cloud environments.

## T1586.002 - Credentials from Password Stores: Cloud Instance Metadata API
Adversaries may exploit cloud instance metadata APIs to extract credentials stored within virtual machines deployed as part of Azure Blueprints assignments. Access to these credentials can facilitate lateral movement and further breach into other services and management layers, expanding their control over the impacted environment.

## T1218.005 - Signed Binary Proxy Execution: Mshta
In the context of Azure Blueprints, adversaries could deploy scripts or applications using seemingly legitimate and approved binaries like Mshta.exe to execute codes without triggering security alerts. This technique can help bypass defenses that explicitly monitor for unauthorized or suspicious executables, enabling attackers to execute malicious payloads unnoticed.

## T1134.002 - Access Token Manipulation: Pass the Token
Azure environments often leverage access tokens for authorization. If an adversary is capable of capturing and manipulating access tokens, they can hijack session identities to perform unauthorized actions through Azure Blueprints, such as deploying insecure configurations or extracting sensitive data without detection.
