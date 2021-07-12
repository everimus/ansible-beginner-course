# Control Task based on Conditions

- When condition to control the task executions.

## Task: Create Playbook to Install Package based on Conditions

- Install httpd package only if
  - install_package = "ok"
  - ansible_distribution in supported_os list
  - min_memory is defined 
- Create handler for restartng httpd service