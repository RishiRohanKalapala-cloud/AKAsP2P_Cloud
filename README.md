# Authentication-and-Key-Agreement-Based-on-Anonymous-Identity-for-Peer-to-Peer-Cloud

# Contents

1. [About the Project](#-about-the-project)
2. [How it Works](#-how-it-works)
3. [Tech Stack](#-tech-stack)
4. [Expected Outcomes](#-expected-outcomes)
5. [Future Scope](#-future-scope)
6. [Project Status](#-project-status)
7. [Team](#-team)
8. [Proposed Workflow](#-11-proposed-workflow)
9. [PPT](#-12-ppt)
10. [Existed Systems](#-2-existed-system)
    - [2020 Proposed](#-21-existed-system--2020-proposed-)
    - [2022 Proposed](#-22-existed-system--2022-proposed-)
11. [Abstract](#-abstract)
12. [Keywords](#-keywords)
13. [Technologies Used (Old System)](#-technologies-used)
14. [Proposed Tech Stack (2025 Model)](#-proposed-tech-stack)
15. [About (Short)](#-about)
16. [Topics](#-topics)
17. [Resources](#-resources)
18. [License](#-license)
19. [Activity](#-activity)
20. [Releases](#-releases)
21. [Packages](#-packages)

## About the Project
This project focuses on building a **secure authentication and key agreement system** for **peer-to-peer (P2P) cloud environments**.  
It uses **anonymous identity-based cryptography** to protect user privacy while ensuring secure communication.  
By combining **Elliptic Curve Cryptography (ECC)** and **Secure Remote Password (SRP)**, the system enables secure key exchange without exposing real user identities.

---

## How it Works
1. Each peer generates an **anonymous identity**.
2. When two peers connect:
   - They perform **mutual authentication** using SRP.
   - A **session key** is established with ECC-based key exchange.
3. The session key is used to **encrypt communication** (AES-GCM).
4. Supabase provides:
   - **Auth** → for identity management.
   - **Realtime** → for peer-to-peer signaling.
   - **Postgres** → for storing encrypted metadata.
   - **REST APIs** → for secure interaction between frontend and backend.

---

## Tech Stack
| Component | Usage |
|-----------|-------|
| **React.js** | Frontend interface for users/peers. |
| **Supabase Auth** | Authentication & anonymous identity management. |
| **Supabase Realtime** | Peer-to-peer communication channel for key exchange. |
| **Supabase Postgres** | Stores metadata and encrypted session data. |
| **Supabase REST APIs** | Secure communication between frontend & backend. |
| **ECC (Elliptic Curve Cryptography)** | Lightweight cryptography for key exchange. |
| **SRP (Secure Remote Password)** | Password-authenticated key agreement. |
| **AES-GCM** | Session encryption after key establishment. |
| **Node.js (optional)** | Middleware for advanced crypto operations. |

---

## Expected Outcomes
- Secure authentication in **P2P cloud systems**.  
- **Anonymous identity** support for enhanced privacy.  
- **Lightweight & efficient** cryptographic operations compared to PKI.  
- Scalable for **IoT, multi-cloud, and blockchain-based environments**.  

---

## Future Scope
- Extend support for **multi-cloud environments**.  
- Integrate with **blockchain** for auditability and trust.  
- Optimize for **IoT devices** with limited resources.  

---

## Project Status
Currently in **initial phase** → Requirement gathering, system design, and stack selection.  
Implementation will focus on **Supabase + ECC + SRP integration**.  

---

## Team
- Rishi Rohan K – B.Tech [AIML Dept/2026]
- Naveen Nunna – B.Tech [AIML Dept/2026]
- Yashwanth I – B.Tech [AIML Dept/2026]    
- Guide/Mentor – K.Vinay Kumar  

### 1.1 Proposed WorkFlow
Link : https://excalidraw.com/#json=RW6Gq3XCzuTYczAWhC_dc,KrRYR74FWcuyeC56unqQtg

### 1.2 PPT
Link : https://www.canva.com/design/DAGwmEsqdf0/d3DhYAAYNvSbJBak_QgfyQ/edit?utm_content=DAGwmEsqdf0&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

### 2.1 Existed System ( 2020 proposed )
Link : (https://ieeexplore.ieee.org/document/9123570)

### 2.2 Existed System ( 2022 proposed )
Link : (https://www.computer.org/csdl/journal/cc/2022/03/09123570/1kTwDCHSirK)

## Abstract

Peer-to-peer (P2P) cloud systems offer scalability and decentralization but face
challenges in secure and private communication. This work presents a
lightweight authentication and key agreement protocol using anonymous
identities and elliptic curve cryptography (ECC). The scheme enables mutual
authentication and secure session key establishment without revealing real
identities, ensuring confidentiality, integrity, and resistance to replay,
impersonation, and man-in-the-middle attacks. Its efficiency makes it suitable
for dynamic, resource-constrained P2P cloud environments, enhancing both
privacy and trustworthiness in distributed data sharing.

## Keywords:
Peer-to-Peer (P2P) Cloud, Authentication, Key Agreement, Anonymous
Identity, Elliptic Curve Cryptography (ECC), Privacy

## Technologies used:
Python, MySQL, Socket Programming (Comm), Elliptic Curve Cryptography
(ECC), Diffie–Hellman Algorithm, Anonymous Identity-based Authentication

## Proposed Tech Stack 

| **Technology / Library**                                 | **Purpose in Project**                                                                     | **Why it is Used**                                                                                                                                                                             |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **React.js (Frontend)**                                  | User Interface for authentication, identity creation, and peer-to-peer session initiation. | React is lightweight, fast, and widely adopted. It allows building a **responsive, interactive UI** to demonstrate the authentication & key agreement process clearly.                         |
| **Supabase Auth**                                        | User authentication & identity management.                                                 | Provides **serverless authentication** (email, passwordless, OAuth) and allows customization for **anonymous identity handling**. Replaces traditional PKI with a **simpler, scalable model**. |
| **Supabase Realtime**                                    | Peer-to-peer communication channel for key exchange and signaling.                         | Enables **secure, low-latency data sync** between peers. Suitable for **P2P-style communication** without managing a custom signaling server.                                                  |
| **Supabase Postgres (Database)**                         | Stores encrypted identities, session tokens, metadata of key agreements.                   | PostgreSQL supports **Row-Level Security (RLS)** and policies, ensuring **confidentiality and controlled access** to sensitive user/session data.                                              |
| **Supabase REST / API Calling**                          | Backend interaction for authentication flow and key exchange logic.                        | Exposes endpoints for **secure session initiation & verification**, making integration with frontend + cryptographic layer seamless.                                                           |
| **ECC (Elliptic Curve Cryptography – JS Library)**       | Cryptographic layer for secure key generation and exchange.                                | ECC provides **lightweight yet strong cryptography**, perfect for cloud and P2P environments. Requires fewer resources than RSA but offers **equivalent/better security**.                     |
| **SRP (Secure Remote Password – JS Library)**            | Password-authenticated key exchange (zero-knowledge proof).                                | Ensures **mutual authentication** without revealing passwords. Protects against eavesdropping, replay attacks, and dictionary attacks.                                                         |
| **AES-GCM (JS Crypto API)**                              | Encrypts peer-to-peer session data after key agreement.                                    | Provides **fast, authenticated encryption** to secure actual communication once session keys are established.                                                                                  |
| **Node.js (Optional Backend Middleware)**                | (If needed) to run custom cryptographic logic beyond Supabase’s capabilities.              | Acts as a middle layer where advanced **crypto operations** can be handled securely if not fully supported in Supabase.                                                                        |
| **Cloud Deployment (Supabase Cloud / Vercel / Netlify)** | Hosting the app & backend in the cloud.                                                    | Enables **realistic cloud environment** deployment, aligning with the **peer-to-peer cloud project domain**.                                                                                   |

