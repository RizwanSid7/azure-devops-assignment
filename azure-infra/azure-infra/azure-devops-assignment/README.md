# Azure DevOps Engineer Assignment

## Project Overview

This project demonstrates the infrastructure design and deployment for a web service with the following requirements:

- SQL Database
- RPS of 1000/sec
- Integration with external services
- High Availability and Fault Tolerance
- Secure and Scalable Architecture

---

## Architecture & Components

1. **Web App** (App Service - S2 Tier)
2. **Azure SQL Database** (Provisioned with secure networking)
3. **Manual Horizontal Scaling** (3 Instances for 1000 RPS support)
4. **TLS Enforcement and HTTPS-only**
5. **Connection string securely stored in Application Settings**
6. **Deployment through Azure Portal**

---

## Screenshots

Screenshots of each step in the deployment process are included in the `screenshots/` folder.

---

## Challenges Faced

- App Service Editor was not visible in Azure UI.
- Uploading files directly to wwwroot was complex due to limited access in Free Tier.
- Faced DNS propagation delays after deploying App Service.
- Encountered "site not reachable" issue which resolved after proper deployment.
- Avoided installing tools like FileZilla due to security flags.

---

## Deployment Output

Static website URL:  
*(Include your actual URL here, if available)*

---

## Author

GitHub: [RizwanSid7](https://github.com/RizwanSid7)
