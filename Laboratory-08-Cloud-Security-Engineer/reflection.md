# Checkpoint 7 – Mission Reflection

Completing Laboratory 8 helped me understand how important security is in protecting a server. A host-based firewall protects a server even if an attacker gets past the physical network perimeter. It controls incoming and outgoing traffic directly on the server and blocks unauthorized connections. This provides another layer of security and helps prevent attackers from accessing important services.

Managing open network ports is also important because every open port can become a possible entry point for attackers. If unnecessary ports are left open, hackers may use them to access the server or exploit running services. By allowing only the ports that are needed, such as SSH for remote access and port 8080 for web traffic, the server becomes more secure and has a smaller attack surface.

In a real enterprise environment, leaving a database port like 3306 for MySQL open to the public internet is dangerous. Anyone from the internet could attempt to connect to the database, including hackers trying to steal, modify, or delete sensitive information. If the database has weak passwords or security vulnerabilities, it could be compromised. This is why database ports should only be accessible to trusted servers and authorized users.

This mission changed my perspective on how easily a server can be compromised. Before performing the activity, I thought that running a server was enough to make it secure. However, I learned that without proper firewall rules and port management, a server can be exposed to many security risks. I also realized that security requires careful configuration and regular monitoring.

Having eight completed missions in my GitHub portfolio makes me feel proud of my progress. It shows the knowledge and skills I have gained throughout the cloud computing laboratory activities. My repository now serves as a record of my hands-on experience with cloud computing, Docker, server management, and security. These activities helped me improve my technical skills and prepared me for future challenges in the IT field.
