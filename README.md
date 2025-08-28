# Ansible NGINX Automation

Automated provisioning of an NGINX web server on Ubuntu using Ansible.

## Inventory

```ini
[web]
localhost ansible_connection=local

Playbook Structure
Installs NGINX

Enables and starts service

Replaces default index page

Opens HTTP port via UFW

Usage
ansible-playbook -i inventory.ini site.yml

Requirements

Ubuntu-based system

Ansible installed (sudo apt install ansible)

Root privileges

Status

Tested on fresh Ubuntu 22.04 VPS with static IPv4.

Author

Ethan E
Email: eradirideitie@gmail.com

Open to relocation and remote DevOps roles
