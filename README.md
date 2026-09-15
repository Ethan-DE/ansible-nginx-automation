# NGINX with Ansible

A small Ansible playbook for configuring NGINX on Ubuntu. The local inventory makes it easy to test on a disposable VM, while the playbook itself is written the same way I would use it against a remote host group.

## What it does

- installs NGINX and UFW
- deploys a templated index page
- opens port 80
- enables and starts NGINX
- reloads NGINX only when the page changes

## Run

Install the required collection first:

```bash
ansible-galaxy collection install -r requirements.yml
```

Then run the playbook:

```bash
ansible-playbook -i inventory.ini site.yml
```

The checked-in inventory uses `localhost` with a local connection for testing. For a remote host, replace it with the target address and normal SSH inventory variables.

A second run should report no changes unless the package state or template has changed.
