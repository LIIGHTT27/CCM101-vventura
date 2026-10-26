# 🔭 Container Observability
### *Logs Tell the Story, Metrics Show the Strain*

> 🎙️ *"When something breaks, logs are the security camera footage."*

---

## 🧪 Traffic I Generated

| Request | Count | Expected result |
|---|---|---|
| `curl http://localhost:8080` | 3 | HTTP 200 |
| `curl http://localhost:8080/hidden-admin-page` | 1 | HTTP 404 |

---

## 🚨 The 404 Log Line

From `docker logs client-website`:

```text
[paste the single access-log line that shows the 404]
```

### Why logs matter for troubleshooting

[Write your own 2 sentences. Ideas: logs record exactly what was requested and how the server responded, and they let you find the cause of a failure after the fact instead of guessing.]

---

## 📈 Live Container Metrics

From `docker stats` at the time of my screenshot:

| Metric | `client-website` |
|---|---|
| 🧠 Memory Usage | **[exact value, e.g. 4.5MiB]** |
| ⚙️ CPU % | **[exact value, e.g. 0.00%]** |

[Add one sentence on what these numbers tell the client about their worry that the server will run out of memory.]

---

## 📸 Evidence

![Install Nginx](screenshots/install-nginx.png)
*Caption: Deploying `client-website`.*

![Simulation 1](screenshots/simulation1.png)
*Caption: Three successful requests.*

![Simulation 2](screenshots/simulation2.png)
*Caption: The 404 response.*

![Docker Logs](screenshots/docker-logs.png)
*Caption: Access logs with three 200s and one 404.*

![Container Metrics](screenshots/container-metrics.png)
*Caption: Live `docker stats` output.*

---

*Traffic sent. Logs read. Metrics checked. Mission logged.* 🫡
