🛡️ SecureCode AI

AI-Powered Application Security & Secure Coding Platform

SecureCode AI is an open-source cybersecurity platform designed to help developers identify, understand, prioritize, and remediate security vulnerabilities in their source code.

It combines SAST, secret detection, dependency scanning, AI-assisted vulnerability analysis, CWE/OWASP mapping, and security reporting into a single developer-friendly platform.

---

🚀 Features

- 🔍 Static Application Security Testing (SAST)
- 🤖 AI-powered vulnerability analysis
- 🔐 Secret and credential detection
- 📦 Dependency vulnerability scanning
- 🐍 Python security analysis with Bandit
- 🧩 CWE classification
- 🛡️ OWASP vulnerability mapping
- 📊 Security risk scoring
- 📈 Security dashboard
- 📝 Automated vulnerability explanations
- 💡 AI-generated remediation recommendations
- 🐙 GitHub repository integration
- 🔄 CI/CD security scanning
- 📄 Security report generation
- 🐳 Docker-based deployment
- 🔌 Provider-agnostic LLM architecture

---

🏗️ Architecture

                         ┌──────────────────────┐
                         │   GitHub Repository  │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │    SecureCode AI     │
                         └──────────┬───────────┘
                                    │
                ┌───────────────────┼───────────────────┐
                │                   │                   │
                ▼                   ▼                   ▼
          ┌──────────┐        ┌──────────┐       ┌──────────┐
          │ Semgrep  │        │ Gitleaks │       │  Trivy   │
          └────┬─────┘        └────┬─────┘       └────┬─────┘
               │                   │                  │
               └───────────────────┼──────────────────┘
                                   ▼
                         ┌──────────────────────┐
                         │ Vulnerability Engine │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │     Risk Engine      │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │    AI Analyzer       │
                         └──────────┬───────────┘
                                    │
                     ┌──────────────┼──────────────┐
                     ▼              ▼              ▼
                Explanation      CWE/OWASP     Remediation
                     │              │              │
                     └──────────────┼──────────────┘
                                    ▼
                         ┌──────────────────────┐
                         │ Security Dashboard   │
                         └──────────────────────┘

---

🧠 AI Architecture

SecureCode AI uses a provider-agnostic AI abstraction.

                    LLM Provider Interface
                             │
          ┌──────────────────┼──────────────────┐
          │                  │                  │
          ▼                  ▼                  ▼
    Mock Provider       OpenAI Provider   Anthropic Provider
          │                  │                  │
          └──────────────────┼──────────────────┘
                             │
                             ▼
                       AI Analyzer

The Mock Provider is the default, allowing the project to run without an external AI API key.

Future providers can be added without changing the application's core security logic.

---

🛠️ Technology Stack

Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS

Backend

- Python
- FastAPI
- Pydantic
- SQLAlchemy

Security

- Semgrep
- Gitleaks
- Trivy
- Bandit

AI

- Provider-agnostic LLM interface
- Mock AI provider
- OpenAI-compatible provider
- Anthropic-compatible provider
- Local-model support planned

Database

- PostgreSQL

DevOps

- Docker
- Docker Compose
- GitHub Actions

---

📂 Project Structure

securecode-ai/
│
├── frontend/
│   ├── app/
│   ├── components/
│   └── lib/
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── ai/
│   │   ├── database/
│   │   ├── github/
│   │   ├── models/
│   │   ├── scanners/
│   │   ├── security/
│   │   └── services/
│   │
│   ├── requirements.txt
│   └── Dockerfile
│
├── database/
│   └── schema.sql
│
├── scanners/
│   ├── semgrep/
│   ├── gitleaks/
│   └── trivy/
│
├── tests/
│
├── .github/
│   └── workflows/
│
├── docs/
│   ├── architecture.md
│   ├── api.md
│   ├── security.md
│   └── deployment.md
│
├── docker-compose.yml
├── .env.example
├── .gitignore
└── README.md

---

⚙️ Getting Started

1. Clone the repository

git clone https://github.com/CyberJana/securecode-ai.git

cd securecode-ai

2. Configure environment variables

cp .env.example .env

For the initial development version, keep:

LLM_PROVIDER=mock

No external LLM API key is required when using the mock provider.

---

🐳 Run with Docker

Start the application:

docker compose up --build

The backend will be available at:

http://localhost:8000

API documentation:

http://localhost:8000/docs

PostgreSQL:

localhost:5432

---

🔍 Run a Security Scan

Example API request:

curl -X POST \
  "http://localhost:8000/api/scans/?repository_path=/workspace/project"

Example response:

{
  "status": "completed",
  "total_findings": 2,
  "findings": [
    {
      "scanner": "Bandit",
      "rule_id": "B105",
      "title": "Possible hardcoded password",
      "severity": "LOW",
      "file": "example.py",
      "line": 12,
      "risk_score": 2,
      "cwe": "CWE-798",
      "owasp": "A07:2025 Authentication Failures"
    }
  ]
}

---

🧪 Security Scanners

SecureCode AI is designed around multiple security engines.

