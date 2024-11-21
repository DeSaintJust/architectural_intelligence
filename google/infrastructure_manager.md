## Initial Access

**Valid Accounts (T1078)**: Attackers may compromise valid credentials to gain unauthorized access to the GCP Infrastructure Manager. Techniques such as phishing or brute force attacks may be employed to capture these credentials, allowing adversaries to bypass initial network barriers by mimicking authorized users and escalating their access.

## Execution

**Command and Scripting Interpreter (T1059)**: Once inside the environment, attackers might exploit the command-line interface capabilities provided by GCP to execute malicious scripts or commands. This can include abusing cloud-native tools or deploying scripts in runtime environments to control resources or disrupt operations.

## Persistence

**Cloud Account (T1098)**: Adversaries may attempt to maintain persistent access by creating, modifying, or leveraging service accounts or roles within GCP. By acquiring persistent cloud account entries, attackers ensure long-term access to the cloud infrastructure, even after attempting to eliminate them.

## Privilege Escalation

**Abuse Elevation Control Mechanism: Impersonation (T1531)**: Malicious actors could exploit permissions management within GCP to escalate privileges. By impersonating service accounts or manipulating IAM policies, attackers could gain higher-level access and perform unauthorized actions within the cloud environment.

## Defense Evasion

**Indicator Removal on Host (T1070)**: Attackers may delete or alter logs to remove traces of their activity. In GCP, this could involve tampering with Stackdriver logs or Google Cloud Audit logs, hiding unauthorized access or modifications from security teams monitoring the infrastructure.

## Credential Access

**Unsecured Credentials (T1552)**: Adversaries may target improperly configured or unsecured GCP credentials, such as API keys or service account files stored without proper encryption. By accessing these secrets, attackers can further their reach within the GCP environment or pivot to other services.

## Discovery

**Cloud Service Discovery (T1538)**: Attackers often perform reconnaissance to map out the cloud infrastructure. In the context of GCP, this could involve querying metadata services or API surfaces to gather sensitive information about resources, network configurations, and permissions to understand the environment fully.

## Lateral Movement

**Internal Spearphishing (T1534)**: Threat actors may leverage compromised accounts to conduct spearphishing attacks within the cloud environment. By crafting deceptive communication mimicking legitimate internal correspondence, attackers can trick other users into divulging credentials or executing malicious payloads directly in GCP.

## Impact

**Resource Hijacking (T1496)**: Malicious actors may attempt to hijack GCP resources, such as virtual machines or cloud functions, to mine cryptocurrency or execute other unauthorized computing tasks. This not only impacts resource allocation but could incur significant financial costs for the cloud account holder.
