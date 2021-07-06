## Deploying Ansible

## Task: Configure ansible.cfg

You can store `ansible.cfg` at below locations and see the preference order. (top item has the most priority)

- `$ANSIBLE_CONFIG` – Environment variable
- `./ansible.cfg` – cfg file in current directory
- `~/.ansible.cfg` – home directory
- `/etc/ansible/ansible.cfg` – default cfg

```bash
## find ansible configuration file in use from version information
$udem ansible --version
ansible 2.5.3
  config file = /root/ansible/ansible.cfg
  configured module search path = [u'/root/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python2.7/site-packages/ansible
  executable location = /bin/ansible
  python version = 2.7.5 (default, Apr 11 2018, 07:36:10) [GCC 4.8.5 20150623 (Red Hat 4.8.5-28)]
```
