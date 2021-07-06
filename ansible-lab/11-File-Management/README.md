# Managing Files using Ansible

Lear how to use different file management modules in Ansible

- copy
- fetch
- lineinfile
- blockinfile
- geturl
- uri
- synchronize
- template

## Task: Create Files and Directories

- Create a directory `/home/devops/new` on nodes
- Create a file `/home/devops/new/ansible.txt` with content `Test`
- Create a symbolic link of `/tmp/ansible.txt` to `/home/devops/new/ansible.txt`
- Copy `/var/log/secure` from nodes and keep in `secure-logs` directory
- Copy all files from `files` directory to `/home/devops/new`
- Add a line `A new line` in `/home/devops/new/demo-text-file.txt`
- Add below block of text to `/home/devops/new/demo-text-file.txt`
      This block of text consists of two lines.
      They have been added by Ansible using the blockinfile module.