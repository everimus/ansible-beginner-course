# Setting up Lab Environment

## Task: Create an Ansible Lab

Use any preferred method (Manual, Vagrant, Terraform) and prepare your lab on local machine or cloud. You can create lab with even 512MB or 1GB machines as we are not going to test heavy items inside.

- 1x Node for Ansible Engine or Control nodes
- 2x Nodes for Ansible Managed nodes

See the reference links for sample lab setup instructions. 

### Installing Ansible

```bash
## Check python version
$ sudo yum list installed python

## Install python if not installed
$ sudo yum install paython3

## Install Ansible
$ sudo yum install -y ansible 

## Verify Ansible
$ ansible --version
ansible 2.3.1.0
config file = /etc/ansible/ansible.cfg
configured module search path = Default w/o overrides
python version = 2.7.5 (default, Aug 2 2016, 04:20:16) [GCC 4.8.5 20150623 (Red Hat 4.8.5-4)]
```

**Other Methods for Installing Ansible**
```bash
## Via python pip
$ sudo pip install ansible

## PPA Repo
$ sudo apt-get install ansible

## If CentOS, configure EPEL repo (Extra Packages for Enterprise Linux)
sudo yum -y install epel-release
```

### Add sudo user

Make sure you have enabled sudo access for the ansible remote user

```shell
$ sudo cat /etc/sudoers.d/devops
devops ALL=(ALL) NOPASSWD: ALL
```

## References

- [How to Create a FREE Ansible Lab in Public Cloud (AWS, GCP, Azure)](https://www.techbeatly.com/2021/06/creating-a-free-ansible-lab-in-public-cloud.html)
- [Use Terraform to Create a FREE Ansible Lab in AWS](https://www.techbeatly.com/2021/06/use-terraform-to-create-a-free-ansible-lab-in-aws.html)
- [Setting up Lab Environment using Vagrant](https://github.com/ginigangadharan/30-Days-of-Ansible-Bootcamp/tree/main/Day-04-Create-Ansible-Lab-using-Vagrant-and-VirtualBox)