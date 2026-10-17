# 🪣 Laboratory 5 — The Cloud Data Engineer
### *CloudNova Technologies — Cloud Data Engineering Team*

> 🎯 **Mission:** Deploy my own S3-compatible object storage server using MinIO and Docker, create a bucket named `client-photos`, and upload a file to prove it works — because a cloud engineer doesn't just store data, they make sure it's scalable, accessible, and secure.

---

## 🚀 Mission Overview

A client is building a photo-sharing app and needs somewhere to keep millions of user-uploaded images. They can't store them inside the web server container, because containers are ephemeral — once a container is removed, its data goes with it. My job was to build a proof-of-concept object storage environment.

Using the KillerCoda Ubuntu Playground, I deployed **MinIO** with a single `docker run` command, opened its web console through port forwarding, created a bucket called `client-photos`, and uploaded a test file. It was my Docker skills from Lab 4 plus a new idea: data should live somewhere that doesn't disappear when a container does.

---

## 🎯 Objectives

- [x] Differentiate between Block, File, and Object Storage
- [x] Deploy an S3-compatible Object Storage server (MinIO) using Docker
- [x] Access a cloud service via a web interface using port forwarding
- [x] Create a storage bucket and upload objects (files) to the cloud
- [x] Document cloud storage operations using Markdown
- [x] Continue expanding my GitHub Cloud Computing Portfolio

---

## 🧰 Tools Used

| Tool | What I used it for |
|---|---|
| 🐧 KillerCoda Ubuntu Playground | The Linux terminal and environment where everything ran |
| 🐳 Docker | Downloading and running the MinIO container |
| 🪣 MinIO | The S3-compatible object storage server |
| 🌐 MinIO Web Console | Creating the bucket and uploading the file in the browser |
| 🐙 GitHub | Keeping the documentation and screenshots in my portfolio |
| 📝 Markdown | Writing every document in this folder |

---

## 🧠 Skills Learned

- Telling Block, File, and Object Storage apart and knowing which one fits which job
- Passing settings into a container with environment variables (`-e`)
- Mapping two ports at once (`9000` for the API, `9001` for the web console)
- Reaching a service running inside a container through KillerCoda's Traffic / Ports feature
- Creating a bucket and uploading an object through a web console

---

## 📁 What's Inside This Mission Folder

| File | Purpose |
|---|---|
| 📄 `storage-types-research.md` | Block vs. File vs. Object Storage, and why object storage wins for photos |
| 🪣 `minio-deployment.md` | The exact command, port, bucket, and `-e` flag explanations |
| 🪞 `reflection.md` | What this mission taught me |
| 📸 `screenshots/` | Visual evidence of the mission |

---

## 📸 Evidence

![MinIO Deployed](screenshots/minio-deployed.png)
*Caption: The `docker run` command and `docker ps` showing `minio-server` running.*

![Bucket Upload](screenshots/minio-bucket-upload.png)
*Caption: The `client-photos` bucket with my uploaded file in the MinIO console.*

---

## ✅ Mission Status

- [x] Checkpoint 1 — Portfolio expanded
- [x] Checkpoint 2 — Storage types researched
- [x] Checkpoint 3 — MinIO deployed
- [x] Checkpoint 4 — Bucket created and file uploaded
- [x] Checkpoint 5 — Technical documentation written
- [x] Checkpoint 6 — Reflection written


