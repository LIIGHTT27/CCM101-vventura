# 🐳 Docker Deployment Log

[![Environment](https://img.shields.io/badge/Environment-KillerCoda-orange)](#)
[![Docker](https://img.shields.io/badge/Docker-29.1.3-2496ED)](#)
[![Image](https://img.shields.io/badge/Image-nginx-009639)](#)

### *Deploying a live web server, one command at a time.*

---

## 🧾 Environment Snapshot

Before touching containers, confirmed the playground was actually ready:

- **Docker version:** `29.1.3`, build `29.1.3-0ubuntu3~24.04.2`
- **OS:** Ubuntu 24.04.5 LTS (kernel `6.8.0-139-generic`)
- **Architecture:** x86_64
- **Storage Driver:** overlay2
- **Containers at start:** 0 running, 0 stopped, 0 images

---

## 🛠️ Commands & What They Actually Do

1. **`docker --version`**
   Confirmed Docker Engine `29.1.3` was installed and available.

2. **`docker info`**
   Checked the current status of the Docker environment — 0 containers, 0 images, running on Ubuntu 24.04.5 LTS with the `overlay2` storage driver.

3. **`docker pull nginx`**
   Pulled the official Nginx image from Docker Hub. Seven layers downloaded, resolving to digest `sha256:abe47724e466aeab9a345d8e46a221c2fa8953c7848bb4a3bd9976a7199f8cf2`.

4. **`docker run -d -p 8080:80 --name my-nginx nginx`**
   Created and started a container (ID `c2132a8d157d`) from the Nginx image in detached mode, mapping host port `8080` to container port `80`.

5. **`curl http://localhost:8080`**
   Sent an HTTP request to the mapped host port and received the full "Welcome to nginx!" HTML page back — confirming the web server inside the container was live and responding.

6. **`docker ps`**
   Listed the running container: `c2132a8d157d`, image `nginx`, status `Up About a minute`, ports `0.0.0.0:8080->80/tcp, [::]:8080->80/tcp`, named `my-nginx`.

7. **`docker stop my-nginx`**
   Gracefully stopped the running `my-nginx` container.

8. **`docker ps -a`**
   Listed all containers, running or not — confirmed `my-nginx` now shows status `Exited (0) 8 seconds ago`.

9. **`docker rm my-nginx`**
   Permanently removed the stopped container from the system.

---

## 📸 Evidence

- ![Docker Version](screenshots/docker-version.png) — `docker --version` and `docker info` output
- ![Nginx Running](screenshots/nginx-running.png) — `docker pull`, `docker run`, and successful `curl` output
- ![Container Lifecycle](screenshots/container-lifecycle.png) — `docker ps` → `docker stop` → `docker ps -a` → `docker rm`

---

*Container pulled. Container deployed. Container tested. Container respectfully removed. Mission logged.* 🫡
