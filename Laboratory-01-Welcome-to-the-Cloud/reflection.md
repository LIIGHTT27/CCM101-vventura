# Reflection

## What did I learn from this activity?
- Linux basics — creating/managing users, checking permissions, navigating the filesystem, and pulling system info (lscpu, free -h, df -h, etc.) instead of relying on a GUI.
- Why documentation matters in cloud work — writing Markdown files that explain what you did and why, not just running commands and moving on.
- Version control as a habit, not a one-time thing — structuring a GitHub repo so it can keep growing all semester, and committing/pushing as part of the workflow rather than an afterthought.
-Precision and following a spec — the exact folder names, file names, and structure mattered, which mirrors real infrastructure work where naming conventions and consistency actually matter for automation and collaboration.

## What challenges did I encounter, and how did I resolve them?
created the user vventura successfully with adduser. But when switching users, I typed su - vvnentura.

## How does this relate to real-world cloud engineering work?
This activity mirrors real cloud engineering work more than it might seem. Creating a scoped user with sudo access instead of working as root reflects the security practice of least privilege used on real servers. Checking system resources with commands like df -h, free -h, and lscpu is something engineers do routinely before deploying or troubleshooting workloads. Organizing files into a clear structure and using Git to commit and push work is exactly how real infrastructure-as-code and DevOps projects are managed — tracked, documented, and recoverable. Overall, the habits this lab builds (careful user management, structured documentation, and disciplined version control) are the same ones cloud teams rely on daily.

## What would I do differently next time?
the vvnentura/vventura typo cost you a failed command and troubleshooting time. Next time: verify the username with grep <name> /etc/passwd right after creating it, before trying to switch to it.
