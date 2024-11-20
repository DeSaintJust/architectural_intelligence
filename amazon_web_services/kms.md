## Unauthorized Key Use (Credential Access - T1078)
An adversary may gain unauthorized access to AWS KMS keys by obtaining valid credentials of an AWS account where KMS is being used. This may involve stealing access keys, exploiting weak credentials, or compromising IAM accounts with permissions to utilize KMS. Once an attacker has access, they could decrypt data or create plaintext copies of sensitive key material.

## Abuse of Valid Credentials (Privilege Escalation - T1078.003)
This technique involves the misuse of existing, legitimate IAM roles or policies that have been granted excessive permissions on KMS. An attacker with access to such credentials may escalate privileges to manage, rotate, or disable existing keys. By leveraging misconfigured roles, an adversary can perform actions that might not be directly malicious but lead to longer espionage or data compromise.

## Execution Through API (Execution - T1106)
AWS KMS can be targeted by attackers executing unauthorized API calls to perform operations like decrypting data or creating key grants. These calls can bypass other layers of security if logs and monitoring are poorly configured, leading to illegitimate execution of potentially harmful actions.

## Discovery of Key Information (Discovery - T1082)
Adversaries might seek to discover key information by listing available KMS keys through APIs or examining the metadata associated with KMS keys and policies. This helps them identify existing permissions and possible attack vectors related to key usage, which could be exploited further for unauthorized access or decryption of secure information.

## Exfiltration of Encrypted Data (Exfiltration - T1020)
Data encrypted with KMS keys can still be exfiltrated if an attacker gains some level of access. This can occur after an adversary decrypts the data with abused KMS permissions or finds and retrieves cached or residual data that was inadequately protected after KMS processing.

## Resource Hijacking (Impact - T1496)
Resource hijacking involves unauthorized consumption or redirection of resources via compromised KMS permissions or API keys. Attackers can manipulate KMS for cryptographic operations, allowing them to potentially redirect service expenses to the victim’s account or degrade service availability as a form of indirect denial-of-service attack.

## Data Manipulation (Impact - T1565.001)
Adversaries who gain access to KMS-encrypted data and keys may manipulate the data post-decryption. This typically involves altering encrypted data’s integrity, which, when processed by applications relying on its authenticity, could result in corrupted outputs or erroneous actions downstream.

## Denial of Service from Key Management Exploits (Availability Impact - T1499.003)
This technique consists of exploiting AWS KMS to disrupt service availability by altering, disabling, or deleting keys crucial for the operation of applications and services. Without access to necessary keys, encrypted data becomes inaccessible, effectively causing a denial-of-service condition.
