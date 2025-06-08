# Azure DevOps Engineer Assignment

## 🌐 Project Overview
This project demonstrates the infrastructure design and deployment for a highly available, secure, and scalable web service on Microsoft Azure. It is designed to handle up to **1000 requests per second (RPS)** while maintaining performance, security, and integration with external services.

---

## 🏗️ Architecture & Components

| Component        | Description |
|------------------|-------------|
| **App Service (S2 Tier)** | Hosts the web frontend, scaled to 3 instances for high availability |
| **Azure SQL Database** | Deployed with secure networking and private endpoint |
| **Load Balancer** | (Logical/Manual) Load distribution across App Service instances |
| **Application Settings** | Secrets and connection strings stored securely |
| **Network Security** | Enforced HTTPS-only, TLS 1.2, and private networking for database |
| **Deployment Method** | Manual provisioning via Azure Portal, Kudu, and SSH |

> 📁 _Screenshots of deployment steps are available in the `screenshots/` folder._

---

## 🖼️ Architecture Diagram

![Architecture Diagram](./architecture.png)


---

## 🛠️ Tech Stack

- **Microsoft Azure**
  - App Service (S2)
  - Azure SQL Database
  - Recovery Services Vault
  - Virtual Network, Subnets
  - Application Settings
- **Tools**
  - Azure Portal & Azure CLI
  - Kudu Console & SSH
  - GitHub for version control

---

## ⚙️ Deployment Guide

### Step-by-Step Setup (Manual)

1. **Create Resource Group**
2. **Create VNet & Subnets**:
   - One for the App Service (public)
   - One for the Azure SQL Database (private)
3. **Deploy Azure SQL Database**:
   - Configure firewall rules or private endpoint access
4. **Deploy App Service (S2 Tier)**:
   - Set scaling to 3 instances (Manual horizontal scale)
5. **Configure Application Settings**:
   - Store database connection strings securely
6. **Enforce HTTPS and TLS**:
   - Enable HTTPS-only, disable HTTP
7. **Upload Web Files**:
   - Use Kudu or SSH to access `wwwroot` and deploy your `index.html`

---

## 🧩 Challenges Faced & Solutions

| Issue | Resolution |
|-------|------------|
| **App Service Editor not visible** | Used Kudu Console and SSH access instead |
| **Uploading to `wwwroot`** | Avoided FileZilla due to security flags; used Azure Portal Kudu |
| **DNS Propagation Delays** | Waited and verified using online tools |
| **“Site Not Reachable” Error** | Resolved by ensuring proper content and endpoint configuration |
| **Free-tier Limitations** | Overcame by manual provisioning and using higher-tier services when needed |

---

## 🔐 Security & Reliability Considerations

- Enforced HTTPS-only and TLS 1.2
- Stored secrets in Application Settings instead of code
- Configured horizontal scaling for high availability
- Manual snapshot recovery and disaster planning considered
- Used Azure-managed identity and access restrictions where applicable

---

## 🚀 Future Enhancements

- Automate deployment with Terraform or Bicep
- Integrate CI/CD using GitHub Actions or Azure Pipelines
- Implement monitoring with Azure Monitor and Log Analytics

---

## 👤 Author

**Rizwan Siddiqui**  
GitHub: [RizwanSid7](https://github.com/RizwanSid7)

---

## 📎 Repository Structure

```plaintext
azure-devops-assignment/
├── azure-infra/
│   └── azure-devops-assignment/
│       ├── README.md
│       ├── screenshots/
│       └── index.html (or other web files)
└── ...
