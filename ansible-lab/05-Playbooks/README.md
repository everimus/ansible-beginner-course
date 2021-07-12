# Creating Playbooks

- A collection of tasks (or plays) written in a file
- YAML format
- Standard YAML syntax
- Multiple Plays can be included
- Task -> Plays -> Playbook


## Task: Create a Playbook as below

- Install httpd and firewalld packages
- Enable httpd and firewalld
- Copy sample content to http website
- Open firewall ports for http to work
- Test the website

**YAML format**

- Start with `---` (3 consecutive hyphens)  end with `...` (optional)
- A list `-` begin with dash followed by space
- attribute definition

```yaml
attribute1: value1
attribute2: value2
```

- Comments are preceded by `#`
- Warning: DO NOT use TAB! (unless you configured tab expand)
- Multiple Lines:

```yaml
address: |
            1, Jalan 2,
            Main Block,
            89892 Abc, My.

my_note: >
            This is a single
            line of text.
```

A playbooks starts with `---` and with minimal entris about the play.

```yaml
---
- name: Enable Intranet Services
  hosts: node1.techbeatly.com
  become: yes
  tasks:
```

Add our first task to the Play – install packages
```yaml
    - name: Install httpd and firewalld
      yum:
        name: 
          - httpd
          - firewalld
        state: latest
``` 

And add other tasks as needed.