**Initial Access - Valid Accounts (T1078):** One of the primary ways adversaries may gain access to Amazon RedShift is via compromised user credentials. This involves obtaining legitimate usernames and passwords through phishing, credential stuffing, or exploiting insufficiently protected credentials. Once the attacker possesses valid credentials, they can log in and access the database cluster, viewing, modifying, or extracting sensitive information.

**Persistence - Valid Accounts (T1078):** After gaining access using valid credentials, adversaries may maintain their foothold using the same accounts. They can ensure persistence by maintaining access to the compromised account or creating additional access mechanisms, such as modifying database roles or permissions to ensure continuous database access even if the original access vector is closed.

**Privilege Escalation - Valid Accounts (T1078):** After obtaining access to RedShift, attackers might seek to escalate privileges to perform actions or execute queries that require higher permissions. This can be achieved by exploiting configuration mistakes where users are inadvertently granted excessive privileges, allowing attackers to execute commands or queries with elevated authorization.

**Defense Evasion - Altered Programming (T1222):** Adversaries may alter stored procedures, functions, or triggers in the RedShift database to perform malicious actions while evading detection. By modifying these database elements, attackers can hide their activities or create backdoors that operate under the guise of normal database functionality.

**Credential Access - Credential Dumping (T1003):** Attackers might attempt to access or "dump" sensitive information from RedShift, like AWS access keys, session tokens, or other credentials stored within the database. This allows adversaries to extend their access beyond RedShift to other AWS resources potentially.

**Discovery - Cloud Service Discovery (T1580):** Adversaries will often perform reconnaissance to gather information about the RedShift cluster, including database instances, roles, users, and permissions. This helps them understand the environment, identify potential targets, and plan subsequent actions.

**Collection - Data from Information Repositories (T1213):** Once the adversaries have access and potentially egress control, they can collect and exfiltrate data stored within RedShift. This might involve exporting entire tables, executing select queries to gather specific data subsets, and storing the collected data in accessible locations.

**Exfiltration - Exfiltration Over Alternative Protocol (T1048):** To avoid detection, adversaries might exfiltrate data using non-standard protocols or novel means, such as using AWS services or APIs that are less monitored. This can help bypass traditional monitoring systems that watch for typical data movement patterns.

**Impact - Data Destruction (T1485):** In some attack scenarios, adversaries may choose to destroy data within RedShift, either as a final act of sabotage after exfiltrating the information or as a means to disrupt business operations. This could involve deleting or truncating database tables, corrupting data, or executing DROP commands to remove critical database structures.
