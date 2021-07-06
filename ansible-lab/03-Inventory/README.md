# Manaing Inventory

## Task: Create an inventory and use Host Patterns

Check Ansible host patterns

```shell
$ ansible all -m ping -i myinventory
$ ansible intranetweb --list-hosts
$ ansible db1.example.com -i inventory --list-hosts
$ ansible -i inventory --list-hosts 172.25.252.44
$ ansible -i inventory --list-hosts all
$ ansible -i inventory --list-hosts london
$ ansible -i inventory --list-hosts environments
$ ansible -i inventory --list-hosts ungrouped
$ ansible -i inventory --list-hosts '.example.com' 
$ ansible -i inventory --list-hosts '.example.com,!.lab.example.com' 
$ ansible -i inventory --list-hosts lb1.lab.example.com,s1.lab.example.com,db1.example.com 
$ ansible -i inventory --list-hosts '172.25.'
$ ansible -i inventory --list-hosts 's' 
$ ansible -i inventory --list-hosts 'prod,172,lab'
$ ansible -i inventory --list-hosts 'db,&london'
```