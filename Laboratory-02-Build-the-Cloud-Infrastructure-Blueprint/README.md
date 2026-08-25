# ☁️ Laboratory Activity 2 — Mission 2
## 🏗️ Build the Cloud Infrastructure Blueprint

> **Trainee:** Junior Cloud Infrastructure Engineer, CloudNova Technologies
> **Assignment:** Prepare a Cloud Infrastructure Assessment Report before any servers are deployed.

---

## 🎯 Mission Overview
I inspected a Linux server running on KillerCoda, documented its infrastructure components, compared the three major cloud providers, and designed a simple cloud architecture diagram — all to simulate the planning phase of a real cloud deployment.

## 🧭 Objectives
- [x] Explain the major components of cloud infrastructure
- [x] Investigate the hardware and software resources available in a Linux environment
- [x] Differentiate compute, storage, networking, and identity resources
- [x] Interpret the relationship between cloud infrastructure components
- [x] Create professional technical documentation using Markdown
- [x] Continue building a structured GitHub Cloud Computing Portfolio

## 🧩 Cloud Infrastructure Components
I identified four core components on my server: compute (1 vCPU, 1.9 GiB RAM), storage (19 GiB root disk via `/dev/vda1`), networking (IP `172.30.1.2`), and the OS (Ubuntu 24.04.4 LTS). Full breakdown in [`cloud-components.md`](./cloud-components.md).

## 🛠️ Tools Used
| Tool | Purpose |
|---|---|
| KillerCoda Playground | Ran the Linux server I inspected |
| GitHub | Hosted my portfolio and documentation |
| Draw.io | Built my cloud architecture diagram |

## 💻 Linux Commands Executed
| Command | Purpose |
|---|---|
| `cat /etc/os-release` | Checked the OS version |
| `uname -r` | Checked the kernel version |
| `lscpu` / `nproc` | Checked CPU model and core count |
| `free -h` | Checked total RAM |
| `df -h` | Checked disk capacity |
| `mount \| grep "^/dev"` | Checked mounted file systems |
| `hostname` / `hostname -I` | Checked hostname and IP address |

## 🌱 Skills Learned
- I learned how to inspect a Linux server's hardware and software specs from the command line.
- I learned how compute, storage, networking, and the OS work together as one system.
- I learned how the same cloud service (compute, storage, IAM) goes by different names across AWS, Azure, and GCP.

## 🚧 Challenges Encountered
- I found it tricky at first to connect raw command output to what it actually meant for cloud readiness.

---

## 📂 Deliverables in This Folder
| File | Description |
|---|---|
| [`infrastructure-report.md`](./infrastructure-report.md) | Server hardware/software inspection |
| [`cloud-components.md`](./cloud-components.md) | Compute, storage, networking & OS breakdown |
| [`cloud-provider-comparison.md`](./cloud-provider-comparison.md) | AWS vs Azure vs GCP comparison |
| [`reflection.md`](./reflection.md) | Mission reflection |
| [`screenshots/`](./screenshots) | Evidence captures |

---
🔙 *Back to [Portfolio Home](../README.md)*


