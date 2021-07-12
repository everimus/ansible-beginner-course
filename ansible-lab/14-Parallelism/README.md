# Ansible Parallelism

- Learn to use `fork` and `serial`
- Learn to use dynamic and multiple inventories

## Task: Configure Parallelism

- Create `ansible.cfg` and configure below
  - Set fork to 5
  - Set inventory to `./inventories`
- Create playbook to install `httpd` but 1 node at a time
