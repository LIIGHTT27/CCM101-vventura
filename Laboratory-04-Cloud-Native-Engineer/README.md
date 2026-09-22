# 🐳 Laboratory 04 — The Cloud-Native Engineer

[![Mission](https://img.shields.io/badge/Mission-04-blue)](#)
[![Focus](https://img.shields.io/badge/Focus-Docker%20%26%20Containers-informational)](#)
[![Docker](https://img.shields.io/badge/Docker-29.1.3-2496ED)](#)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)](#)

### *From renting servers to running services — welcome to the container era.*

---

## 🚀 Mission Overview

Plot twist: after surviving the multi-cloud gauntlet, I got promoted to **CloudNova Technologies'** Cloud-Native Engineering Team. New title, new problem — a client stuck with slow, RAM-hungry Virtual Machines who kept hearing the word *"Docker"* thrown around in meetings without knowing what it actually does.

So I hopped into the **KillerCoda Playground** (Ubuntu 24.04.5 LTS, Docker 29.1.3), pulled up a terminal, and did what any self-respecting cloud-native engineer does: deployed a live Nginx web server inside a container, timed it against a mental image of a VM boot screen, and won.

**Lesson of the mission:** *a traditional sysadmin manages servers — a cloud-native engineer manages the services running on them.*

---

## 🎯 Objectives

- [x] Differentiate between traditional Virtual Machines (VMs) and Containers
- [x] Access a Docker-enabled cloud environment using KillerCoda
- [x] Execute fundamental Docker CLI commands
- [x] Pull, run, manage, and terminate a containerized application (Nginx)
- [x] Document container operations professionally in Markdown
- [x] Keep leveling up the GitHub Cloud Computing Portfolio

---

## ⌨️ Docker Commands Executed

| # | Command | What it did |
|---|---------|-------------|
| 1 | `docker --version` | Confirmed Docker `29.1.3` was installed |
| 2 | `docker info` | Verified environment status — Ubuntu 24.04.5 LTS, overlay2 driver, 0 containers/images at start |
| 3 | `docker pull nginx` | Pulled the official Nginx image from Docker Hub |
| 4 | `docker run -d -p 8080:80 --name my-nginx nginx` | Ran Nginx in detached mode as container `c2132a8d157d`, mapped host port 8080 → container port 80 |
| 5 | `curl http://localhost:8080` | Got back the full "Welcome to nginx!" page — server confirmed live |
| 6 | `docker ps` | Listed the running `my-nginx` container, status `Up About a minute` |
| 7 | `docker stop my-nginx` | Stopped the running container |
| 8 | `docker ps -a` | Verified status changed to `Exited (0) 8 seconds ago` |
| 9 | `docker rm my-nginx` | Removed the container completely |

*(Full explanations with raw output live in [`docker-deployment.md`](./docker-deployment.md).)*

---

## 🧠 Skills Learned

- How to spin up a fully working web server in **seconds**, not minutes
- The real meaning of port mapping and why containers don't talk to the outside world unless you let them
- The difference between *stopping* and *removing* a container — and why that distinction matters for data
- Reading `docker info` output to sanity-check an environment before deploying anything
- Why containers are the backbone of modern DevOps workflows

---

## 🧩 Challenges Encountered

Biggest "wait, why isn't this working" moment: making sure `curl` pointed at the **host** port (8080), not the container's internal port (80) — a classic first-timer mix-up that `docker ps`'s `PORTS` column cleared up instantly once I actually read it properly.

---

## 🖼️ Evidence

| Screenshot | Description |
|---|---|
| `screenshots/docker-version.png` | `docker --version` + `docker info` output confirming Docker 29.1.3 on Ubuntu 24.04.5 LTS |
| `screenshots/nginx-running.png` | `docker pull nginx`, `docker run`, and the successful `curl` response |
| `screenshots/container-lifecycle.png` | Full lifecycle: `docker ps` → `docker stop` → `docker ps -a` → `docker rm` |

---

*Next mission: who knows. But the containers are running, the client is impressed, and the portfolio keeps growing.* 🌱
