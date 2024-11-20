### Execution: Native API (T1106)
Attackers may exploit AWS CodeBuild's capability to execute build scripts by injecting malicious commands into buildspec files. These scripts are used to specify the commands required to build the project. An attacker with write access to the buildspec or the environment can potentially insert harmful commands or PowerShell scripts, leading to unauthorized execution and compromising the build environment.

### Persistence: Account Manipulation (T1098)
AWS CodeBuild interacts with AWS services through the use of IAM roles and policies. An attacker who gains access to IAM credentials with the appropriate permissions may modify a build project or even create a new one to introduce malicious code or adjustments. This can lead to persistent threats as the attacker remains embedded in the build process.

### Privilege Escalation: Service Exploitation (T1583)
AWS CodeBuild itself runs under specific service roles that can sometimes have more permissions than necessary. If an attacker gains access to an over-permissioned role, they can exploit this to escalate privileges, gaining access to other AWS resources beyond the CodeBuild project, potentially compromising the entire AWS environment.

### Defense Evasion: Obfuscated Files or Information (T1027)
Attackers might camouflage their activity within CodeBuild by obfuscating the malicious payloads in build scripts. Techniques such as encoding, encryption, or use of alias commands can hide harmful commands from simple scrutiny, making it difficult for security systems and human reviewers to quickly detect and respond to these threats.

### Impact: Data Manipulation (T1565)
Implementing code integrity checks within CodeBuild is essential, as attackers can manipulate application source code within the build process. They might alter version control systems or directly change code files within CodeBuild projects to introduce vulnerabilities or backdoors into the final product, compromising the software integrity and security.

### Impact: Resource Hijacking (T1496)
AWS CodeBuild can be leveraged for unauthorized cryptocurrency mining or other forms of resource exploitation if an attacker injects resource-intensive scripts into build processes. By abusing the AWS resources allocated for legitimate builds, attackers can perform illicit activities without detection initially, increasing operational costs and impairing performance.

### Initial Access: Valid Accounts (T1078)
Compromised credentials pose a significant risk to AWS CodeBuild environments. If an attacker gains access to valid AWS credentials with permissions to manage CodeBuild projects, they can manipulate ongoing builds, access sensitive data, and potentially pivot to other parts of the AWS infrastructure, establishing a foothold in the network.

### Collection: Data from Network Shared Drive (T1039)
AWS CodeBuild projects often require access to shared resources such as source code repositories and artifacts stored in places like Amazon S3 or EBS. Attackers who compromise CodeBuild can leverage this connection to collect, copy, or tamper with sensitive data that resides in these network-attached storage locations, potentially leading to data breaches.
