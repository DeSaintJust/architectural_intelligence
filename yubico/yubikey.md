### Phishing (T1566)

The YubiKey, like many other security mechanisms, can be subject to phishing attacks. Threat actors may attempt to deceive users into entering their credentials and YubiKey One-Time Passwords (OTPs) on fake websites that closely mimic legitimate ones. Even though the YubiKey provides additional protection beyond just a password, attackers can capture session-specific OTPs through a convincing phishing attempt, which can then be used to gain unauthorized access within a narrow time window.

### Man-in-the-Middle (T1557)

In a man-in-the-middle attack, a threat actor could potentially intercept communication between the user and the authentication service. If a YubiKey is used for OTP or U2F (Universal 2nd Factor), the attacker could capture these authentication messages. To mitigate this, YubiKey primarily protects against the misuse of such attacks by attaching the user's session to a specific physical device; however, it still does not completely eliminate threats if attackers can manipulate or forward requests before they reach their intended destination.

### Credential Dumping (T1003)

Although YubiKeys themselves are hardware tokens and do not have traditional credentials stored like passwords, credential dumping techniques can still pose a risk in a broader sense. If an adversary gains access to a user's system, they might extract other credentials saved in browsers or applications compromised on the device. They might then combine this information with manipulation tactics to bypass or socially engineer around the necessity of a YubiKey authentication step.

### Supply Chain Compromise (T1195)

A supply chain compromise involving YubiKeys could theoretically occur if an attacker infiltrates the manufacturing or distribution processes. Compromised YubiKeys could have tampered firmware or additional components inserted to capture usage data or OTPs without the user's knowledge. Although stringent security measures are in place by manufacturers like Yubico, the supply chain remains a potential threat vector.

### Hardware Additions (T1200)

Adversaries could use hardware addition techniques to tamper with YubiKeys, especially in situations where they have temporary physical access to the device. This could involve opening the physical token to implant unauthorized chips or RFID sensors to capture tokens or subtler data during its use, though such actions require considerable expertise and target-specific motivation by attackers.

### Side-channel Attacks (T1580)

Side-channel attacks against a YubiKey might exploit physical phenomena like electromagnetic leaks or power signature variations to infer sensitive information as it operates. Although hardware like the YubiKey is designed to counter such attacks, potential vulnerabilities could be exploited by highly skilled adversaries focusing on encryption operations or data processing within the device.

### Exploit Public-Facing Application (T1190)

In this context, a threat actor might target public-facing services that utilize YubiKey authentication to slip past the security mechanisms implemented by the service. For example, abusing application vulnerabilities that are responsible for handling YubiKey validation requests could enable attackers to spoof validation responses, essentially bypassing the security intended by the YubiKey mechanism.
