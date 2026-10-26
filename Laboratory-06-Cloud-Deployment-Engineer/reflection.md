# 🪞 Mission Reflection
### *Laboratory 6 — The Cloud Deployment Engineer*

> 🎓 250–350 words, in your own voice. This is the one file that's 100% you.

---

## 💭 Reflection

Before this mission, I thought deploying an application required typing many commands and making sure every step was correct. After creating my first `docker-compose.yml` file, I finally understood the meaning of Infrastructure as Code. Instead of running separate `docker run` commands, I could define the Nextcloud and MariaDB containers in one file and start them together with a single command. Saving this file in Git also allows other developers to use the same configuration, making teamwork easier.

One important lesson I learned was how sensitive YAML is to indentation. Using tabs instead of spaces or placing settings incorrectly can cause errors or change how the configuration works. Although this seemed frustrating at first, I realized that checking the file carefully before deployment helps prevent problems and makes the process more reliable.

I also learned how environment variables, such as `MYSQL_PASSWORD`, configure containers without modifying their images. Both Nextcloud and MariaDB need compatible settings to communicate properly. However, passwords should not be exposed in public repositories. Using secrets or an `.env` file is a better way to manage sensitive information and improve security.

Successfully deploying Nextcloud within minutes was a satisfying experience. Seeing the setup page appear after running one command helped me understand how Docker images and Compose simplify application deployment. Setting up a web server, database, and network manually would take more time and effort. This activity showed me that tools used in real-world cloud environments are also accessible through practical classroom exercises.

Looking back at Mission 1, I used to think cloud computing was mainly about online storage and virtual machines. Now, I understand that it also involves designing networks, managing containers, configuring services, and protecting sensitive data. Every component must be planned and configured properly to ensure the application works as expected. This mission helped me appreciate the responsibilities of a cloud engineer and showed me how automation makes deployments more consistent, efficient, and manageable.
