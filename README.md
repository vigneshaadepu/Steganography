<div align="center">

  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=36&pause=1000&color=00F2FE&center=true&vcenter=true&width=650&height=70&lines=S+T+E+G;Secure+Steganographic+System;AES-256+%2B+LSB+Pixel+Embedding;Zero-Trace+Cyber-Vault" alt="STEG Banner Animation" />

  <h3>🛡️ Next-Generation Steganographic Cyber-Vault & Encrypted Communication Portal</h3>

  <p align="center">
    <strong>Invisible Data Embedding &bull; AES-256 Encryption &bull; Bcrypt Vault Protection &bull; One-Click Cryptographic Purge</strong>
  </p>

  <p align="center">
    <a href="https://python.org"><img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.8+"></a>
    <a href="https://flask.palletsprojects.com/"><img src="https://img.shields.io/badge/Backend-Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask"></a>
    <a href="https://pycryptodome.readthedocs.io/"><img src="https://img.shields.io/badge/Crypto-AES--256-00F2FE?style=for-the-badge&logo=letsencrypt&logoColor=black" alt="AES-256"></a>
    <a href="https://pillow.readthedocs.io/"><img src="https://img.shields.io/badge/Stego-LSB%20RGB-FF2A6D?style=for-the-badge&logo=image&logoColor=white" alt="LSB Steganography"></a>
    <a href="https://sqlite.org/"><img src="https://img.shields.io/badge/Database-SQLite3-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite"></a>
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-05D54B?style=for-the-badge" alt="License"></a>
  </p>

  <p align="center">
    <a href="#-key-features"><b>Key Features</b></a> &bull;
    <a href="#-system-architecture"><b>Architecture</b></a> &bull;
    <a href="#-tech-stack"><b>Tech Stack</b></a> &bull;
    <a href="#-repository-structure"><b>Repository Structure</b></a> &bull;
    <a href="#-quick-start"><b>Quick Start</b></a> &bull;
    <a href="#-security-specifications"><b>Security Specs</b></a>
  </p>

  <hr width="100%" size="1" color="#1F2937" />
</div>

<br />

## 🌟 Executive Overview

**STEG** is a flagship high-integrity security suite engineered for ultra-confidential data transmission. By synergizing **AES-256 symmetric cipher encryption** with **24-bit RGB Least Significant Bit (LSB) steganography**, STEG transforms ordinary image files into cryptographically sealed, visually indistinguishable data carriers. 

Even if an image carrier is intercepted by unauthorized entities, the payload remains double-shielded—imperceptible to manual visual analysis and cryptographically unbreakable without the private decryption key.

<div align="center">

| Security Layer | Defense Mechanism | Cryptographic Principle | Target Threat |
| :--- | :--- | :--- | :--- |
| **Layer 1: Confidentiality** | AES-256 Payload Cipher | Symmetric Key Derivation | Unauthorized Data Extraction |
| **Layer 2: Invisibility** | Spatial LSB Pixel Shading | RGB Color Channel Modification | Statistical & Visual Detection |
| **Layer 3: Access Control** | Bcrypt Vault Passwords | Salted Work-Factor Hashing | Unauthorized Vault Access |
| **Layer 4: Erasure** | One-Click Purge Pipeline | Instant File & DB Record Shredding | Data Persistence Risks |

</div>

<br />

---

