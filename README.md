# Automated CI/CD Deployment Pipeline

A robust, automated continuous integration and continuous deployment (CI/CD) pipeline built using **GitHub Actions**, **AWS EC2**, **Ubuntu**, and **Nginx**. This project automates code delivery from local development branches straight to a cloud production server.

---

## 🚀 Architecture & Features

* **Automated Deployments:** Code pushes to specific branches automatically trigger workflows, eliminating manual file transfers.
* **Dual-Environment Workflow:** Configured independent deployment targets for separate development stages (`staging` and `production`).
* **Web Server Hosting:** Powered by an optimized **Nginx** reverse proxy and web server running on an **AWS EC2** Ubuntu instance.
* **Secure Remote Execution:** Leverages SSH keys and GitHub Secrets to securely communicate with the remote cloud server during pipeline runs.

---

## 🛠️ Tech Stack

* **Cloud Provider:** AWS EC2 (Ubuntu Server)
* **Web Server:** Nginx
* **Automation & CI/CD:** GitHub Actions
* **Version Control:** Git & GitHub
* **Frontend:** HTML5 / CSS3

---

## 📂 Project Structure

```text
├── .github/
│   └── workflows/
│       ├── staging.yml      # Triggers deployment on push to 'staging' branch
│       └── production.yml   # Triggers deployment on push to 'main' branch
├── index.html               # Main landing page asset
└── README.md                # Project documentation

⚙️ How It Works
1. Trigger: A developer pushes code changes to the ⁠main⁠ or ⁠staging⁠ branch on GitHub.
2. Action Runner: GitHub Actions spins up a virtual runner to execute the workflow steps defined in ⁠.github/workflows/⁠.
3. Secure Transfer: The runner authenticates via SSH using encrypted repository secrets and securely syncs the updated project files to the corresponding directory on the AWS EC2 instance.
4. Serving Content: Nginx instantly serves the updated static web files live to the public IP address.
🔮 Future Enhancements
 Implementing Docker containerization for consistent environment isolation.
 Integrating Infrastructure as Code (IaC) using Terraform.
 Setting up automated SSL certificates via Let's Encrypt for HTTPS support.
