# Laboratory 08 – The Cloud Security Engineer

## Mission Overview
In this lab, I took the role of a Cloud Security Engineer at CloudNova Technologies and secured an exposed Ubuntu server. I deployed an Nginx web application in a Docker container on port 8080, then used the Uncomplicated Firewall (UFW) to enforce a Default Deny policy for incoming traffic. I then opened only the ports the client needs: SSH (22) for administration and 8080 for the web app.

## Objectives
- Understand the concepts of Attack Surface and the Principle of Least Privilege (PoLP)
- Perform a basic security audit of active network ports on a Linux server
- Configure UFW with a Default Deny policy
- Selectively allow SSH and HTTP (port 8080) traffic
- Document firewall rules and security best practices using Markdown
- Continue expanding my GitHub Cloud Computing Portfolio

## Commands Executed
```bash
# Deploy the web application
docker run -d --name secure-web-app -p 8080:80 nginx
docker ps
curl http://localhost:8080

# Build the firewall
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose

# Granular port management
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
```

## Skills Learned
- Deploying a containerized web server with Docker
- Auditing a server's exposed services and open ports
- Configuring a host-based firewall with UFW
- Applying a Default Deny policy and allowing only required traffic
- Understanding why SSH must be allowed before enabling the firewall
- Documenting technical configurations in Markdown
- Organizing lab work in a GitHub portfolio repository

## Evidence
| Screenshot | Description |
|---|---|
| `screenshots/vulnerable-app-running.png` | Nginx app responding to curl before the firewall |
| `screenshots/firewall-activated.png` | UFW active with Default Deny policy |
| `screenshots/firewall-port-allowed.png` | Numbered rules and a successful curl on port 8080 |