Scanner| Purpose
Semgrep| Source-code security analysis
Gitleaks| Secret and credential detection
Trivy| Dependency/container vulnerability scanning
Bandit| Python security analysis

The results are normalized into a common vulnerability format before being processed by the risk and AI engines.

---

🎯 Risk Scoring

SecureCode AI currently uses severity-based scoring:

Severity| Score
Critical| 10
High| 8
Medium| 5
Low| 2
Informational| 0

The scoring system is designed to evolve toward contextual risk analysis using factors such as:

- Exploitability
- Asset criticality
- Exposure
- Authentication requirements
- Vulnerability confidence
- Threat intelligence
- Reachability

---

🧩 CWE & OWASP Mapping

Security findings are mapped to recognized security classifications.

Examples:

SQL Injection
    ↓
CWE-89
    ↓
OWASP Injection Category

Command Injection
    ↓
CWE-78
    ↓
OWASP Injection Category

Mappings will be expanded as additional scanner rules are integrated.

---

🤖 AI Vulnerability Analysis

The AI layer converts technical scanner output into developer-friendly information.

Example:

Finding
   ↓
AI Analysis
   ↓
What is the vulnerability?
   ↓
Why is it dangerous?
   ↓
What could be affected?
   ↓
How should it be fixed?

Example output:

Severity: HIGH

Summary:
Potential command injection vulnerability detected.

Risk:
Untrusted input may reach an operating-system command.

Recommendation:
Use a safe API instead of constructing shell commands
from untrusted input. Validate and constrain input where
shell execution is unavoidable.

AI output should be treated as security assistance, not authoritative proof of exploitability. Findings should be validated by appropriate security testing and human review.

---

🔐 Security Principles

SecureCode AI follows several security principles:

- Never expose API keys to the frontend.
- Store secrets in environment variables or a secrets manager.
- Validate repository inputs.
- Avoid arbitrary code execution.
- Sandbox security tooling where appropriate.
- Validate AI-generated remediation.
- Use parameterized database queries.
- Apply authentication and authorization.
- Log security-sensitive actions.
- Do not automatically deploy AI-generated patches without validation.

---

🧪 Testing

Run backend tests:

pytest

Run frontend checks:

npm run lint

Build the frontend:

npm run build

---

🗺️ Roadmap

Phase 1 — MVP

- [x] FastAPI backend
- [x] Mock AI provider
- [x] Bandit integration
- [x] Risk scoring
- [x] CWE mapping
- [x] OWASP mapping
- [ ] PostgreSQL persistence
- [ ] Frontend dashboard

Phase 2 — Security Platform

- [ ] Semgrep integration
- [ ] Gitleaks integration
- [ ] Trivy integration
- [ ] GitHub repository integration
- [ ] Scan history
- [ ] Security reports
- [ ] Authentication

Phase 3 — AI DevSecOps

- [ ] AI vulnerability triage
- [ ] AI remediation suggestions
- [ ] GitHub Pull Request comments
- [ ] CI/CD security gates
- [ ] Automated regression testing
- [ ] Security policy engine

Phase 4 — SaaS

- [ ] Multi-tenant architecture
- [ ] Organization management
- [ ] RBAC
- [ ] Team dashboards
- [ ] Audit logging
- [ ] Usage analytics
- [ ] Billing

Phase 5 — Advanced Security

- [ ] Attack-path analysis
- [ ] Threat intelligence integration
- [ ] Reachability analysis
- [ ] AI security agent
- [ ] Autonomous security investigation
- [ ] Enterprise integrations

---

🌟 Future Vision

SecureCode AI aims to evolve from a vulnerability scanner into an AI-powered DevSecOps security platform.

Developer
    ↓
GitHub
    ↓
SecureCode AI
    ↓
Detect
    ↓
Understand
    ↓
Prioritize
    ↓
Recommend Fix
    ↓
Validate
    ↓
Pull Request
    ↓
Human Approval
    ↓
Secure Deployment

The long-term goal is to help development teams make security part of the software-development lifecycle rather than treating security as a final-stage activity.

---

🤝 Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.

git checkout -b feature/security-improvement

3. Make your changes.
4. Add or update tests.
5. Commit your changes.

git commit -m "feat: improve vulnerability analysis"

6. Push the branch.

git push origin feature/security-improvement

7. Open a Pull Request.

---

📜 License

This project is intended to be released under the MIT License.

See "LICENSE" for details.

---

⚠️ Disclaimer

SecureCode AI is a security-development and defensive analysis tool.

Security findings and AI-generated recommendations should be validated by qualified security professionals before being used for production security decisions.

Only scan repositories and systems that you own or have explicit authorization to test.

---

👨‍💻 Author

Janarthanan A

Cybersecurity | Digital Forensics | AI Security | DevSecOps

GitHub: CyberJana

---

⭐ Support the Project

If you find SecureCode AI useful:

- ⭐ Star the repository
- 🐛 Report security issues responsibly
- 💡 Suggest improvements
- 🤝 Contribute
- 🔀 Submit Pull Requests

Building the future of AI-powered application security. 🛡️🤖