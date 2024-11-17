### Credential Dumping (T1003)

Credential dumping is a technique where attackers attempt to extract credentials from a system to gain unauthorized access. In the context of Azure Cosmos DB, attackers might target storage accounts, virtual machines, or other resources to obtain credentials that allow privileged access. They could potentially use tools or scripts to capture sensitive authentication tokens or keys stored in improperly secured configurations. Mitigations include stringent access controls, regular credential rotations, and monitoring for unusual access patterns.

### Cloud Instance Metadata API (T1552.005)

Threat actors may attempt to exploit the Cloud Instance Metadata API to gather sensitive information from virtual machines associated with Azure services. This information can include tokens or access keys that provide privileges to access Azure Cosmos DB. Configuring restricted access to metadata endpoints and using role-based access controls are prudent methods to protect against such exploitation.

### Account Manipulation (T1098)

Account manipulation involves altering existing accounts to impede legitimate access and grant unauthorized access. Attackers with insider knowledge or compromised accounts can exploit account settings associated with Azure Cosmos DB services to escalate privileges or to maintain persistence. Regular audits of user permissions and employing multi-factor authentication can mitigate these risks.

### Valid Accounts (T1078)

Attackers using valid but compromised accounts can gain illicit access to Azure Cosmos DB. This could happen through phishing attacks, password cracking, or social engineering. Once inside, attackers may exploit the permissions of these accounts to query databases or extract data. Monitoring access logs and implementing strong password policies help in mitigating this threat.

### Exfiltration Over Web Service (T1567)

Threat actors might exfiltrate data directly from Azure Cosmos DB by exploiting API endpoints or legitimate web services that rely on database information. They can mask their activities under normal web traffic to evade detection. Ensuring API logic requires authentication, rate-limiting requests, and auditing access logs are crucial steps for identifying and containing such threats.

### Query Parameter Poisoning (T1190: SQL Injection)

Azure Cosmos DB is vulnerable to query parameter poisoning, akin to SQL injection in traditional databases. Attackers may craft malicious queries to manipulate database operations, read data, or escalate access privileges. Secure coding practices that include input validation and parameterized queries are essential safeguards to prevent such attacks.

### DoS: Resource Exhaustion (T1499)

A Denial-of-Service attack can target Azure Cosmos DB by exhausting its allocated resources, resulting in service downtime or degraded performance. This approach may involve flooding the database with requests to consume processing power and throughput. Implementing network-level rate limiting, configuring alerts for unusual use patterns, and adjusting auto-scaling resources help mitigate resource exhaustion threats.

### Data Destruction (T1485)

Threat actors may engage in data destruction to damage data integrity and availability within Azure Cosmos DB. This can happen through direct data deletions, overwriting configurations, or altering business-resilient settings such as backups and replica configurations. Regularization of backups, implementing role-based access controls, and anomaly detection help prevent and recover from destructive actions.

### Sensitive Data Exposure (T1530)

Sensitive data stored in Azure Cosmos DB can be exposed inadvertently through unsecured network configurations or improper access policies. Attackers may exploit these weaknesses to access PII (Personally Identifiable Information) or business-critical data. Encryption of data at rest and transit, along with rigorous access logging, can safeguard against such exposure.
