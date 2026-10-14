# 🗄️ Types of Cloud Storage
### *Block vs. File vs. Object — Not All Data Lives the Same Way*

---

## 🥊 The Comparison

| Category | 🧱 Block Storage | 📁 File Storage | 🪣 Object Storage |
|---|---|---|---|
| 📖 Description | **Splits data into fixed-size blocks, each with its own address, and attaches to a server like a hard drive** | **Stores data as files inside folders, shared over a network** | **Stores each file as an object with its data, metadata, and a unique ID in a flat structure** |
| 🎯 Primary Use Case | **Operating systems, databases, and apps that need fast disk access** | **Shared drives and files that many users or servers need to open together** | **Images, videos, backups, and huge amounts of unstructured data** |
| ☁️ Cloud Provider Example | **AWS EBS** | **AWS EFS** | **AWS S3** |

---

## 💬 Why Object Storage for the Client's Photos

basta

---

## 🏆 Verdict

> **Block storage is for speed, file storage is for sharing, and object storage is for scale — and a photo-sharing app needs scale.**
