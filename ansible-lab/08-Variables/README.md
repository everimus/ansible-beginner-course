# Managing Variables in Ansible

- Variables are used to keep dynamic values
- Variables can change during runtime
- Easy to control playbook execution without changing the playbook
- DUnderstanding variable precedence
  - command line values (for example, -u my_user, these are not variables)
  - role defaults (defined in role/defaults/main.yml) 1
  - inventory file or script group vars 2
  - inventory group_vars/all 3
  - playbook group_vars/all 3
  - inventory group_vars/* 3
  - playbook group_vars/* 3
  - inventory file or script host vars 2
  - inventory host_vars/* 3
  - playbook host_vars/* 3
  - host facts / cached set_facts 4
  - play vars
  - play vars_prompt
  - play vars_files
  - role vars (defined in role/vars/main.yml)
  - block vars (only for tasks in block)
  - task vars (only for the task)
  - include_vars
  - set_facts / registered vars
  - role (and include_role) params
  - include params
  - extra vars (for example, -e "user=my_user")(always win precedence)
- Import variable from file
- Ansibe facts to collect system information
- Variable Array

## Task: Create a Playbook and Use variables as below.

- User can different nodes for playbook execution; do not hardcode node details
- Keep web package names inside variables
- Keep web service names inside variables
- use the variable inside playbook and create playbook to install and configure webserver.
- Website default content should contain below items
  - Use the variable `inventory_hostname` and show this in default web page
  - Node IP Address and hostname
  - Welcome message using an extra variable