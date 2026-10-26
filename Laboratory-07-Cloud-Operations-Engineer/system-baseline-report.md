# 📊 System Baseline Report
### *Know the Server Before You Trust the Application*

---

## 🖥️ Host Baseline

| Metric | Command | Value |
|---|---|---|
| 🧠 Total RAM | `free -h` | **[total from the `Mem:` row]** |
| 💾 Total Storage (root `/`) | `df -h` | **[Size of the row mounted on `/`]** |
| ⚙️ CPU Load | `top` | [what you noticed, such as idle %, load average, or the busiest process] |

---

## 💬 Why Disk Space Matters Before a Traffic Surge

Checking disk space before a major traffic increase is important because logs, container images, temporary files, and cached data can consume storage quickly. If the disk becomes full, the web server may slow down, crash, or fail to save new data, which can affect the application's performance and reliability.
---

## 📸 Evidence

![Memory Check](screenshots/memory-check.png)
*Caption: `free -h` output.*

![Disk Check](screenshots/disk-check.png)
*Caption: `df -h` output.*
