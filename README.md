<h1 align="center">Hi, I'm Souhila Sehili 👋</h1>

<p align="center">
  <b>Software & DevSecOps Engineer · PhD in Computer Science</b><br/>
  I build CI/CD pipelines that stop vulnerable code before it reaches production.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/souhila-sehili/"><img src="https://img.shields.io/badge/LinkedIn-Souhila%20Sehili-0A66C2?style=for-the-badge" alt="LinkedIn"/></a>
  <img src="https://img.shields.io/badge/Open%20to-relocating%20to%20London-1F3864?style=for-the-badge" alt="Open to relocating to London"/>
</p>

## 🧭 About me

- 🔐 Software engineer specialising in **DevSecOps**: automated tests, dependency scanning, static analysis and merge gates in CI/CD.
- 🛠️ **7 years** building and integrating web applications and **REST APIs**.
- 🎓 **PhD in Computer Science** · technical trainer since 2020.
- ☁️ Currently learning **Terraform on AWS** and preparing **AWS Solutions Architect – Associate**.

## 🚀 Featured project: [Secure CI/CD pipeline with automated security gates](https://github.com/SouhilaShl/tasks-api)

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

- ✅ **Nothing reaches `main` unchecked:** 3 required status checks protect the branch.
- 🧪 **Proven, not assumed:** I introduced a known HIGH vulnerability (CVE-2018-18074) and the pipeline blocked the merge.
- 🔗 **Supply chain:** every third-party action pinned to a commit SHA; secrets in GitHub Secrets; least-privilege tokens.
- 🔍 **Troubleshooting:** fixed a stuck required check, and found and fixed Docker bypassing UFW firewall rules.

## 🧰 Tech stack

![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![SonarCloud](https://img.shields.io/badge/SonarCloud-F3702A?style=flat-square&logo=sonarqubecloud&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat-square&logo=trivy&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
<br/>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Symfony](https://img.shields.io/badge/Symfony-000000?style=flat-square&logo=symfony&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

## 🧠 How I work

| Principle | In practice |
|---|---|
| **Rules, not advice** | A scan that can be ignored is a suggestion. Required checks make it a rule. |
| **Pin what you run** | A tag can be moved by its owner; a commit SHA cannot. |
| **Block, never auto-fix** | The pipeline stops the merge; a person understands and fixes the cause. |

<p align="center">💬 <b>Let's connect on <a href="https://www.linkedin.com/in/souhila-sehili/">LinkedIn</a></b></p>
