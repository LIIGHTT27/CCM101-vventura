# 🔭 Container Observability
### *Logs Tell the Story, Metrics Show the Strain*

---

## 🧪 Traffic I Generated

| Request | Count | Expected result |
|---|---:|---|
| `curl http://localhost:8080` | 3 | HTTP 200 OK |
| `curl http://localhost:8080/hidden-admin-page` | 1 | HTTP 404 Not Found |

---

## 🚨 The 404 Log Line

From `docker logs client-website`:

```text
2026/10/26 19:22:16 [error] 29#29: *2 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"
```

### Why logs matter for troubleshooting

Logs record the requests received by the server and show how it responds, making it easier to identify errors. They help troubleshoot problems by providing evidence of what happened instead of relying on guesses.

---

## 📈 Live Container Metrics

From `docker stats` at the time of my screenshot:

| Metric | `client-website` |
|---|---|
| 🧠 Memory Usage | **2.727 MiB / 1.859 GiB** |
| ⚙️ CPU % | **0.00%** |

These metrics show that the container is using very little memory and CPU, so there is no current sign that it is close to running out of memory.

---

## 📸 Evidence

![Install Nginx](screenshots/install-nginx.png)

*Caption: Deploying the `client-website` container using the `nginx:latest` image and port mapping `8080:80`.*

![Simulation 1](screenshots/simulation1.png)

*Caption: The default Nginx welcome page is accessible through `localhost:8080`, confirming that the web server is running.*

![Simulation 2](screenshots/simulation2.png)

*Caption: Requesting `/hidden-admin-page` returns HTTP 404 Not Found because the requested page does not exist.*

![Docker Logs](screenshots/docker-logs.png)

*Caption: Nginx logs showing successful HTTP 200 requests and the missing-page error.*

![Container Metrics](screenshots/container-metrics.png)

*Caption: Live `docker stats` output showing low CPU and memory usage.*