## ⚡ Key Features

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3 align="left">🔐 Dual-Layer Defense Architecture</h3>
      <p>Messages undergo AES-256 encryption using a user-specified key prior to spatial embedding, guaranteeing payload privacy even if steganographic algorithms are inspected.</p>
    </td>
    <td width="50%" valign="top">
      <h3 align="left">👁️‍🗨️ Zero-Distortion LSB Embedding</h3>
      <p>Utilizes Least Significant Bit manipulation across RGB image channels. Alters pixel values by microscopic amounts to maintain zero perceptual quality loss.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3 align="left">🛡️ Bcrypt Cyber-Vault Portal</h3>
      <p>Access to encoded assets is protected by <code>bcrypt</code> hashed access credentials. Database records contain zero plaintext secret keys or passwords.</p>
    </td>
    <td width="50%" valign="top">
      <h3 align="left">🌫️ Privacy-Blurred Decode Gateway</h3>
      <p>Decryption portal features client-side privacy blur layers, requiring multi-factor authentication steps (Vault Password + Decryption Key) to unveil data.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3 align="left">📊 Interactive Asset Dashboard</h3>
      <p>Futuristic cyber-vault console for managing steganographic assets, tracking creation dates, and viewing real-time asset metrics powered by Chart.js.</p>
    </td>
    <td width="50%" valign="top">
      <h3 align="left">💥 Cryptographic One-Click Purge</h3>
      <p>Execute immediate, irreversible removal of carrier image files and SQLite relational records upon completing sensitive communications.</p>
    </td>
  </tr>
</table>

<br />

---

## 🏗️ System Architecture & Workflow

```mermaid
flowchart TD
    %% Styling Node Definitions
    classDef client fill:#0d1117,stroke:#00F2FE,stroke-width:2px,color:#fff;
    classDef crypto fill:#0d1117,stroke:#FF2A6D,stroke-width:2px,color:#fff;
    classDef stego fill:#0d1117,stroke:#05D54B,stroke-width:2px,color:#fff;
    classDef db fill:#0d1117,stroke:#FFC107,stroke-width:2px,color:#fff;

    subgraph ENCODE_PIPELINE ["🔒 1. Encoding & Embedding Pipeline"]
        A[Plaintext Secret Message] ::: client --> B[AES-256 Encryption Engine] ::: crypto
        K1[Encryption Password] ::: crypto --> B
        B --> C[Encrypted Cipher Text Payload] ::: crypto
        D[Original Carrier Image] ::: stego --> E[LSB Spatial Domain Embedder] ::: stego
        C --> E
        E --> F[Encoded Stego Image File] ::: stego
        P1[Vault Access Password] ::: client --> G[Bcrypt Hash Generator] ::: crypto
        G --> H[(SQLite Database Record)] ::: db
        F --> H
    end

    subgraph DECODE_PIPELINE ["🔑 2. Vault Access & Extraction Pipeline"]
        I[User Requests Vault Asset] ::: client --> J[Bcrypt Vault Authentication] ::: crypto
        J -->|Access Granted| L[Privacy-Blur Extraction Portal] ::: client
        L --> M[LSB Spatial Domain Extractor] ::: stego
        F --> M
        M --> N[Extracted Cipher Text] ::: crypto
        N --> O[AES-256 Decryption Engine] ::: crypto
        K2[Decryption Key Input] ::: client --> O
        O --> P[Original Unveiled Secret Message] ::: client
    end
```

<br />

---

## 🛠️ Tech Stack & Engineering Specs

<div align="center">

| Category | Technology | Usage & Purpose |
| :--- | :--- | :--- |
| **Backend Engine** | <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" /> | Core micro-framework handling server routing, payload processing, and asset lifecycle |
| **Cryptography** | <img src="https://img.shields.io/badge/PyCryptodome-00F2FE?style=flat-square&logo=letsencrypt&logoColor=black" /> <img src="https://img.shields.io/badge/Bcrypt-FF2A6D?style=flat-square&logo=auth0&logoColor=white" /> | High-performance AES-256 symmetric encryption and salted password hashing |
| **Image Processing** | <img src="https://img.shields.io/badge/Pillow_(PIL)-05D54B?style=flat-square&logo=image&logoColor=white" /> | Spatial domain pixel buffer manipulation for 24-bit RGB LSB steganography |
| **Database** | <img src="https://img.shields.io/badge/SQLite3-003B57?style=flat-square&logo=sqlite&logoColor=white" /> | Relational data persistence for asset metadata, hashed access keys, and cipher pointers |
| **Frontend UI/UX** | <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" /> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" /> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" /> | Custom Cyberpunk Glassmorphism UI with responsive design tokens |
| **Visuals & UX** | <img src="https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white" /> <img src="https://img.shields.io/badge/AOS.js-00D2FF?style=flat-square" /> <img src="https://img.shields.io/badge/SweetAlert2-7066E0?style=flat-square" /> | Dynamic interactive charts, scroll animations, and context-aware alerts |

