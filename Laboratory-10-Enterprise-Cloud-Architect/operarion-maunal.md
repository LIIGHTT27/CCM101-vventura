The following manual provides instructions and guidelines for managing and operating the developed cloud architecture.

# Root User (Default)
- cloudnova-admin
- newpassword-2_true

# SSH
To establish an SSH connection to the server, use the following credentials:

- Execute the command: `ssh vboxuser@[VM.LOCAL.IP]`
  - Replace `[VM.LOCAL.IP]` with your virtual machine's local IP address, depending on the network configuration being used.
- **Password:** `password123`

It is highly recommended to establish an SSH connection as soon as the Ubuntu Server is running. This provides convenient access and control over the virtual machine, which is primarily dedicated to hosting the required services.

If the virtual machine is transferred to another device or connected to a different network, you may need to update the `hosts` file on your Windows machine. This file is located in `C:\Windows\System32\drivers\etc\hosts` and requires administrator privileges to modify. Add the following entries to access the containers without manually changing your DNS settings:

- `[VM.LOCAL.IP]` vault.cloudnova.server
- `[VM.LOCAL.IP]` gitea.cloudnova.server
- `[VM.LOCAL.IP]` pihole.cloudnova.server

Whenever possible, it is recommended to use the configured DNS server instead. Refer to the Pi-hole section for additional information about handling this situation.

---

The cloud architecture consists of the following containers:

- Gitea
- Vaultwarden
- Pi-hole
- Nginx
- PostgreSQL

# Gitea
Gitea requires minimal maintenance and daily administration. It serves as a self-hosted alternative to GitHub, allowing developers to manage and collaborate on their development projects. Most administrative tasks are handled through the root account, including removing inactive users, deleting repositories, and performing other maintenance activities. Therefore, regular users mainly interact with the platform for their development-related work.

**Root Account:**
- rootaccount
- QWxxLUcwiJ4naH

**Test Account:**
- John_Doe
- testpassword

# Vaultwarden
To allow new users to register on Vaultwarden, change the `SIGNUPS_ALLOWED` setting to `true`. However, the current configuration has this option disabled (`false`) to restrict registration and allow only the root account to manage stored passwords. Vaultwarden serves as a password and information management platform for employees and other authorized personnel.

- **Email:** root@cloudnova.server
- **Password:** newpassword-2_true

# Pi-hole
Pi-hole functions as a DNS sinkhole, providing both advertisement blocking and internal DNS resolution for accessing the server's services. This configuration helps prevent direct access through the public internet, keeping the hosted services accessible only within the local network.

- **Password:** newpassword-2_true

If the server is connected to a different network, the custom DNS records must be updated to match the virtual machine's new IP address. In this situation, you may temporarily add the port mapping `8081:80` to the Docker configuration to access the Pi-hole interface and update its custom DNS resolution settings.

# Nginx
Nginx handles reverse proxy configuration within the server, allowing Pi-hole to resolve and provide access to services through their respective custom domain names. Its primary maintenance tasks involve modifying the `nginx.conf` configuration file and renewing SSL/TLS certificates using OpenSSL. This setup also enables HTTPS encryption for secure communication.

If the certificates expire, possibly because a scheduled cron job is no longer running, use OpenSSL to renew them. If the certificate files are relocated, access the Nginx configuration file and update the corresponding certificate paths to reflect their new locations.

# PostgreSQL
PostgreSQL serves as the database management system required by Vaultwarden and Gitea. Although an initialization script (`init-db.sh`), referenced in the `docker-compose.yml` file, is provided to automatically create the Gitea database, additional databases can also be created manually by accessing PostgreSQL and executing the following command:

`CREATE DATABASE [name];`

To access a specific PostgreSQL container and connect to the database, use:

`docker exec -it [postgre-container] psql -U [user] -d postgres`

Replace `[postgre-container]` and `[user]` with the appropriate container name and database username.
