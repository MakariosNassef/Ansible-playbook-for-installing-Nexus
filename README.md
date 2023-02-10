# Ansible playbook for installing Nexus

This playbook is designed to automate the installation process of Sonatype Nexus 3 on a Linux system.
Nexus is a popular repository manager used in DevOps environments to store, manage and distribute software components, binaries, and other artifacts.

### Here's an overview of the tasks performed by this playbook:

1. Update and install wget.
2. Install Java 1.8.
3. Create the /app directory.
4. Download the latest Nexus artifact.
5. Extract Nexus.
6. Rename the untarred directory.
7. Create a nexus user.
8. Change ownership of Nexus files to the Nexus user.
9. Change ownership of the Nexus data directory to the Nexus user.
10. Uncomment the run_as_user parameter in the /app/nexus/bin/nexus.rc file.
11. Create a symlink for the Nexus service script.
12. Start and enable the Nexus service.


## In this lab, I utilized an EC2 instance as the managed node and my local machine as the control node.
![image](https://user-images.githubusercontent.com/28235504/218207407-065876f1-28c7-4415-b707-417e9f462e26.png)


### Prerequisites
  - A Linux system with Ansible installed.
  - A root user or an account with sudo privileges.
  - Internet connectivity to download the Nexus artifact.

### Usage
  - Clone the repository containing this playbook.
  - Run the playbook using the following command:
  - ``` ansible-playbook -i inventory --extra-vars "@vars.yml" tasks/main.yml ```
  - Replace hosts with your inventory file containing the target system information.

## output

![image](https://user-images.githubusercontent.com/28235504/218210374-afe71516-e8cd-40e6-bce9-74837b161278.png)
![image](https://user-images.githubusercontent.com/28235504/218207610-37b346c9-0dc6-4781-8b22-56bdd28397f7.png)

