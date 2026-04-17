# 🌐 Module 02: Network Security

Welcome to Network Security! In this module, we explore how data travels across the internet and how to secure networks against unauthorized access, interception, and disruption.

---

## 🏗️ The OSI Model (Open Systems Interconnection)

Understanding the OSI model is crucial for troubleshooting and identifying where a cyber attack is taking place.

```mermaid
graph BT;
    L1[Layer 1: Physical] --> L2[Layer 2: Data Link];
    L2 --> L3[Layer 3: Network];
    L3 --> L4[Layer 4: Transport];
    L4 --> L5[Layer 5: Session];
    L5 --> L6[Layer 6: Presentation];
    L6 --> L7[Layer 7: Application];

    style L1 fill:#e63946,stroke:#fff,stroke-width:2px,color:#fff
    style L3 fill:#457b9d,stroke:#fff,stroke-width:2px,color:#fff
    style L4 fill:#1d3557,stroke:#fff,stroke-width:2px,color:#fff
    style L7 fill:#2a9d8f,stroke:#fff,stroke-width:2px,color:#fff
🚪 Common Network Ports and ProtocolsAs a cyber security professional, you must memorize common ports. These are the "doors" through which network communication happens.Port NumberProtocolDescriptionSecurity Risk / Note21FTPFile Transfer ProtocolData sent in plaintext. Highly vulnerable.22SSHSecure ShellSecure alternative to Telnet. Used for remote access.80HTTPHypertext Transfer ProtocolWeb traffic in plaintext. Susceptible to sniffing.443HTTPSHTTP SecureEncrypted web traffic (SSL/TLS).3389RDPRemote Desktop ProtocolHighly targeted by ransomware attackers.🛡️ Firewalls and Intrusion Detection Systems (IDS)Network security relies heavily on defense mechanisms.Firewall: Acts as a barrier between a trusted internal network and an untrusted external network (Internet).IDS (Intrusion Detection System): Monitors network traffic for suspicious activity and issues alerts.IPS (Intrusion Prevention System): Similar to IDS, but actively blocks or prevents the detected malicious activity.🖼️ Network Scanning Concept<div align="center"><img src="https://www.google.com/search?q=https://images.unsplash.com/photo-1558494949-ef010cbdcc31%3Fixlib%3Drb-4.0.3%26auto%3Dformat%26fit%3Dcrop%26w%3D800%26q%3D80" alt="Server Room" width="600"><em>Networks are the backbone of modern infrastructure. Scanning them safely is the first step in ethical hacking.</em></div>📚 Practical TaskDownload and install Wireshark.Capture your own network traffic for 5 minutes.Try to filter out HTTP and DNS traffic using the search bar.⬅️ Back to Fundamentals | ➡️ Next Module: Web Security
---

### 2. තුන්වන ෆෝල්ඩර් එකට (`03-Web-Application-Security/README.md`)
දැන් ඔයාගේ `03-Web-Application-Security` ෆෝල්ඩර් එකේ තියෙන `README.md` එක Edit කරලා මේක සම්පූර්ණයෙන්ම Paste කරන්න.

```markdown
# 🕸️ Module 03: Web Application Security

Web applications are the most common attack surface for modern hackers. In this module, we will learn about the **OWASP Top 10** and how attackers exploit web vulnerabilities.

---

## 🎯 OWASP Top 10 (Critical Vulnerabilities)

The Open Web Application Security Project (OWASP) releases a list of the most critical security risks to web applications. Here are the top three you must know:

| Vulnerability | How it Works | Prevention Strategy |
| :--- | :--- | :--- |
| **A01: Broken Access Control** | Users can act outside of their intended permissions (e.g., standard user accessing admin panel). | Implement role-based access control (RBAC) and strict server-side validation. |
| **A03: Injection (SQLi)** | Untrusted data is sent to an interpreter as part of a command or query. | Use Prepared Statements (Parameterized Queries). |
| **A07: Identification and Auth Failures** | Flaws in login mechanisms, session management, or weak passwords. | Implement Multi-Factor Authentication (MFA) and secure session cookies. |

---

## 💥 How an SQL Injection (SQLi) Attack Works

An attacker manipulates input fields to run unauthorized database queries.

```mermaid
sequenceDiagram
    participant Attacker
    participant WebServer
    participant Database

    Attacker->>WebServer: Enters payload: ' OR 1=1 --
    WebServer->>Database: Query: SELECT * FROM users WHERE user='' OR 1=1 --'
    Note right of Database: The condition 1=1 is always TRUE.
    Database-->>WebServer: Returns all user data!
    WebServer-->>Attacker: Displays unauthorized sensitive data.
⚔️ Introduction to Cross-Site Scripting (XSS)XSS occurs when an application includes untrusted data in a web page without proper validation or escaping.Reflected XSS: The malicious script is bounced off a web server (e.g., via a malicious link).Stored XSS: The payload is permanently stored on the target servers (e.g., in a forum post or comment section).DOM-based XSS: The vulnerability is in the client-side code rather than the server-side code.🛠️ Essential Web Security Tool: Burp Suite<div align="center"><img src="https://www.google.com/search?q=https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5%3Fixlib%3Drb-4.0.3%26auto%3Dformat%26fit%3Dcrop%26w%3D800%26q%3D80" alt="Matrix Code" width="600"><em>Burp Suite allows you to intercept and modify web requests before they reach the server.</em></div>📚 Practical TaskSet up an account on TryHackMe or HackTheBox.Complete a beginner room on SQL Injection.Learn to configure Burp Suite with your web browser (FoxyProxy is highly recommended).⬅️ Back to Network Security | ➡️ Next Module: Ethical Hacking Labs.
