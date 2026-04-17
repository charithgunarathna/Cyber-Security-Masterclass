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

    🚪 Common Network Ports and Protocols
As a cyber security professional, you must memorize common ports. These are the "doors" through which network communication happens.
Port Number,Protocol,Description,Security Risk / Note
21,FTP,File Transfer Protocol,Data sent in plaintext. Highly vulnerable.
22,SSH,Secure Shell,Secure alternative to Telnet. Used for remote access.
80,HTTP,Hypertext Transfer Protocol,Web traffic in plaintext. Susceptible to sniffing.
443,HTTPS,HTTP Secure,Encrypted web traffic (SSL/TLS).
3389,RDP,Remote Desktop Protocol,Highly targeted by ransomware attackers.

🛡️ Firewalls and Intrusion Detection Systems (IDS)
Network security relies heavily on defense mechanisms.

Firewall: Acts as a barrier between a trusted internal network and an untrusted external network (Internet).

IDS (Intrusion Detection System): Monitors network traffic for suspicious activity and issues alerts.

IPS (Intrusion Prevention System): Similar to IDS, but actively blocks or prevents the detected malicious activity.
🖼️ Network Scanning Concept
<div align="center">
<img src="https://www.google.com/search?q=https://images.unsplash.com/photo-1558494949-ef010cbdcc31%3Fixlib%3Drb-4.0.3%26auto%3Dformat%26fit%3Dcrop%26w%3D800%26q%3D80" alt="Server Room" width="600">


<em>Networks are the backbone of modern infrastructure. Scanning them safely is the first step in ethical hacking.</em>
</div>
📚 Practical Task
Download and install Wireshark.

Capture your own network traffic for 5 minutes.

Try to filter out HTTP and DNS traffic using the search bar.

⬅️ Back to Fundamentals | ➡️ Next Module: Web Security
