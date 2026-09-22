# 🐳 Laboratory 04 — The Cloud-Native Engineer

[![Mission](https://img.shields.io/badge/Mission-04-blue)](#)
[![Focus](https://img.shields.io/badge/Focus-Docker%20%26%20Containers-informational)](#)
[![Docker](https://img.shields.io/badge/Docker-29.1.3-2496ED)](#)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)](#)

### *From renting servers to running services — this is where I actually started using containers.*

---

## 🚀 Mission Overview

For this one, I'm supposedly part of CloudNova Technologies' Cloud-Native Engineering Team, and the client's complaint is something I think a lot of people run into: their Virtual Machines take forever to boot and eat up way more RAM than they'd like. They kept hearing the word "Docker" thrown around but nobody on their end could actually explain what it does or why it matters.

So I opened up the KillerCoda Playground (Ubuntu 24.04.5 LTS, Docker 29.1.3 already installed) and just worked through it — checked that Docker was actually running, pulled the Nginx image, ran it as a container, and hit it with curl to prove it was serving a real page. The whole thing, start to finish, probably took less time than a single VM would've needed just to boot.

The thing that stuck with me most: I'm not managing a server anymore, I'm managing a service that happens to be running somewhere. That's a different mindset than I expected going in.

---

## 🎯 Objectives

- [x] Differentiate between traditional Virtual Machines (VMs) and Containers
- [x] Access a Docker-enabled cloud environment using KillerCoda
- [x] Execute fundamental Docker CLI commands
- [x] Pull, run, manage, and terminate a containerized application (Nginx)
- [x] Document what I did clearly enough that someone else could repeat it
- [x] Keep building out my GitHub Cloud Computing Portfolio

---

## ⌨️ Docker Commands I Ran

| # | Command | What I was doing |
|---|---------|-------------|
| 1 | `docker --version` | Checking that Docker `29.1.3` was actually installed |
| 2 | `docker info` | Getting a status check on the environment — Ubuntu 24.04.5 LTS, overlay2 driver, nothing running yet |
| 3 | `docker pull nginx` | Downloading the official Nginx image from Docker Hub |
| 4 | `docker run -d -p 8080:80 --name my-nginx nginx` | Starting the container in the background as `my-nginx`, mapping my host's port 8080 to the container's port 80 |
| 5 | `curl http://localhost:8080` | Hitting the server to see if it actually responded — it did, full "Welcome to nginx!" page |
| 6 | `docker ps` | Confirming `my-nginx` was up and running |
| 7 | `docker stop my-nginx` | Shutting the container down |
| 8 | `docker ps -a` | Double-checking it actually stopped |
| 9 | `docker rm my-nginx` | Deleting the container for good |

*(I broke down what each command actually does in more detail in [`docker-deployment.md`](./docker-deployment.md).)*

---

## 🧠 What I Actually Learned

Honestly the biggest thing was just seeing the speed difference in real time — I'm used to VMs taking a while, and watching a full web server come online in under a second was kind of a "oh, okay, THAT'S why people use this" moment. Beyond that, I understood port mapping way better after actually using it than I did just reading about it, and I finally get why `docker stop` and `docker rm` are two separate commands instead of one — because sometimes you want to pause something, not erase it.

---

## 🧩 Where I Got Stuck

I'll admit I almost ran `curl` against port 80 instead of 8080 out of habit, which obviously didn't work since 80 isn't exposed on the host. Looking at the `PORTS` column in `docker ps` output made it click — that's literally where the mapping is spelled out, I just had to actually read it.

---

## 🖼️ Screenshots

| Screenshot | What it shows |
|---|---|
| `screenshots/docker-version.png` | `docker --version` and `docker info` output confirming Docker 29.1.3 on Ubuntu 24.04.5 LTS |
| `screenshots/nginx-running.png` | Pulling the image, running the container, and the successful `curl` response |
| `screenshots/container-lifecycle.png` | The full lifecycle — list, stop, verify, remove |

---

*Onto whatever mission comes next. The client's servers are faster now, at least in theory.* 🌱
