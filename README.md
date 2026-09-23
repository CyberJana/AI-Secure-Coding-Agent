🛡️ SecureCode AI

<p align="center">
  <img src="docs/assets/securecode-ai.gif" alt="SecureCode AI Animation" width="900"/>
</p><h3 align="center">
  🤖 AI-Powered Application Security & DevSecOps Platform
</h3><p align="center">
  Detect • Analyze • Prioritize • Remediate • Secure
</p><p align="center">"Python" (https://img.shields.io/badge/Python-3.12-blue?logo=python)
"FastAPI" (https://img.shields.io/badge/FastAPI-Backend-009688?logo=fastapi)
"Next.js" (https://img.shields.io/badge/Next.js-Frontend-black?logo=next.js)
"Docker" (https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker)
"PostgreSQL" (https://img.shields.io/badge/PostgreSQL-Database-4169E1?logo=postgresql)
"Security" (https://img.shields.io/badge/Focus-Cybersecurity-red)
"AI" (https://img.shields.io/badge/AI-Security-purple)

</p>---

⚡ What is SecureCode AI?

SecureCode AI is an open-source application security platform that combines traditional security scanners with AI-assisted vulnerability analysis.

        👨‍💻 Developer
             │
             ▼
       🐙 GitHub Code
             │
             ▼
      ┌──────────────┐
      │ SecureCode AI│
      └──────┬───────┘
             │
      ┌──────┼───────┐
      ▼      ▼       ▼
   🔍 SAST  🔐 Secrets  📦 Dependencies
      │      │       │
      └──────┼───────┘
             ▼
       🧠 AI Analysis
             │
      ┌──────┼───────┐
      ▼      ▼       ▼
   🎯 Risk  CWE    OWASP
   Score   Map     Map
      │      │       │
      └──────┼───────┘
             ▼
       💡 Remediation
             │
             ▼
       🔀 Pull Request
             │
             ▼
        🚀 Secure Code

---

🧠 AI Security Engine

SecureCode AI uses a provider-agnostic architecture.

                 🧠 AI ENGINE
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
   🤖 Mock AI      OpenAI       Anthropic
        │             │             │
        └─────────────┼─────────────┘
                      ▼
                AI Analyzer
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
   Explanation    Risk Analysis   Remediation

The default development provider is Mock AI, so the project can run without an external AI API key.

---

🔍 Security Scanning

Tool| Purpose
🔎 Semgrep| Static security analysis
🔐 Gitleaks| Secret detection
📦 Trivy| Dependency/container scanning
🐍 Bandit| Python security analysis

---

🎯 Vulnerability Intelligence

SecureCode AI transforms raw scanner findings into structured security intelligence.

Vulnerability
      ↓
Severity
      ↓
Risk Score
      ↓
CWE
      ↓
OWASP
      ↓
AI Explanation
      ↓
Remediation

---

📊 Security Dashboard

The platform will provide:

- 🔴 Critical vulnerabilities
- 🟠 High vulnerabilities
- 🟡 Medium vulnerabilities
- 🟢 Low vulnerabilities
- 📈 Security trends
- 📋 Scan history
- 🎯 Risk distribution
- 🧩 CWE analysis
- 🛡️ OWASP analysis

---

🚀 Roadmap

MVP
 │
 ├── ✅ FastAPI
 ├── ✅ Mock AI
 ├── ✅ Bandit
 ├── ✅ Risk Engine
 ├── ✅ CWE Mapping
 └── ✅ OWASP Mapping
        │
        ▼
Security Platform
 │
 ├── 🔲 Semgrep
 ├── 🔲 Gitleaks
 ├── 🔲 Trivy
 ├── 🔲 GitHub Integration
 └── 🔲 PostgreSQL
        │
        ▼
AI DevSecOps
 │
 ├── 🔲 AI Vulnerability Triage
 ├── 🔲 AI Remediation
 ├── 🔲 GitHub PR Comments
 ├── 🔲 CI/CD Security Gates
 └── 🔲 Automated Validation
        │
        ▼
Future
 │
 ├── 🔲 Attack Path Analysis
 ├── 🔲 Threat Intelligence
 ├── 🔲 AI Security Agent
 ├── 🔲 Autonomous Investigation
 └── 🔲 Enterprise Security

---

🐳 Quick Start

git clone https://github.com/CyberJana/securecode-ai.git

cd securecode-ai

cp .env.example .env

docker compose up --build

Backend:

http://localhost:8000

API documentation:

http://localhost:8000/docs

---

🏗️ Architecture

┌────────────────────────────────────────────────────┐
│                  SECURECODE AI                     │
├────────────────────────────────────────────────────┤
│                                                    │
│  GitHub ──► Scanner Layer ──► Risk Engine         │
│                         │             │             │
│                         ▼             ▼             │
│                    Vulnerabilities   CWE/OWASP     │
│                         │             │             │
│                         └──────┬──────┘             │
│                                ▼                    │
│                         🧠 AI Analyzer              │
│                                │                    │
│                    ┌───────────┼───────────┐        │
│                    ▼           ▼           ▼        │
│                Explain      Prioritize   Fix        │
│                    │           │           │        │
│                    └───────────┼───────────┘        │
│                                ▼                    │
│                       Security Dashboard            │
│                                │                    │
│                                ▼                    │
│                         GitHub Pull Request          │
│                                                    │
└────────────────────────────────────────────────────┘

---

🔐 Security Philosophy

«AI assists security professionals — it does not replace security validation.»

SecureCode AI is designed around:

- 🔒 Secure-by-default architecture
- 🧪 Automated testing
- 👨‍💻 Human approval
- 🔐 Secret protection
- 🛡️ Least privilege
- 📋 Auditability
- 🚫 No unrestricted AI code execution

AI-generated remediation should be validated and tested before deployment.

---

🤝 Contributing

Contributions are welcome!

git checkout -b feature/your-feature

git commit -m "feat: add security improvement"

git push origin feature/your-feature

Then open a Pull Request.

---

⚠️ Responsible Use

Only scan source code and systems that you own or have explicit authorization to test.

SecureCode AI is intended for defensive security, secure software development, and authorized security testing.

---

👨‍💻 Author

Janarthanan A

Cybersecurity | Digital Forensics | AI Security | DevSecOps

<p align="center">🛡️ Secure Code. Secure Systems. Secure Future. 🤖

</p>---

<p align="center">
  ⭐ Star the repository if you find the project useful!
</p>