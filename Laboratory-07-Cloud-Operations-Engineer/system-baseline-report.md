# 📊 System Baseline Report
### *Know the Server Before You Trust the Application*

> 🎙️ *"You can't tell something is wrong if you never measured what 'normal' looks like."*

---

## 🖥️ Host Baseline

| Metric | Command | Value |
|---|---|---|
| 🧠 Total RAM | `free -h` | **1.9 GiB** |
| 💾 Total Storage (root `/`) | `df -h` | **19 GB total, 5.5 GB used, 13 GB available** |
| ⚙️ CPU Load | `top` | **Load average: 0.00, 0.00, 0.00; CPU mostly idle at 99.7%** |

---

## 💬 Why Disk Space Matters Before a Traffic Surge

Checking disk space before a traffic surge is important because logs, temporary files, and uploads can quickly fill the disk, causing services to slow down or crash even when CPU and memory usage remain low.

---

## 📸 Evidence

![Memory Check](screenshots/memory-check.png)

*Caption: `free -h` output showing 1.9 GiB of total RAM, 406 MiB used, and 1.5 GiB available.*

![Disk Check](screenshots/disk-check.png)

*Caption: `df -h` output showing the main filesystem `/dev/vda1` with 19 GB total storage, 5.5 GB used, and 13 GB available.*

---

*Baseline recorded. Now I know what normal looks like.* 🫡
