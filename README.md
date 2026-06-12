# Enterprise DevSecOps Pipeline - DataFlow Analytics Integration

Security Pipeline
GitLab CI
Azure

## Project Overview

This repository implements an enterprise-grade DevSecOps pipeline for **DataFlow Analytics**, a newly acquired subsidiary of NexusCore Technologies. The pipeline brings security automation to an organization with 200+ enterprise clients processing sensitive data analytics.

### Business Context

- **Client**: NexusCore Technologies / DataFlow Analytics (M&A Integration)
- **Challenge**: Acquired company had zero security scanning, posing compliance risks
- **Solution**: Enterprise DevSecOps pipeline with GitLab CI/CD and Azure deployment

## Security Tools Implemented


| Tool                        | Purpose                                    | Stage      |
| --------------------------- | ------------------------------------------ | ---------- |
| **Semgrep**                 | Static Application Security Testing (SAST) | Build      |
| **Snyk**                    | Software Composition Analysis (SCA)        | Build      |
| **Checkov**                 | Infrastructure as Code Security            | Build      |
| **GitLab Secret Detection** | Credential Scanning                        | Pre-commit |


## Architecture


Developer Push --> GitLab CI/CD --> Security Scans --> Docker Build --> Azure Deployment
                        |
                        ├── SAST (Semgrep)
                        ├── SCA (Snyk)
                        ├── Secret Scan (GitLab)
                        └── IaC Scan (Checkov)


## Security Findings Summary

### SAST Findings (Semgrep)

- SQL Injection vulnerabilities
- Command injection risks
- Insecure deserialization

### SCA Findings (Snyk)

- CVE-2020-14343 in PyYAML (Critical)
- Multiple Django 3.2.0 vulnerabilities
- Outdated Flask with security patches

### IaC Findings (Checkov)

- Azure Storage without HTTPS enforcement
- NSG rules allowing unrestricted access
- SQL Server firewall misconfigurations

## Skills Demonstrated

- **CI/CD**: GitLab CI/CD pipeline design
- **SAST**: Semgrep rule configuration
- **SCA**: Snyk vulnerability management
- **IaC Security**: Checkov policy enforcement
- **Cloud**: Azure infrastructure with Terraform
- **Enterprise Security**: M&A security integration

## Multi-Platform Expertise

This is **Project 2** of the Cyber Agoge DevSecOps series:

- **Project 1**: GitHub Actions + AWS ([View Repository](https://github.com/swcloud93/devsecops-pipeline-project-1.git))
- **Project 2**: GitLab CI/CD + Azure (This repository)

Together, these projects demonstrate versatility across major DevOps platforms.

## About This Project

Built as part of the **Cyber Agoge DevSecOps Bootcamp** - training elite security engineers.

---

*Note: Vulnerabilities are intentional for educational purposes. Never deploy to production.*
EOF
