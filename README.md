# Introduction to Ansible
Ansible provides open-source automation that reduces complexity and runs everywhere. Using Ansible lets you automate virtually any task. Here are some common use cases for Ansible:

Eliminate repetition and simplify workflows

Manage and maintain system configuration

Continuously deploy complex software

Perform zero-downtime rolling updates

Ansible uses simple, human-readable scripts called playbooks to automate your tasks. You declare the desired state of a local or remote system in your playbook. Ansible ensures that the system remains in that state.

## As automation technology, Ansible is designed around the following principles:

## Agent-less architecture
Low maintenance overhead by avoiding the installation of additional software across IT infrastructure.

## Simplicity
Automation playbooks use straightforward YAML syntax for code that reads like documentation. Ansible is also decentralized, using SSH existing OS credentials to access to remote machines.

## Scalability and flexibility
Easily and quickly scale the systems you automate through a modular design that supports a large range of operating systems, cloud platforms, and network devices.

## Idempotence and predictability
When the system is in the state your playbook describes Ansible does not change anything, even if the playbook runs multiple times.

![image](https://github.com/bhaveshcse/ansible-tutorial/assets/22559264/ab0724b1-fdfe-47cd-ad77-0da1b98df030)

# Ansible installation on Ubuntu

```bash
sudo apt-get update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt-get -y install ansible
```
## Show Ansible configuration

```bash
sudo cat /etc/ansible/hosts
```
## Update host file
```bash
[server]
server1 ansible_host=PUBLIC IP ADDRESS
server2 ansible_host=PUBLIC IP ADDRESS
server3 ansible_host=PUBLIC IP ADDRESS

[server:vars]
ansible_python_interpreter=/usr/bin/python3
ansible_user=ubuntu
ansible_ssh_private_key_file=/home/ubuntu/keys/ansible-tutorial/ansible-server-key.pem
```

## ping to all server
"-m": module
"-a": ad-hoc command
```bash
$ sudo ansible all -m ping
```
## Display uptime of servers
```bash
$ sudo ansible all -a "uptime"
```
