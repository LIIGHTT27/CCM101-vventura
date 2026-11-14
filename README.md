<div align="center">

```text
 ██████╗ ██████╗███╗   ███╗ ██╗ ██████╗  ██╗
██╔════╝██╔════╝████╗ ████║███║██╔═████╗███║
██║     ██║     ██╔████╔██║╚██║██║██╔██║╚██║
██║     ██║     ██║╚██╔╝██║ ██║████╔╝██║ ██║
╚██████╗╚██████╗██║ ╚═╝ ██║ ██║╚██████╔╝ ██║
 ╚═════╝ ╚═════╝╚═╝     ╚═╝ ╚═╝ ╚═════╝  ╚═╝
```

# ⚡ CCM101 — CLOUD COMPUTING PORTFOLIO ⚡
### 🚀 *Architecting the Virtual Frontier*

[![Student](https://img.shields.io/badge/AUTHOR-Victor%20Ventura-8A2BE2?style=for-the-badge&logo=github&logoColor=white)](https://github.com/LIIGHTT27)
[![Institution](https://img.shields.io/badge/INSTITUTION-UEP%20College%20of%20IT-00FFFF?style=for-the-badge&logo=google-cloud&logoColor=black)](https://uep.edu.ph)
[![Course](https://img.shields.io/badge/COURSE-CCM101%20Cloud%20Computing-FF007F?style=for-the-badge&logo=amazon-aws&logoColor=white)](#)
[![Status](https://img.shields.io/badge/SYSTEM%20STATUS-100%25%20ONLINE-00FF66?style=for-the-badge&logo=docker&logoColor=black)](#)

---

</div>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2500&pause=1000&color=00FFFF&center=true&vCenter=true&width=600&lines=System+Initialized...;Welcome+to+the+Cloud+Infrastructure+Hub;Deploying+Containers...;Securing+Perimeters...;Automating+Operations...;Capstone+Deployed." alt="Typing SVG" />
</p>

---

## 🛰️ SYSTEM OVERVIEW

Welcome to my central command interface for **CCM101 — Cloud Computing**.

I am **Victor Juvenile M. Ventura**, a student at the **University of Eastern Pangasinan (College of Information Technology)**. This repository is a version-controlled record of my journey through containerization, multi-cloud architecture, DevOps automation, security hardening, and observability — culminating in a **capstone project** where a full multi-service infrastructure was designed and deployed from scratch.

---

## 🗺️ MISSION LOG & EXECUTION MATRIX

| ID | Mission Target | Core Focus Area | Tech Stack | Status |
| :---: | :--- | :--- | :--- | :---: |
| **[`LAB-01`](./Laboratory-01-Welcome-to-the-Cloud)** | **Welcome to the Cloud** | Linux Fundamentals, Shell, Git Architecture | `Bash` `Git` `GitHub` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-02`](./Laboratory-02-Build-the-Cloud-Infrastructure-Blueprint)** | **Build the Cloud Infrastructure Blueprint** | Compute, Storage, VNETs, Provider Abstraction | `Cloud Arch` `IaaS` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-03`](./Laboratory-03-Multi-Cloud-Explorer)** | **Multi-Cloud Explorer** | AWS vs Azure vs GCP Analysis & Benchmarking | `AWS` `Azure` `GCP` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-04`](./Laboratory-04-Cloud-Native-Engineer)** | **The Cloud-Native Engineer** | Container Isolation, Images, Nginx Orchestration | `Docker` `Nginx` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-05`](./Laboratory-05-Cloud-Data-Engineer)** | **The Cloud Data Engineer** | Block/File/Object Storage, S3 API, Buckets | `MinIO` `S3 API` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-06`](./Laboratory-06-Cloud-Deployment-Engineer)** | **The Cloud Deployment Engineer** | Multi-Tier Orchestration & Persistence | `Docker Compose` `MariaDB` `Nextcloud` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-07`](./Laboratory-07-Cloud-Operations-Engineer)** | **The Cloud Operations Engineer** | Real-time Metrics, Log Streaming, Telemetry | `Observability` `Docker Logs` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-08`](./Laboratory-08-Cloud-Security-Engineer)** | **The Cloud Security Engineer** | Firewall Hardening, Attack Surface Reduction, Default Deny | `UFW` `Netstat` `Security Audit` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-09`](./Laboratory-09-Cloud-Automation-Engineer)** | **The Cloud Automation Engineer** | Shell Scripting, Cron Automation, Auto-Backups | `Bash` `Cron` `Automation` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |
| **[`LAB-10`](./Laboratory-10-Enterprise-Cloud-Architect)** | **The Enterprise Cloud Architect** *(Capstone)* | End-to-End Infrastructure Design, Reverse Proxy & TLS, Private DNS, Self-Hosted Services, Automated Backups | `Ubuntu Server` `Docker Compose` `PostgreSQL` `Gitea` `Vaultwarden` `Pi-hole` `Nginx` | ![Completed](https://img.shields.io/badge/-ONLINE-00FF66?style=flat-square) |

---

## 🏗️ FEATURED: LAB 10 — ENTERPRISE CLOUD ARCHITECT

The capstone moved from guided labs to an open-ended build: no step-by-step instructions, just a goal — design and deliver a production-style environment inside a headless Ubuntu Server VM, then present it. It was completed as a team project.

| Layer | Component | Role |
| :--- | :--- | :--- |
| **Edge** | `Nginx` | Reverse proxy terminating HTTPS for all services |
| **DNS** | `Pi-hole` | Internal DNS resolution (`*.cloudnova.server`) and ad blocking |
| **Apps** | `Gitea` · `Vaultwarden` | Self-hosted Git platform and password manager |
| **Data** | `PostgreSQL 15` | Shared database backing the apps, with persistent volumes |
| **Ops** | `Bash` + `cron` + `OpenSSL` | Nightly database dumps, 30-day backup retention, certificate renewal, proxy reload |

All five containers share a dedicated bridge network (`cloudnova-network`) and are defined in a single [`docker-compose.yml`](./Laboratory-10-Enterprise-Cloud-Architect/docker-compose.yml). Maintenance is scripted in [`automation-script.sh`](./Laboratory-10-Enterprise-Cloud-Architect/automation-script.sh).

---

## 🧭 REPOSITORY ARCHITECTURE

```plain
CCM101-vventura
├── 📄 README.md                                                 
├── 📁 Laboratory-01-Welcome-to-the-Cloud/                      
├── 📁 Laboratory-02-Build-the-Cloud-Infrastructure-Blueprint/  
├── 📁 Laboratory-03-Multi-Cloud-Explorer/                      
├── 📁 Laboratory-04-Cloud-Native-Engineer/                     
├── 📁 Laboratory-05-Cloud-Data-Engineer/                       
├── 📁 Laboratory-06-Cloud-Deployment-Engineer/                 
├── 📁 Laboratory-07-Cloud-Operations-Engineer/                 
├── 📁 Laboratory-08-Cloud-Security-Engineer/                   
├── 📁 Laboratory-09-Cloud-Automation-Engineer/               
└── 📁 Laboratory-10-Enterprise-Cloud-Architect/                
    ├── 📄 README.md
    ├── 🐳 docker-compose.yml
    ├── ⚙️ automation-script.sh
    ├── 🖼️ architecture-diagram.png
    ├── 📄 operarion-maunal.md
    └── 📄 final-reflection.md
```

> **Note**: Laboratories 01–09 each contain their own `README.md`, written documentation, and an evidence folder (`screenshots/`). Laboratory 10 is the capstone and instead ships its deployable configuration, an architecture diagram, an operations manual, and a final reflection covering all ten missions.

---

## 🛠️ ARSENAL & TECH MATRIX

<div align="center">

### **Infrastructure & Multi-Cloud**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Google Cloud](https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)

### **Containerization, Storage & Data**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![MinIO](https://img.shields.io/badge/MinIO-C72C48?style=for-the-badge&logo=minio&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

### **Networking & Self-Hosted Services**
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Pi-hole](https://img.shields.io/badge/Pi--hole-96060C?style=for-the-badge&logo=pihole&logoColor=white)
![Gitea](https://img.shields.io/badge/Gitea-609926?style=for-the-badge&logo=gitea&logoColor=white)
![Vaultwarden](https://img.shields.io/badge/Vaultwarden-175DDC?style=for-the-badge&logo=bitwarden&logoColor=white)
![Nextcloud](https://img.shields.io/badge/Nextcloud-0082C9?style=for-the-badge&logo=nextcloud&logoColor=white)

### **Systems, Automation & Security**
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Ubuntu](https://img.shields.io/badge/Ubuntu%20Server-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![GNU Bash](https://img.shields.io/badge/GNU%20Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)

</div>

---

## 🏆 PORTFOLIO COMPLETION & LEARNING OUTCOMES

Across ten missions, I built practical, hands-on experience across foundational and advanced cloud computing principles:

* 🔹 **Containerization & Deployment**: Worked with container isolation, image management, and multi-service deployment using Docker and Docker Compose (Nextcloud + MariaDB stack).
* 🔹 **Cloud Data Architecture**: Explored object, file, and block storage, deploying private S3-compatible object storage with MinIO and bucket configuration.
* 🔹 **Security & Hardening**: Applied defense-in-depth by configuring host firewalls (`UFW`), auditing listening services, and enforcing default-deny policies.
* 🔹 **Operations & Automation**: Built automated backup pipelines with shell scripts and `cron`, alongside container log inspection and monitoring.
* 🔹 **Infrastructure Design (Capstone)**: Planned and delivered a complete environment on a headless Ubuntu Server VM — five containerized services behind an HTTPS reverse proxy, internal DNS, persistent volumes, and scripted maintenance.

For a mission-by-mission look back, see the [final reflection](./Laboratory-10-Enterprise-Cloud-Architect/final-reflection.md).

---

<div align="center">

### 🌐 *Designed & Developed by Victor Juvenile M. Ventura*
**University of Eastern Pangasinan — College of Information Technology**

```text
[ STATUS: ALL 10 MISSIONS COMPLETED ] • [ SYSTEM OPERATIONAL ]
```

</div>
