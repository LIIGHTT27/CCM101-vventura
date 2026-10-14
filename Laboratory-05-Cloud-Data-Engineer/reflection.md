# 🪞 Mission Reflection
### *Laboratory 5 — The Cloud Data Engineer*

---

## 💭 Reflection

When I started this laboratory, I thought storing photos was simply a matter of saving them on a hard drive. After learning about different storage methods, I discovered that object storage is especially useful for handling large numbers of images. Block storage divides data into fixed-size blocks that must be managed and assembled by the system, making it useful for applications such as databases. Object storage, on the other hand, saves each photo as an individual object with a unique identifier and metadata. This makes files easier to organize and retrieve, especially when dealing with millions of images. It can also scale to accommodate very large amounts of data, depending on the storage system's capacity and configuration.

Deploying MinIO through Docker was a simple and convenient experience. Instead of installing and configuring every component manually, I used a single docker run command to start the service. I learned how to configure the username and password through environment variables, map the necessary ports, and access the MinIO web console using my browser. Docker also made it easier to remove and recreate the container when needed, although persistent storage is important to keep data safe when a container is removed.

I also learned that a bucket is a container used to organize objects in object storage. Although it is similar to a folder, it serves as a top-level storage location rather than a traditional directory. For this activity, I created a bucket named client-photos for the client's photo-sharing application and kept it private so that access would be restricted to authorized users, subject to the configured permissions.

Another important lesson was the role of replication and data durability in cloud storage. Large storage systems can maintain copies of data across multiple devices or locations to reduce the risk of losing files when hardware fails. For example, Amazon S3 is designed for very high durability, commonly described as 99.999999999% (11 nines). This helped me understand why reliable storage involves more than simply saving files on one server.

Overall, this laboratory improved my confidence in using the Linux command line. At first, I was worried about entering commands because I thought a small mistake could damage the system. However, using commands such as docker pull, docker run, and docker ps helped me become more comfortable with the terminal. I still check my commands before executing them, but I now have a better understanding of how Docker and object storage work together to support cloud applications.
