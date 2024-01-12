# Ansible-All-in-One
Ansible-All-in-One


# Feature

- Install podman, docker
- Install docker


# How to use ansible-playbook in example

## 1. User SSH passpharase

```
rsa=/home/quangvv/.ssh/id_rsa
eval `ssh-agent`
ssh-add $rsa

ansible-playbook -i inventory.d/LAB.hosts -u quangvv --key-file $rsa --ask-become-pass playbook.install.docker.yaml
```


## 2. User SSH password

```
ansible-playbook -i inventory.d/LAB.hosts -u quangvv -K -k playbook.install.docker.yaml
```