</div>

<br />

---

## 📂 Repository Structure

```gcode
STEG/
├── 📄 app.py                  # Core Flask Application Server & Route Handlers
├── 📄 config.py               # Application Constants & Directory Configurations
├── 📄 requirements.txt        # Python Dependency Manifest
├── 📄 cleanup_db.py           # Utility Script for Database Maintenance
│
├── 📁 auth/                   # Authentication & Security Module
│   └── 📄 password_utils.py   # Bcrypt Hashing & Password Verification Logic
│
├── 📁 crypto/                 # Cryptographic Processing Engine
│   ├── 📄 encrypt.py          # AES-256 Message Encryption Handler
│   └── 📄 decrypt.py          # AES-256 Message Decryption Handler
│
├── 📁 stego/                  # Steganographic Processing Module
│   ├── 📄 embed.py            # LSB Image Embedding Algorithm
│   └── 📄 extract.py          # LSB Image Extraction Algorithm
│
├── 📁 database/               # Data Persistence Layer
│   ├── 📄 db.py               # SQLite Connection Provider
│   ├── 📄 init_db.py          # Database Schema Initialization Script
│   ├── 📄 models.py            # Schema Definitions (Images & Messages)
│   └── 📄 steg.db             # Local Relational Database Storage
│
├── 📁 templates/              # Glassmorphism HTML5 Views
│   ├── 📄 base.html           # Master Layout Template
│   ├── 📄 index.html          # Portal Landing Page
│   ├── 📄 encode.html         # Data Encoding Portal
│   ├── 📄 dashboard.html      # Asset Management Vault
│   ├── 📄 access.html         # Vault Access Guard
│   └── 📄 decode.html         # Privacy Blur Decryption Portal
│
└── 📁 static/                 # Static Assets & Styling System
    ├── 📁 css/                # Custom Glassmorphism Stylesheets
    ├── 📁 js/                 # Client-side Scripts & Integrations
    ├── 📁 img/                # UI Graphical Assets
    └── 📁 uploads/            # Encoded & Original Image Repositories
```

<br />

---

## 🚀 Quick Start & Execution

### 1. Prerequisites
Ensure **Python 3.8+** is installed on your local environment.

### 2. Installation & Virtual Environment
```bash
# Clone the repository
git clone https://github.com/vigneshaadepu/Steganography.git
cd Steganography

# Create and activate a virtual environment (Recommended)
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install required dependencies
pip install -r requirements.txt
```

### 3. Initialize Database
Initialize the SQLite storage schema:
```bash
python database/init_db.py
```

### 4. Launch Application
Start the local development server:
```bash
python app.py
```
Open your browser and navigate to **`http://127.0.0.1:5000`**.

<br />

---

## 🔬 Cryptographic & Security Specifications

<div align="center">

```
================================================================================
  SPECIFICATION KEY         |  IMPLEMENTATION DETAILS
================================================================================
  Encryption Standard       |  AES-256 (Advanced Encryption Standard)
  Cipher Mode               |  PyCryptodome Symmetric Block Cipher
  Steganographic Method     |  Least Significant Bit (LSB) 24-bit RGB Channel
  Key Storage               |  Zero-Knowledge (Keys are never saved to disk/DB)
  Vault Access Hashing      |  Bcrypt Salted Password Hashing
  Image Carrier Integrity   |  100% Visual Fidelity (Zero Perceptible Distortion)
  Asset Destruction         |  Cryptographic File & DB Record Shredding
================================================================================
```

</div>

<br />

---

<div align="center">

  <hr width="100%" size="1" color="#1F2937" />

  <p align="center">
    <strong>STEG | Secure Steganographic Communication System</strong>
  </p>

  <p align="center">
    <a href="#top">⬆ Back to Top</a>
  </p>

  <p align="center">
    <sub>Developed with precision by <strong>Antigravity AI</strong> &bull; Released under the MIT License</sub>
  </p>

</div>
