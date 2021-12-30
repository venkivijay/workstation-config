# venkivijay/infra

Ansible role to install and configure personal workstation and servers(wip). Intended to use with ansible-pull.

## Installation

Temporary workaround until everything is in place. Enter password for sudo when prompted.

```bash
echo -e "[workstation]\r\nlocalhost" > /tmp/inventory;
ansible-pull -U https://github.com/venkivijay/infra.git -i /tmp/inventory -kK;
```
