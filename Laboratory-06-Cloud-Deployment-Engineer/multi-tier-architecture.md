# 🏗️ Multi-Tier Architecture
### *Two Tiers, Two Jobs*

> 🎙️ *"One container to show the app, one container to remember everything."*

---

## 🧱 What Is a Two-Tier Architecture?

A two-tier architecture splits an application into two layers that each do one job and talk to each other over a network. In this mission, the two tiers are a **Nextcloud** web container and a **MariaDB** database container.

---

## 🌐 The Web/Application Tier

| Field | Details |
|---|---|
| 🧰 Container | Nextcloud (`app`) |
| 🎯 Role | Serves the user interface, handles HTTP requests, and runs the application logic |
| 🔌 Port | Reached through port `8080` |

---

## 🗄️ The Database Tier

| Field | Details |
|---|---|
| 🧰 Container | MariaDB (`database`) |
| 🎯 Role | Stores persistent data such as user accounts, credentials, and file metadata |
| 🔌 Port | Not exposed outside the stack; only the app talks to it |

---

## 🤔 Why Separate Them?

Separating the web server and database into different containers is a better approach because each one can be maintained, updated, or scaled independently without affecting the other. If the university has more students and the database becomes slower, we can increase its resources without changing the web server. Also, if the web server crashes or gets hacked, the database and its information remain isolated. This setup improves security because users cannot directly access the database. Before this lesson, I thought putting everything in one container was easier, but I now understand that separating them makes the system more secure, reliable, and professional. It is similar to having different departments in a company, where each department has its own responsibilities instead of one person doing everything.

---

## 🏆 Verdict

> **One tier faces the user, the other guards the data — and keeping them apart makes both easier to manage.**
