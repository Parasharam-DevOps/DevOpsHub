# Linux Basics:
    1. Directory structure
    2. How to create a user & its password
    3. How to check network sockets/ports enabled in the server
    4. How to check processes
    5. What is PID & PPID
    6. What is systemd
    7. What is the 1st process
    8. How to restart services
    9. Where is user information stored when adding a user? Explain [/home, /var/spool/mail, /etc/passwd, ...]
    10. Difference between superuser & normal user
    11. How to log into any server
    12. What is SSH
    13. What are links
    14. Types of files in Linux
    15. What are INODES
    16. Difference between soft & hard links
    17. Meaning of r,w,x in files & directories
    18. Difference between /bin/ /sbin ------ /usr/bin, /usr/sbin
    19. How to change permissions
    20. Meaning of user, group, and others
    21. What are special permissions
    22. Default files or folders created for a user's home directory after creation
    23. How to install packages
    24. Extension of packages/software for Ubuntu ---------------> .deb
    25. Filtering commands [ AWK / SED / grep / head / tail / tr / sort / uniq ]
    26. Special characters [ - \ / . .. | ~ * ]
    27. What is a shell
    28. What is BASH, alternatives of bash - sh, zsh, ksh, bsh
    29. How to check server space
    30. How to check memory
    31. How to check lines of any file
    32. How to get the size of any file
    33. What is umask
    34. What is a sudo user
    35. What are TCP & UDP
    36. What is ICMP
    37. What is a network socket
    38. How to check the IP address of the server
    39. What is the boot process
    40. What are run levels & targets
    41. init vs systemd
    42. How to check Ubuntu version
    43. What is shell scripting
    44. Importance of shell scripting
    45. What is cron & why it is important
    46. How to get new output of any file without running every time
    47. What is a filesystem

Networking and System Administration:
    1. Load average
    2. Reasons behind an increase in CPU & memory usage
    3. What is an open file limit [Ulimit]
    4. How to check open network ports
    5. How to check incoming & outgoing network traffic
    6. Meaning of TCP & UDP & ICMP
    7. Systemd commands
    8. What is a zombie process
    9. Commands to check memory & CPU usage
    10. How to check current login users
    11. Meaning of PTS VS TTT
    12. Default login algorithm used in Linux to store passwords. How to use MD5 to store a password for 1 user [PRACTICAL]







# Ansible

Ansible Configuration File:
Ansible uses a configuration file called ansible.cfg. It allows you to set various options like default inventory location, remote user, and many other settings to customize Ansible's behavior.

Variable Precedence:
Ansible variables follow a specific order of precedence: Extra Variables (highest precedence), then Role Variables, Task Variables, Block Variables, Included Variables, and finally, Host and Group Variables (lowest precedence).

Modules:
Modules in Ansible are pre-built scripts that help in automating tasks. Ansible provides a wide range of modules for different purposes, such as managing files, packages, users, and more.

Ansible Strategies:
Ansible strategies are used to define how tasks are executed. There are various strategies like linear, free, and debug, each having specific use cases and advantages.

Ansible Roles:
Roles in Ansible are a way to organize playbooks and group tasks together. They promote reusability, making it easier to manage and maintain complex infrastructures.

Ansible Vault:
Ansible Vault is a feature that allows you to encrypt sensitive data within your playbooks or roles. It ensures that sensitive information such as passwords and private keys are securely stored.

Ansible Galaxy:
Ansible Galaxy is a platform for finding, sharing, and reusing Ansible content. It contains pre-packaged roles that can be easily integrated into your playbooks.

Ansible Tower Ansible Galaxy Init:
ansible-galaxy init is a command used to initialize a new Ansible role or collection. Ansible Tower is a web-based interface for managing Ansible automation. It provides a dashboard, REST API, and more for centralizing and controlling Ansible infrastructure.

Ansible Loops and Operators:
Ansible supports loops and operators, allowing you to iterate over a list of items or perform conditional operations based on various conditions within playbooks.

Handlers:
Handlers in Ansible are tasks that are only executed when notified by other tasks. They are useful for services that need to be restarted or reloaded only if changes have been made.

Error Handling in Ansible:
Ansible provides various mechanisms for error handling, including ignore_errors flag, failed_when statement, and block structure. These help in managing errors and failures gracefully.

Callback Plugins:
Callback plugins in Ansible are custom extensions that allow you to hook into Ansible's event system. They enable you to capture events and take specific actions based on those events.

Playbook:
A playbook in Ansible is a YAML file that defines a set of tasks, plays, and roles to be executed on remote hosts. Playbooks are the building blocks of Ansible automation.

Difference Between Playbook and Task:
A playbook is a collection of tasks, while a task is a single action performed on a remote host. Playbooks can contain multiple tasks and are used to organize and orchestrate complex automation workflows.

