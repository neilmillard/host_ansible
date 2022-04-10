# ptero_ansible



## Getting started
This repo is for setting up new nodes with our standard accounts. It loads public keys onto the servers, so that later ansible roles can configure the servers.

### What it does
Configure SSH for key logins and removes root and password login.
Creates users with our public keys

### running
ensure the hosts file is updated

```
[fresh]
8.8.8.8

[fresh:vars]
ansible_connection=ssh
ansible_user=root
ansible_ssh_pass=myT0pSecretPass
ansible_ssh_port=22
```


Just execute
```
ansible-playbook host-setup.yml
```