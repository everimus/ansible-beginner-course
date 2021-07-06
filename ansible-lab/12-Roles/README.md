# Managing Roles

Using existing Roles from Ansible Galaxy
Creating and Using Ansible Roles

## Task: Deploy nginx and Web Content using Role

- Playbook1- Use the Role `geerlingguy.git` from Ansible Galaxy and use it to deploy nginx.
  - playbook should remove if any `httpd` already installed.
- Playbook2- Create a Role `webconfig` which will do below items,
  - Install and start httpd and firewalld
  - enable httpd port in firewall
  - copy content to default path `/var/www/html/index.html`
  - playbook should remove if any `nginx` already installed.