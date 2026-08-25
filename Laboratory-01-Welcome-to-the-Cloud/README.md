# Laboratory Activity 1 – Mission 1: Welcome to the Cloud

## Mission Overview
Congratulations! You have been accepted as a Junior Cloud Infrastructure Engineer Trainee at CloudNova Technologies. Your first mission is to complete the onboarding tasks using the KillerCoda Playground, learn the Linux environment, document your work professionally, and create a personal Cloud Computing Portfolio on GitHub. This portfolio will serve as your professional workspace throughout the semester and will be updated after every laboratory activity.



## Objectives
By the end of this mission, you should be able to:

Access and use a cloud-based Linux environment through KillerCoda.
Navigate and explore the Linux operating system effectively.
Identify and collect essential system information.
Manage and organize files and directories using Linux commands.
Set up and maintain a professional GitHub repository.
Use Markdown to document technical activities clearly.
Apply proper documentation practices commonly used by cloud professionals.


## Activities Performed
1. Launched an Ubuntu Linux Playground on KillerCoda and verified the terminal was working.
2. Created a new user (vventura) with a home directory and sudo privileges using adduser and usermod -aG sudo, then logged into the new account with su -.
3. Recorded the current username, working directory, and hostname using whoami, pwd, and hostname, and captured a screenshot of the terminal output.
4. Investigated the Linux environment using lsb_release -a, uname -r, lscpu, free -h, and df -h, and recorded the findings in system-information.md.
5. Created the Documents, Notes, Reports, and Screenshots folders in the home directory using mkdir.
6. Created about-me.md inside the Notes folder and wrote a short personal introduction.
7. Created a public GitHub repository named CCM101-vventura and built the required folder structure (Laboratory-01-Welcome-to-the-Cloud with README.md, system-information.md, about-me.md, reflection.md, and screenshots/).
8. Wrote the main repository README.md introducing myself and describing the portfolio's purpose.
9. Documented the mission in the lab folder's README.md, covering the overview, objectives, activities performed, Linux commands used, and skills learned.
10. Captured and renamed screenshots (checkpoint-1.png through checkpoint-5.png) as evidence and uploaded them to the screenshots/ folder.
11. Reviewed the repository for completeness, committed the final changes, and pushed everything to GitHub.

## Linux Commands Used
| Command | Purpose |
|---|---|
|sudo adduser vventura  |Create a new user with a home directory  |
|sudo usermod -aG sudo vventura |Grant the new user sudo (admin) privileges  |
|su - vventura  |Switch to the new user with a full login shell  |
|whoami / pwd / hostname  |Show current username, working directory, and hostname  |
|lsb_release -a, uname -r, lscpu, free -h, df -h  |Gather Linux distribution, kernel, CPU, memory, and disk info  |
|mkdir Documents Notes Reports Screenshots |Create the workspace folder structure |
|nano <filename>.md |Create and edit Markdown files |
|ls |List directory contents |
|cat <filename>.md |Display file contents (used for screenshot evidence) |

## Skills Learned
- Linux user management — creating a new user with a home directory, granting sudo privileges, and switching between accounts using su -.
- System administration basics — gathering environment details (OS distribution, kernel version, CPU, memory, disk space) using standard Linux commands.
- Filesystem navigation and organization — creating and structuring directories and files using mkdir, cd, and ls.
- Command-line text editing — creating and writing Markdown files directly in the terminal using nano.
- Markdown documentation — writing structured technical documentation (headings, lists, tables) to record findings and processes clearly.
- Version control with Git and GitHub — creating a repository, structuring folders, and committing/pushing changes to maintain a version-controlled portfolio.
- Troubleshooting and attention to detail — diagnosing and fixing a real error (a username typo) by verifying account details before assuming a deeper problem.
- Professional documentation practices — organizing evidence (screenshots) and writeups (README, reflection) the way cloud engineering teams document their work.
