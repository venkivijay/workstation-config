# venkivijay/infra

Ansible playbook to install and configure personal workstation and servers(wip). Intended to use with ansible-pull.

## Installation

Temporary workaround until everything is in place. Enter password for sudo when prompted.

```bash
ansible-pull -U https://github.com/venkivijay/infra.git -kK;
```

To run the playbook against a new linode node:

```bash
ansible-playbook local.yml --private-key=~/.ssh/id_rsa -l server.venkivijay.com -u root
```
