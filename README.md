# EL_Q1_2K26_CS_Task_1
task 1 repo

1. CIA Triad (Confidentiality, Integrity, Availability)
Confidentiality: Ensuring data is accessible only to authorized parties. Example: Bank account
details must remain readable only by the account owner and the bank.
Integrity: Ensuring data is correct and unaltered. Example: A transaction amount must not be
tampered with in transit or at rest.
Availability: Ensuring systems and data are available when needed. Example: Online banking
should be reachable during business hours — DDoS can impact availability.


2. Types of Attackers (Motivations & Examples)
• Script Kiddies — inexperienced attackers using existing tools; motivation: curiosity, vandalism.
• Insiders — employees or contractors with legitimate access; motivation: financial gain, revenge,
coercion.
• Hacktivists — politically or socially motivated attackers targeting organizations to make a
statement.
• Cybercriminals — financially motivated; use ransomware, theft of payment data, credential
stuffing.
• Nation-State Actors / APTs — highly resourced, long-term campaigns for espionage or
sabotage.
• Competitors or Industrial Spies — steal IP or sabotage systems for business advantage.



3. Common Attack Surfaces
• Web Applications — login pages, forms, file uploads (e.g., SQLi, XSS).
• Mobile Apps — insecure storage, improper cert validation, IPC weaknesses.
• APIs — exposed endpoints, broken auth, rate limiting issues.
• Networks — open ports, weak Wi■Fi encryption, misconfigured firewalls.
• Cloud Infrastructure — misconfigured storage (S3 buckets), excessive permissions, insecure
IAM.
• Endpoints — user devices (laptops, phones) with malware risk.
• IoT Devices — weak defaults, outdated firmware.
• Third-Party / Supply Chain — libraries, SDKs, and services that introduce vulnerabilities.



4. OWASP Top 10 (Why it matters)
The OWASP Top 10 lists the most critical web application security risks. It is widely used as a
baseline for secure coding, testing, and audits. Examples of entries: Injection, Broken
Authentication, Sensitive Data Exposure, XML External Entities (XXE), Broken Access Control,
Security Misconfiguration, Cross-Site Scripting (XSS), Insecure Deserialization, Using
Components with Known Vulnerabilities, Insufficient Logging & Monitoring.



5. Mapping Daily Apps to Attack Surfaces (examples)
• Email (Gmail): Client-side phishing, malicious attachments (endpoint), MITM if network
untrusted, OAuth token theft via malicious app.
• WhatsApp / Messaging: Mobile app vulnerabilities, social engineering, backups stored
unencrypted on cloud.
• Banking Apps: Mobile app logic flaws, insecure backend APIs, broken authentication, session
fixation.
• Social Media: OAuth misuse, third-party apps, XSS via user content, account takeover via
weak passwords.


6. Typical Data Flow and Attack Points
Data flow: User → Client (browser/app) → Network → Server/API → Database → Third-party
services
• Client: XSS, compromised device, insecure local storage.
• Network (in transit): MITM, sniffing, inadequate TLS configuration.
• Server/API: SQL Injection, broken authentication/authorization, insecure deserialization.
• Database (at rest): Unencrypted sensitive data, SQLi leading to data exfiltration.
• Third-party: Malicious or vulnerable libraries, compromised CDNs or SDKs.



7. Practical Mitigations (high level)
• Use strong authentication (MFA), principle of least privilege, and secure session handling.
• Validate and sanitize all inputs, use parameterized queries to prevent injection.
• Encrypt data in transit (TLS) and at rest using strong algorithms and proper key management.
• Perform regular vulnerability scanning, dependency checks, and update third-party
components.
• Implement logging, monitoring, and an incident response plan; practice backups and disaster
recovery.
• Harden configurations for cloud and network resources; use WAFs where appropriate.
• Secure SDLC: code reviews, threat modeling, secure coding training, and security testing
(DAST/SAST).

