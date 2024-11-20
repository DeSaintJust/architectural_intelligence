### Initial Access: Valid Accounts (T1078)

Threat actors may attempt to gain initial access to AWS environments by compromising valid AWS accounts. If an adversary obtains credentials with permissions to operate AWS CloudFormation, they can create, manipulate, or delete cloud resources by executing scripts or using the AWS Management Console. This access could lead to unauthorized provisioning or modifications of the infrastructure, which might serve as a foothold for more advanced attacks.

### Execution: Exploitation of Remote Services (T1210)

An attacker may exploit vulnerabilities in an associated service in AWS that has been deployed via CloudFormation. Once they gain access through a vulnerable component, they can use CloudFormation stack permissions to modify or extend their reach within the cloud environment. This tactic might be used to inject malicious configurations or deploy additional resources under the attacker's control.

### Persistence: Account Manipulation (T1098)

After gaining access, adversaries could modify user accounts, roles, or security group settings in AWS CloudFormation to maintain persistent access to the environment. By altering IAM policies associated with AWS CloudFormation stacks, attackers could ensure they have the necessary privileges to consistently return to the environment, even if their initial method of access is discovered and mitigated.

### Privilege Escalation: Abuse Elevation Control Mechanism (T1548)

Threat actors may exploit AWS CloudFormation by manipulating stack templates to escalate privileges within the AWS environment. For example, they could alter IAM roles and permissions included in a CloudFormation template to gain administrative access to other resources or services, leading to an expansion of control and impact across the cloud infrastructure.

### Defense Evasion: Impair Defenses (T1562)

Attackers might use AWS CloudFormation to disable security features or logging mechanisms. By modifying stack configurations, they could disable AWS Config, CloudTrail, or other monitoring and alerting tools, making it easier to perform malicious actions without detection. Such impairment of defenses allows attackers to maintain a low profile while they perform recon or data exfiltration.

### Credential Access: Valid Accounts (T1078)

CloudFormation scripts and templates often contain sensitive data, such as IAM roles, policies, and ARNs. If an attacker successfully accesses or manipulates these elements, they might gain access to valid account credentials or roles. This breach could allow them to perform unauthorized actions under the guise of legitimate users, leading to potential exploitation across the environment.

### Discovery: Cloud Service Discovery (T1580)

Adversaries may leverage AWS CloudFormation to gain detailed insights into the cloud environment. By querying CloudFormation stacks and templates, they can discover the architecture, resources, and configurations in use. This information can help attackers map out the infrastructure and identify potential weaknesses or targets for their attack operations.

### Impact: Resource Hijacking (T1496)

AWS CloudFormation can be used by attackers to deploy unauthorized resources that consume compute, storage, or networking capabilities, leading to resource hijacking. By adding malicious resources through CloudFormation, adversaries can incur costs to the victim organization or use resources for crypto mining and other unauthorized operations, resulting in financial and performance impacts.
