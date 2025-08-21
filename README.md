# Authentication-and-Key-Agreement-Based-on-Anonymous-Identity-for-Peer-to-Peer-Cloud  

## 📑 Contents
- [About the Project](#about-the-project)  
- [How it Works](#how-it-works)  
- [Tech Stack](#tech-stack)  
- [Expected Outcomes](#expected-outcomes)  
- [Future Scope](#future-scope)  
- [Project Status](#project-status)  
- [Team](#team)  
- [Proposed Workflow](#11-proposed-workflow)  
- [PPT](#12-ppt)  
- [Existed Systems](#existed-systems)  
  - [2020 Proposed](#21-existed-system--2020-proposed-)  
  - [2022 Proposed](#22-existed-system--2022-proposed-)  
- [Abstract](#abstract)  
- [Keywords](#keywords)  
- [Technologies Used (Old System)](#technologies-used)  
- [Proposed Tech Stack (2025 Model)](#proposed-tech-stack)  
- [About (Short)](#about-short)  
- [Topics](#topics)  
- [Resources](#resources)  
- [License](#license)  
- [Activity](#activity)  
- [Releases](#releases)  
- [Packages](#packages)  

---

## About the Project
This project focuses on building a secure authentication and key agreement system for peer-to-peer (P2P) cloud environments.  
It uses anonymous identity-based cryptography to protect user privacy while ensuring secure communication.  
By combining **Elliptic Curve Cryptography (ECC)** and **Secure Remote Password (SRP)**, the system enables secure key exchange without exposing real user identities.  

---

## How it Works
Each peer generates an anonymous identity.  
When two peers connect:  
1. They perform mutual authentication using SRP.  
2. A session key is established with ECC-based key exchange.  
3. The session key is used to encrypt communication (**AES-GCM**).  

Supabase provides:  
- **Auth** → for identity management.  
- **Realtime** → for peer-to-peer signaling.  
- **Postgres** → for storing encrypted metadata.  
- **REST APIs** → for secure interaction between frontend and backend.  

---

## Tech Stack
| Component | Usage |
|-----------|-------|
| React.js | Frontend interface for users/peers. |
| Supabase Auth | Authentication & anonymous identity management. |
| Supabase Realtime | Peer-to-peer communication channel for key exchange. |
| Supabase Postgres | Stores metadata and encrypted session data. |
| Supabase REST APIs | Secure communication between frontend & backend. |
| ECC (Elliptic Curve Cryptography) | Lightweight cryptography for key exchange. |
| SRP (Secure Remote Password) | Password-authenticated key agreement. |
| AES-GCM | Session encryption after key establishment. |
| Node.js (optional) | Middleware for advanced crypto operations. |

---

## Expected Outcomes
- Secure authentication in P2P cloud systems.  
- Anonymous identity support for enhanced privacy.  
- Lightweight & efficient cryptographic operations compared to PKI.  
- Scalable for IoT, multi-cloud, and blockchain-based environments.  

---

## Future Scope
- Extend support for multi-cloud environments.  
- Integrate with blockchain for auditability and trust.  
- Optimize for IoT devices with limited resources.  

---

## Project Status
Currently in **initial phase** → Requirement gathering, system design, and stack selection.  
Implementation will focus on **Supabase + ECC + SRP** integration.  

---

## Team
- **Rishi Rohan K** – B.Tech [AIML Dept/2026]  
- **Naveen Nunna** – B.Tech [AIML Dept/2026]  
- **Yashwanth I** – B.Tech [AIML Dept/2026]  
- **Guide/Mentor:** K. Vinay Kumar  

---

## 1.1 Proposed WorkFlow
🔗 [Workflow Diagram](https://excalidraw.com/#json=RW6Gq3XCzuTYczAWhC_dc,KrRYR74FWcuyeC56unqQtg)  

---

## 1.2 PPT
🔗 [Presentation Link](https://www.canva.com/design/DAGwmEsqdf0/d3DhYAAYNvSbJBak_QgfyQ/edit?utm_content=DAGwmEsqdf0&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)  

---

## Existed Systems  

### 2.1 Existed System (2020 Proposed)  
🔗 [Read Paper](https://ieeexplore.ieee.org/document/9123570)  

### 2.2 Existed System (2022 Proposed)  
🔗 [Read Paper](https://www.computer.org/csdl/journal/cc/2022/03/09123570/1kTwDCHSirK)  

---

## Abstract
Peer-to-peer (P2P) cloud systems offer scalability and decentralization but face challenges in secure and private communication.  
This work presents a lightweight authentication and key agreement protocol using **anonymous identities** and **elliptic curve cryptography (ECC)**.  
The scheme enables **mutual authentication** and **secure session key establishment** without revealing real identities, ensuring **confidentiality, integrity, and resistance** to replay, impersonation, and man-in-the-middle attacks.  
Its efficiency makes it suitable for dynamic, resource-constrained P2P cloud environments.  

---

## Keywords
Peer-to-Peer (P2P) Cloud, Authentication, Key Agreement, Anonymous Identity, Elliptic Curve Cryptography (ECC), Privacy  

---

## Technologies Used
- Python  
- MySQL  
- Socket Programming (Comm)  
- Elliptic Curve Cryptography (ECC)  
- Diffie–Hellman Algorithm  
- Anonymous Identity-based Authentication  

---

## Proposed Tech Stack
| Technology / Library | Purpose in Project | Why it is Used |
|----------------------|--------------------|----------------|
| React.js (Frontend) | User Interface for authentication, identity creation, and peer-to-peer session initiation. | Lightweight, fast, widely adopted, great for UI. |
| Supabase Auth | User authentication & identity management. | Serverless auth (email, passwordless, OAuth), supports anonymous identity. |
| Supabase Realtime | Peer-to-peer communication channel. | Low-latency sync between peers. |
| Supabase Postgres | Stores encrypted identities, tokens, metadata. | PostgreSQL + RLS for secure storage. |
| Supabase REST APIs | Secure backend interaction. | Exposes endpoints for session initiation & verification. |
| ECC (JS Library) | Cryptographic key generation & exchange. | Lightweight, secure, better than RSA for cloud. |
| SRP (JS Library) | Password-authenticated key exchange. | Zero-knowledge proof, protects against eavesdropping & replay. |
| AES-GCM (Crypto API) | Session encryption. | Authenticated encryption for secure comms. |
| Node.js (Optional Middleware) | Extra cryptographic logic. | Used if Supabase can’t handle certain crypto ops. |
| Cloud Deployment (Supabase/Vercel/Netlify) | Hosting. | Realistic deployment for cloud-native project. |

---

## About (Short)
🔒 Secure authentication and key agreement protocol using **anonymous identities** for peer-to-peer cloud communication.  

---

## Topics
- UDM  

---

## Resources
- [Readme](#authentication-and-key-agreement-based-on-anonymous-identity-for-peer-to-peer-cloud)  

---

## License
📜 Licensed under **BSL-1.0**.  
See [LICENSE](./LICENSE) for details.  

---

## Activity
- ⭐ Stars: 1  
- 👀 Watchers: 0  
- 🍴 Forks: 0  

---

## Releases
No releases published.  
👉 [Create a new release](../../releases)  

---

## Packages
No packages published.  
👉 [Publish your first package](../../packages)  

---

## Footer
<p align="center">
 🔒 Built with <b>Security, Privacy, and Trust</b> in mind.  
 <br/>Made with ❤️ by <b>Team CKR</b>  
</p>
