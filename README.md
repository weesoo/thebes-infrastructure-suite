# Thebes Modular Node Automation Framework

A production-grade, modular DevOps framework designed for independent Node Operators and Validators to deploy, harden, and monitor nodes across the **Thebes Substrate**. 

Instead of forcing a one-size-fits-all setup, this framework uses a **Modular Profile Architecture**. Operators can selectively choose and deploy an isolated infrastructure tailored to a single specific subnet based on their hardware requirements and budget.

---

## ⚡ Current Project Status: Active Learning & Development
> ⚠️ **Note to Reviewers:** This repository is currently under **Active Development**. I am dynamically building out this infrastructure framework while deeply studying the Thebes protocol specs, Substrate architecture, and advanced Linux/AWS security patterns. Commits are pushed regularly as my learning progresses.

---

## 📂 Repository Code Status (Transparent Roadmap)

To ensure full transparency during review, here is the current status of the codebase:
*   **`terraform/`**: Directory structure initialized and tracked via `.gitkeep`. Foundational AWS VPC and EC2 modules will be drafted next as cloud architecture patterns are reviewed.
*   **`ansible/`**: Base layout created. Roles for OS hardening and binary automation will be pushed in parallel with protocol installation guide syncs next week.
*   **`.gitignore`**: Fully configured for production security to prevent any accidental leakage of private keys (`.pem`, `.key`) or environment secrets.

---

## 🏗️ Modular Subnet Profiles

Each subnet requires unique hardware configurations and security baselines. This repository isolates them into independent deployment profiles:

1.  **Application Subnet Profile**: Optimized for standard compute and dApp hosting.
2.  **Signing Subnet Profile**: Hardened networking with strict firewall configurations for transaction relaying.
3.  **Financial Subnet Profile**: High-security isolated topology for ledger validation.
4.  **Inference Subnet Profile (AI)**: High-performance computing setups optimized for GPU workloads and verifiable AI runtime execution.

---

## 🛠️ Operational Design

*   **Modular Provisioning (`terraform/`)**: Organized into independent modules, allowing validators to provision a single AWS EC2 instance with the exact specifications (CPU/GPU/RAM) required for their chosen subnet.
*   **Targeted Configuration (`ansible/`)**: Playbooks are tagged and separated by roles, ensuring only the necessary dependencies and configurations are applied to the selected node type.
*   **Target OS**: Ubuntu Server (Linux)

---

## 🚀 Future Roadmap & Work-in-Progress (WIP)

- [x] Design modular multi-subnet directory layout and security rules (`.gitignore`).
- [🔄] **[In Progress]** Deep-diving into Thebes protocol documentation and Linux fundamentals.
- [ ] Develop independent Terraform modules for custom hardware scaling on AWS.
- [ ] Build specialized Ansible roles for targeted node software deployment and OS hardening.
- [ ] Implement individual node telemetry and health monitoring.