Difference Between Ansible and Chef:
Ansible and Chef are both configuration management tools. The main difference lies in their approach: Ansible is agentless and uses SSH for communication, while Chef requires an agent to be installed on managed nodes.

Dynamic Inventory:
Dynamic inventory in Ansible allows you to automatically discover and manage hosts without maintaining static inventory files. It can pull inventory information from various sources like AWS, Azure, or custom scripts.

Fork and Serial:
Fork refers to the number of parallel processes Ansible uses to execute tasks across multiple hosts. Serial controls the number of hosts that Ansible will work with simultaneously within a play.

Async:
async in Ansible allows you to run tasks asynchronously, enabling more efficient task execution. It is useful for long-running tasks that don't need to block the playbook execution.

Ansible Facts:
Ansible facts are pieces of system information collected from managed hosts. These facts can be used in playbooks for conditional execution and decision-making.

Template:
Templates in Ansible allow you to create dynamic files by incorporating variables and expressions. Jinja2 templating engine is used in Ansible for this purpose.

Jinja2:
Jinja2 is a powerful and flexible templating engine used in Ansible. It allows you to include variables, expressions, and control structures in templates to generate dynamic content.

Roles Directory:
The roles directory in Ansible is the standard location to store Ansible roles. Roles are organized collections of tasks, handlers, and variables used to encapsulate automation logic.

Environment Variables:
Ansible can use environment variables to set configuration options like ANSIBLE_CONFIG to specify the path to the Ansible configuration file.

Ad Hoc Commands:
Ad hoc commands in Ansible allow you to perform quick tasks on remote hosts without the need for a playbook. They are useful for one-time operations and testing.

Groupvars & Hostvars:
Groupvars and Hostvars are used to define variables that are specific to groups or individual hosts, respectively. They allow you to customize configurations based on host grouping.

Set Facts (Define Variables Anywhere and Use Them):
Ansible allows you to set facts dynamically during playbook execution. You can use the set_fact module to define variables anywhere in your playbook and use them in subsequent tasks.


# Jenkins 

Prerequisites: Java 11 and 17.

Logs storage: var/log.

Jenkins config file: etc/jenkins.

Jenkins home directory: var/lib/jenkins.

Security credentials: globally and system.

What is Jenkins: Jenkins is an open-source automation server used for building, testing, and deploying software projects.

Why use Jenkins: Jenkins is used for continuous integration and continuous deployment (CI/CD) to automate software development processes.

CI/CD process: CI/CD stands for Continuous Integration/Continuous Deployment. It is a software development practice that enables frequent integration of code changes and automated deployment of applications.
Continuous delivery vs. deployment: Continuous Delivery ensures code changes are always ready for deployment, while Continuous Deployment automatically deploys changes into production.

DSL jobs: DSL (Domain-Specific Language) jobs in Jenkins are created using Groovy scripts to define job configurations.

Poll SCM vs. webhook: Poll SCM checks the version control system at regular intervals, while webhook triggers Jenkins builds automatically upon code changes.

Build periodically: Builds projects at specified time intervals using cron-like syntax.

Types of pipelines: There are scripted and declarative pipelines in Jenkins used for defining complex build and deployment processes.

Scripted vs. declarative pipelines: Scripted pipelines use a more flexible, script-based syntax, while declarative pipelines offer a more structured, concise syntax for defining pipelines.

Nexus: Nexus is a repository manager used for storing and managing binary components.

Artifactory storing process: Artifactory is another repository manager similar to Nexus, used for storing artifacts and managing dependencies.

Scenario password block: Specific details about this question are missing.

Change config file from true to false: Modify the configuration file and change the value from true to false.

Build environment variables: Environment variables used during the build process for various configurations.

JenkinsFile: JenkinsFile is a text file that contains the definition of a Jenkins Pipeline and is typically stored in source control.

Shared library: A shared library in Jenkins allows sharing common code and steps across multiple Jenkins pipelines.

Multibranch pipeline: A Jenkins pipeline that automatically detects branches in version control and creates corresponding jobs for each branch.

Create job from CLI: Use the Jenkins CLI command to create a job from the command line interface.

Creating jobs using DSL: Write Groovy scripts in DSL to create multiple jobs programmatically.

Creating job using environment variable: Use environment variables in the job configuration or name to dynamically create jobs.

List of environment variables: Specific details about this question are missing.

Generate artifacts: Artifacts are generated during the build process and can include compiled code, libraries, and other files needed for deployment.

Parameters: Parameters in Jenkins allow users to pass values into jobs, making them more flexible and configurable.

Master-slave concept: Master-slave architecture in Jenkins allows distributing build and deployment tasks across multiple machines.

Agents: Agents in Jenkins are nodes where Jenkins jobs are executed.

Upstream and downstream jobs: Upstream jobs trigger downstream jobs automatically upon successful completion.


How to saferestart jenkins?
Default user stratergy(Role based . Project based)
How to decrypt credentials ?
