## Initial Access

**Phishing: Spearphishing via Service (T1566.002):** Attackers may target AWS Copilot developers or administrators through spearphishing emails that direct recipients to malicious websites or attachments. These emails can appear to be legitimate notifications from AWS services, exploiting trust to gain credentials or execute unauthorized actions within an AWS Copilot environment.

## Execution

**Command and Scripting Interpreter: Bash (T1059.004):** If an attacker gains access to the underlying infrastructure where AWS Copilot is deployed, they can use Bash scripts to execute unauthorized operations. This could involve modifying application deployments, accessing environment variables, or interacting with AWS services directly via the command line.

## Persistence

**Valid Accounts (T1078):** Compromised or maliciously created valid AWS IAM accounts can be used to maintain persistent access to AWS Copilot-managed resources. Attackers might create accounts with limited visibility but sufficient privileges to alter application configurations or access sensitive data without detection.

## Privilege Escalation

**Abuse Elevation Control Mechanism: Sudo and Sudo Caching (T1548.003):** Exploiting sudo privileges in the environment where AWS Copilot is operating might allow attackers to escalate their privileges. This could help them alter deployment settings or access sensitive project configurations that they normally wouldn’t have access to.

## Defense Evasion

**Obfuscated Files or Information (T1027):** To evade detection, attackers might obfuscate scripts or data sources used within AWS Copilot workflows. This can hinder incident response efforts by making it challenging to identify malicious changes in application deployment scripts or configuration files.

## Credential Access

**Cloud Instance Metadata API (T1552.005):** Attackers who gain access to application hosting environments might target the AWS Instance Metadata API to steal temporary credentials. These credentials can be abused to access AWS resources managed by AWS Copilot, enabling unauthorized actions like data exfiltration or configuration changes.

## Discovery

**Cloud Service Discovery (T1580):** Adversaries may explore AWS services integrated with AWS Copilot to identify potential resources, configurations, and security groups that could be further exploited. This can involve reviewing details of deployed applications, pipelines, and connected services to plan subsequent attacks.

## Lateral Movement

**Internal Spearphishing (T1534):** Compromising an account with access to AWS Copilot may give attackers the ability to conduct spearphishing attacks within the organization. They could target other employees with AWS Copilot permissions to expand their control over the cloud infrastructure.

## Collection

**Application Layer Protocol: Web Protocols (T1071.001):** Through compromising AWS Copilot's environment, adversaries could intercept HTTP/HTTPS traffic, gathering sensitive information transferred in application logs, environment variables, or service communications during deployments.

## Command and Control

**Application Layer Protocol: Web Protocols (T1071.001):** An attacker with access may establish command and control channels over common web protocols, blending malicious traffic with regular AWS Copilot communications. This tactic can be used to remotely control compromised services without triggering alarms.

## Impact

**Data Destruction (T1485):** An adversary may exploit AWS Copilot configurations to trigger the deletion or extensive alteration of resources like databases, objects within an S3 bucket, or other critical infrastructure, rendering applications dysfunctional or causing irreversible data loss.

**Service Stop (T1489):** Attackers could stop or disable AWS Copilot-managed services or deployments. This impact tactic can be particularly disruptive, halting business operations and transactions reliant on these services, potentially leading to financial and reputational damage.
