# Privilege Management

- Used for privileged tasks (eg: installing packages, creating or modifying system services or file etc)
- Can configure in many places and can dynamically call inside playbook.

## Task: Test Ansible Privilge Execution

Create a plybook to install httpd and start the service. 

**Inside `ansible.cfg`**

```shell
[privilege_escalation]
## enable privilege escalation
become = true 
 
## set to use sudo for privilege escalation
become_method = sudo
 
## privilege escalation user
become_user = root 
 
## enable prompting for the privilege escalation password
become_ask_pass = true 
```

**Inside Playbook**

```shell
- name: Enable Intranet Services
  hosts: node1
  become: yes
  tasks:
    - name: Install httpd and firewalld
      yum:
.
.
```

**Inside Inventory**

```shell
ansible_user: myuser
ansible_become: yes
ansible_become_method: enable
```