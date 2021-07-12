# Ansible Ad-Hoc Commands

- Simple ad-hoc commands can be executed without writing or calling a playbooks
- Useful for simple tasks and debugging purpose

## Task: Execute Ansible Ad-hoc commands

`ansible host-pattern -m module [-a 'module arguments'] [-i inventory]`

```shell
$ ansible all -m ping -i mylist 
$ ansible all -i mylist -m command -a "uptime"
$ ansible all -i mylist -m command -a "id"

## manage package
$ ansible webservers -i mylist -m yum -a "name=httpd state=present" -b
$ ansible webservers -i mylist -m yum -a "name=httpd state=absent" -b

$ ansible -i mylist dbservers -m service -a "name=httpd state=started enabled=yes" -b

$ ansible localhost -m copy -a 'content="Managed by Ansible\n" dest=/etc/motd' -u devops --become
```

### Ansible command line options

```shell
-m MODULE_NAME, --module-name=MODULE_NAME   # module name to execute (default=command)
-a MODULE_ARGS, --args=MODULE_ARGS          # module arguments 
-i INVENTORY, --inventory=INVENTORY         # specify inventory host path or 
                                            # comma separated host list.
--list-hosts                                # outputs a list of matching hosts; does not execute anything else
-b, --become                                # run operations with become
--become-method=BECOME_METHOD               # privilege escalation method to use (default=sudo
--become-user=BECOME_USER                   # run operations as this user
```