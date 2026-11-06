<h1 align="center">Hi, I'm Souhila Sehili 👋</h1>

<p align="center">
  <b>Software & DevSecOps Engineer · PhD in Computer Science</b><br/>
  I build CI/CD pipelines that stop vulnerable code before it reaches production.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/souhila-sehili/"><img src="https://img.shields.io/badge/LinkedIn-Souhila%20Sehili-0A66C2?style=for-the-badge" alt="LinkedIn"/></a>
  <a href="mailto:souhilasehili.s@gmail.com"><img src="https://img.shields.io/badge/Email-souhilasehili.s%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Based%20in-Normandy%2C%20France-555555?style=for-the-badge" alt="Based in Normandy, France"/>

</p>

---

## 🧭 About me

- 🛠️ **7 years** building and integrating web applications and **REST APIs** (Python, PHP, JavaScript, Salesforce API).
- 🔐 Now focused on **DevSecOps**: shifting security left with automated tests, dependency scanning, static analysis and merge gates.
- 🎓 **PhD in Computer Science** (University of Corsica): discrete event simulation for IoT system design.
- 👩‍🏫 **Technical trainer since 2020**: I teach web development, databases and Git, and coach developers on good practices.
- ☁️ **Currently learning:** Terraform on AWS · preparing **AWS Certified Solutions Architect – Associate**.
- 💼 **Open to:** DevSecOps, DevOps and software engineering roles in **London**.

---

## 🚀 Featured project: [Secure CI/CD pipeline with automated security gates](https://github.com/SouhilaShl/tasks-api)

> **The pipeline is the project.** The FastAPI app is deliberately simple, so the focus stays on how code is tested, scanned, gated, built and deployed.

```mermaid
flowchart LR
    A[Pull request] --> B{CI: 3 parallel jobs}
    B --> C[Tests and lint<br/>pytest + ruff]
    B --> D[Dependency scan<br/>Trivy: HIGH or CRITICAL fails]
    B --> E[Static analysis<br/>SonarCloud quality gate]
    C --> F{Branch protection<br/>3 required checks}
    D --> F
    E --> F
    F -->|all green| G[Merge to main]
    F -->|any red| H[Merge blocked]
    G --> I[Docker image<br/>pushed to GHCR]
    I --> J[Ubuntu VPS<br/>nginx + UFW]
```

- ✅ **Nothing reaches `main` unchecked:** branch protection with 3 required status checks.
- 🧪 **Proven, not assumed:** I introduced a known HIGH vulnerability (CVE-2018-18074) and the pipeline blocked the merge.
- 🔗 **Supply-chain hardening:** every third-party action pinned to a full commit SHA; secrets in GitHub Secrets; least-privilege registry token.
- 🔍 **Real troubleshooting:** fixed a stuck required check by moving SonarCloud into the pipeline; found and fixed Docker bypassing UFW firewall rules.
- 🐳 **Deployment:** containerised API on an Ubuntu VPS behind an nginx reverse proxy, container bound to localhost only.

### 🔄 Latest commits on this project

- [Finalise README: fill placeholders, update SonarCloud CI section](https://github.com/SouhilaShl/tasks-api/commit/d5faa59f2552ca94046c40b7f654aae0de7bfda5)
- [update readme](https://github.com/SouhilaShl/tasks-api/commit/0585b91db0da2ee1d96d717a4e407d53b1a08645)
- [Add SonarCloud analysis to CI pipeline](https://github.com/SouhilaShl/tasks-api/commit/5a307a39ed28dacc21475ebb5c3e4557a3b10483)
- [Add SonarCloud project configuration](https://github.com/SouhilaShl/tasks-api/commit/3bfadc486f83d46a6fd311f9084bbf1a70fc9203)


---

## 🧰 Tech stack

**Security (DevSecOps)**<br/>
![SonarCloud](https://img.shields.io/badge/SonarCloud-SAST-F3702A?style=flat-square&logo=sonarqubecloud&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy-SCA-1904DA?style=flat-square&logo=trivy&logoColor=white)
![Secrets](https://img.shields.io/badge/Secrets%20management-GitHub%20Secrets-181717?style=flat-square&logo=github&logoColor=white)
![Supply chain](https://img.shields.io/badge/Supply%20chain-SHA--pinned%20actions-2EA44F?style=flat-square)

**CI/CD**<br/>
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**Containers & Linux**<br/>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu%20Server-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Cloud & IaC (learning)**<br/>
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)

**Development**<br/>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Symfony](https://img.shields.io/badge/Symfony-000000?style=flat-square&logo=symfony&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![REST APIs](https://img.shields.io/badge/REST%20APIs-Salesforce%20integration-00A1E0?style=flat-square)

**Databases**<br/>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logoColor=white)

---

## 🧠 How I work

| Principle | In practice |
|---|---|
| **Rules, not advice** | A scan that can be ignored is a suggestion. Required checks make it a rule. |
| **Pin what you run** | A tag can be moved by its owner; a commit SHA cannot. |
| **Report and block, never auto-fix** | The pipeline stops the merge; a person understands and fixes the cause. |
| **Clean as you code** | Gates enforce quality on new code, so the codebase improves with every change. |
| **Explain it simply** | If I can teach it to a beginner, I understand it well enough to run it in production. |

---

## 💼 Experience

| Role | Where | When |
|---|---|---|
| Technical Trainer (freelance) | Training centres in Rouen and Dieppe | 2020 – present |
| Software Engineer (freelance) | Wonderlive, decentralised social network | 2025 |
| Software Engineer | Paris-Normandie, regional newspaper | 2020 – 2021 |
| Web Developer (internship) | Qwantis, start-up | 2019 |
| PhD Researcher & Teaching Assistant | University of Corsica | 2013 – 2018 |

🎓 PhD in Computer Science (2018) · Master's in Information Systems and Internet (2013) · 📄 3 papers at international conferences (SIMULTECH 2015, SIGSIM-PADS 2015)

---

<p align="center">
  <sub>🤖 This README is rebuilt every day by a GitHub Actions workflow using <a href="https://github.com/rderik/octoprofile">octoprofile</a>, pinned to a commit SHA and running with least-privilege permissions.</sub>
</p>
