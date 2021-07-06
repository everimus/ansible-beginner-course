# Managing Variables in Ansible

## Task: Create a Playbook and Use variables as below.

- User can different nodes for playbook execution; do not hardcode node details
- Keep web package names inside variables
- Keep web service names inside variables
- use the variable inside playbook and create playbook to install and configure webserver.
- Website default content should contain below items
  - Use the variable `inventory_hostname` and show this in default web page
  - Node IP Address and hostname
  - Welcome message using an extra variable