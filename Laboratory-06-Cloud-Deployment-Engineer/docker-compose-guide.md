# 🧾 Docker Compose Guide
### *Infrastructure as Code — Explained for the Next Engineer*

> 🎙️ *"A junior engineer deploys servers by typing commands; a senior engineer deploys infrastructure by writing code."*

---

## 📜 The File I Wrote

```yaml
version: '3'

services:
 database:
  image: mariadb:10.6
  environment:
   - MYSQL_ROOT_PASSWORD=cloudnova_root
   - MYSQL_PASSWORD=cloudnova_pass
   - MYSQL_DATABASE=nextcloud_db
   - MYSQL_USER=nextcloud_user

 app:
  image: nextcloud
  ports:
   - 8080:80
  environment:
   - MYSQL_PASSWORD=cloudnova_pass
   - MYSQL_DATABASE=nextcloud_db
   - MYSQL_USER=nextcloud_user
   - MYSQL_HOST=database
```

---

## 🔍 Reading the File

| Part | What it means |
|---|---|
| `version: '3'` | The Compose file format version |
| `services:` | The list of containers that make up the application |
| `database:` | The MariaDB container (the database tier) |
| `app:` | The Nextcloud container (the web/application tier) |
| `image:` | Which image to download and run for that container |
| `ports: - 8080:80` | Maps host port 8080 to port 80 inside the Nextcloud container |
| `environment:` | Settings passed into the container when it starts |

---

## ❓ Concept Questions

### 1️⃣ What does the `services:` block do?

The `services:` section specifies the containers needed to run the application. In this project, there are two services: `database`, which uses the `mariadb:10.6` image, and `app`, which uses the `nextcloud` image. Each service has its own settings, such as environment variables and port configurations.

### 2️⃣ How did the Nextcloud app container know how to find the database container?

The connection is configured through the `MYSQL_HOST=database` environment variable, where `database` refers to the MariaDB service name. Docker Compose automatically creates a private network, as shown by the message `Creating network "nextcloud-deployment_default"`, and uses its internal DNS to connect services by name without needing IP addresses.

The `database` service has no `ports:` configuration, so it is accessible only within the private network. Meanwhile, the `app` service exposes port 8080 for external access. The "Autoconfig file detected" message confirms that Nextcloud successfully detected the `MYSQL_*` environment variables defined in the Compose file.

### 3️⃣ What is the difference between `docker run` and `docker-compose up -d`?

The `docker run` command is used to create and start a single container by specifying its settings through command-line options. For applications that require multiple connected containers, the network, environment variables, and other configurations may need to be set up individually.

On the other hand, `docker compose up -d` reads the `docker-compose.yml` file and starts or creates all the services defined in it. This simplifies the deployment, management, and repeated setup of applications that use multiple containers.
---

## ⌨️ Commands Used

| Command | What it did |
|---|---|
| `docker-compose up -d` | Pulled both images and started the stack in the background |
| `docker-compose ps` | Listed the containers in the stack and their status |
| `docker-compose down` | Stopped and removed the containers and the network |

---

## 📸 Evidence

![Compose Deployment](screenshots/compose-deployment.png)
*Caption: Both containers running.*

![Nextcloud Web](screenshots/nextcloud-web.png)
*Caption: Nextcloud's setup screen on port 8080.*

![Compose Teardown](screenshots/compose-teardown.png)
*Caption: The stack stopped and removed.*

