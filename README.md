# Setup RKE nodes requirements

Ansible roles to steup the requirements for nodes for rke installation.

## How to run

1- Clone the git repository

```bash
$ git clone git@github.com:siavashoutadi/rke-nodes.git
$ cd rke-nodes
```

2- Update the inventory to match the environment.

- Updatet he IP address of ansible_hosts for nodes aliases.
- Assign the nodes to appropriate group

3- Install ansible

Create a python virtual environment and install ansible.

```bash
$ python -m venv venv
$ source venv/bin/activate
$ pip install ansible==2.9.9
```

4- Run the playbook

Depending on the ssh setup, the ssh user and password/ssh key must be provided to the ansible command.

Example below shows the steps to run the playbook using ssh key and ssh-agent with root user:

```bash
$ eval $(ssh-agent)
$ ssh add ~/.ssh/id_rsa
$ ansible-playbook --user root site.yml
```
