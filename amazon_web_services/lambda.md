### Initial Access

- **Valid Accounts (T1078):** Attackers may gain unauthorized access to AWS Lambda by using valid credentials. This can happen through phishing campaigns or credential stuffing attacks, particularly if the credentials are cached in the code, misconfigured IAM roles, or leaked due to a lack of environment configuration management. Once inside, they can execute code with the privileges associated with those credentials.

### Execution

- **Command and Scripting Interpreter (T1059):** AWS Lambda functions are executed through supported runtimes like Node.js, Python, or Java. Adversaries can manipulate these runtimes to execute unauthorized commands, especially if they exploit inadequate validation of inputs within the function code.

- **Exploitation for Client Execution (T1203):** AWS Lambda might be targeted using vulnerabilities in its code or dependencies. By exploiting these vulnerabilities, attackers can execute arbitrary code. Using outdated libraries and packages in Lambda functions increases such risks.

### Persistence

- **Event Triggered Execution (T1546):** Lambda functions can be triggered by various AWS services, such as S3 or DynamoDB. Adversaries could manipulate these event triggers by leveraging permissions to configure persistent execution whenever a legitimate event occurs, maintaining their foothold.

### Privilege Escalation

- **Abuse Elevation Control Mechanism (T1548):** Attackers might exploit misconfigurations in Lambda's IAM policies to escalate their privileges. For example, if the Lambda execution role has excessive permissions, attackers might execute actions that were initially out of their scope.

### Defense Evasion

- **Obfuscated Files or Information (T1027):** Adversaries could obfuscate files or scripts running in a Lambda environment to avoid detection through standard monitoring and logging tools. They may use techniques like encoding, encryption, or packing executable contents.

### Credential Access

- **Credentials from Password Stores (T1555):** Attackers may attempt to access environment variables within Lambda to extract sensitive information such as API keys and database credentials that are often stored there to facilitate interactions with other AWS services.

### Discovery

- **Cloud Service Discovery (T1580):** Adversaries might enumerate Lambda functions, their permissions, and event triggers to understand the environment better. This could involve leveraging access to AWS's SDKs or APIs to collect details on deployed functions and associated resources.

### Lateral Movement

- **Remote Services (T1021):** Lateral movement can occur if an attacker leverages a compromised function to interact with other AWS services and resources. They may use a function's permissions to access unauthorized cloud resources or interact with services like EC2 instances or RDS databases.

### Collection

- **Data from Information Repositories (T1213):** Attackers could misuse Lambda to collect data from AWS resources it interacts with, such as reading from S3 buckets or extracting records from databases. Functions with these capabilities may be exploited to gather sensitive data.

### Exfiltration

- **Transfer Data to Cloud Account (T1567):** Adversaries might exploit the function's outbound capabilities to transfer collected data to an external cloud account. This can happen over HTTP/S through API calls or storage services, utilizing the available network access.

### Impact

- **Resource Hijacking (T1496):** AWS Lambda functions can be co-opted into unauthorized cryptocurrency mining operations or to perform other resource-intensive tasks. This hijacking not only impacts billing but also can deplete account-based resource limits, disrupting legitimate AWS service use.
