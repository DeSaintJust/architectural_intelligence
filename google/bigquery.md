### Initial Access
**Phishing: Spearphishing Link**  
Attackers may employ spearphishing tactics to trick a user into clicking on a malicious link, which could grant unauthorized access to the Google Cloud environment. By exploiting trust relationships, adversaries aim to gain initial foothold enabling them to exploit BigQuery services.

### Execution
**Command and Scripting Interpreter: Bash**  
Adversaries might execute unauthorized scripts through Bash, potentially exploiting cloud instance metadata and gaining escalated privileges, allowing access or manipulation of BigQuery datasets.

### Persistence
**Application Layer Protocol: Web Service**  
Attackers could leverage cloud application interfaces that use web services to create backdoors or maintain persistent access after initial compromise. Misconfigured API permissions may enable adversaries to access or alter BigQuery resources.

### Privilege Escalation
**Valid Accounts: Cloud Accounts**  
Adversaries with access to a low-level cloud account could exploit IAM misconfigurations to escalate privileges within the cloud environment, enabling wider access to BigQuery datasets and altering permissions.

### Defense Evasion
**Impair Defenses: Disable Cloud Services Logging**  
An adversary might disable logging features within GCP to avoid detection and maintain access to BigQuery. This tactic can include modifying permissions or settings related to Stackdriver or other logging mechanisms associated with BigQuery.

### Credential Access
**Credential Dumping: Cloud Instance Metadata API**  
Adversaries may attempt to extract sensitive information, such as service account tokens, from BigQuery environments by querying the metadata API of cloud instances. This action could potentially grant them unauthorized access to BigQuery datasets.

### Discovery
**Cloud Infrastructure Discovery: Cloud Service Dashboard**  
Using legitimate user access, adversaries may explore cloud service dashboards looking for BigQuery datasets. Through this technique, they aim to understand the cloud environment and identify valuable information stored in BigQuery.

### Lateral Movement
**Cloud Services: Storage Applications**  
Adversaries could move laterally into BigQuery environments by transferring data across different GCP services such as Cloud Storage to BigQuery. They might leverage compromised service accounts or API keys to facilitate this movement.

### Collection
**Data from Cloud Storage Object**  
Attackers may target data stored in nearby cloud storage (e.g., Google Cloud Storage), which is often integrated with BigQuery. Compromising these storage services could provide access to large datasets intended for analytical processing in BigQuery.

### Exfiltration
**Transfer Data to Cloud Account**  
Adversaries might exfiltrate data from BigQuery by transferring it to an external cloud account. This might be performed using services such as Google Cloud Storage, exploiting permissions or credentials to siphon off datasets.

### Impact
**Data Destruction**  
An attacker with excessive permissions could leverage BigQuery’s interfaces to modify or delete analytical and structured datasets. Such destructive actions might aim to disrupt business operations or conceal unauthorized activities.
