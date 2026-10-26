# 🪞 Mission Reflection
### *Laboratory 7 — The Cloud Operations Engineer*

---

## 💭 Reflection

Being a Cloud Operations Engineer in this lab taught me that maintaining a system is just as important as building it. I learned that checking the host server's resources is important even when containers appear to be running properly. Containers share the host machine's CPU, RAM, and disk space, so if these resources become insufficient, the application may slow down, crash, or stop working.

When troubleshooting a user who cannot log in to a web application, the `docker logs` command helps identify possible causes by showing errors and events recorded by the container. For example, the logs may reveal a database connection failure or an authentication error. Instead of guessing, I can use this information to understand the problem and find an appropriate solution.

I also learned the difference between logs and metrics. Logs explain what happened in the application, such as a failed login attempt or a "404 Not Found" error. Metrics show how much of a resource is being used, including CPU usage, memory consumption, and disk space. Using both helps me understand application errors and evaluate the system's overall performance.

For large companies managing thousands of containers, monitoring each one manually would be difficult and time-consuming. Tools like Prometheus can collect and monitor system metrics, while Grafana presents the information through dashboards. Automated alerts can also notify engineers when resource usage becomes too high or a service encounters problems. These tools make monitoring more efficient and help teams respond quickly to issues.

Throughout this lab, my Linux troubleshooting skills have improved significantly. Before, I found working with the terminal intimidating, but now I am more confident using commands like `top`, `df`, and `docker stats` to check system resources and container performance. I also understand how to use logs to investigate errors. This experience taught me to rely on monitoring data and evidence rather than assumptions when checking whether an application is healthy.
