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

**Challenges Faced**

**1. App Service Editor Visibility Issue:**
I encountered an issue where the "App Service Editor" was not visible in the Azure portal. This made it difficult to directly edit files on the deployed app, as I had to find an alternative method to access and modify content.

**2. Uploading Files to wwwroot:**
Uploading files directly to the wwwroot folder was complex due to limited access in the free-tier App Service plan. This required additional steps and tools to work around the limitations of the free-tier.

**3. DNS Propagation Delays:**
After deploying the app, the DNS settings took some time to propagate. As a result, the website was not immediately accessible, causing delays in testing and validation.

**4. “Site Not Reachable” Issue:**
I encountered a "site not reachable" issue after deployment. This was resolved by ensuring proper deployment of the necessary files (like the index.html) and fixing a few configurations in the app.

**5. Avoiding FileZilla Due to Security Flags:**
I initially considered using tools like FileZilla to upload files, but security flags on my system prevented the installation. I decided to proceed with Azure Portal's Kudu service and SSH into the App Service to manage and deploy files directly to the web app.
---

## Author

GitHub: [RizwanSid7](https://github.com/RizwanSid7)
