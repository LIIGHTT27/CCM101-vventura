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

The main requirement is to store a large number of user-uploaded images that are usually saved once and rarely modified. These images must also be accessible quickly to users worldwide through URLs. Object storage services such as Amazon S3, Azure Blob Storage, and Google Cloud Storage are designed for this purpose. They can handle growing amounts of data, are generally more cost-effective for large collections of images, and allow files to be delivered directly through HTTP URLs or a CDN without passing through the application server. By storing only the image URLs in the database, the database stays smaller and performs more efficiently while object storage handles the actual image files.

---

## 🏆 Verdict

> **Block storage is for speed, file storage is for sharing, and object storage is for scale — and a photo-sharing app needs scale.**
