# Authentication-and-Key-Agreement-Based-on-Anonymous-Identity-for-Peer-to-Peer-Cloud

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

