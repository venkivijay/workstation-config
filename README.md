# venkivijay/infra

Ansible playbook to configure my personal workstation and server.

## System info

- **Workstation**:
  - OS: Pop!_OS 21.10 x86_64
- **Server**:
  - OS: Ubuntu 20.04.3 LTS x86_64

## Installation

### Production

*To configure localhost:*

> Temporary workaround until everything is in place. Enter password for sudo when prompted.

```bash
ansible-pull -U https://github.com/venkivijay/infra.git -kK;
```

*To run the playbook against a new linode from workstation:*

> DNS should be available. Else replace with IP address.

```bash
ansible-playbook local.yml --private-key=~/.ssh/id_rsa -l server.venkivijay.com -u root;
```

### Development

```bash
ansible-pull -U https://github.com/venkivijay/infra.git -kK -C develop;
```

## Disclaimer ⚠️

Please don't directly use this asnible setup on your own machines, as it is something I developed for myself and may not translate to your use-case. It configures OpenSSH, so you might get yourself locked out of your system. This has been tested only on Debian based systems (more specifically, Pop!_OS 21.10 and Ubuntu 20.04 LTS). Not guaranteed to work on other systems. The main purpose of this repository is to simply provide an outside view of my setup, so:

1. If noticed, feedback can be obtained, and
2. Others can learn from what I've implemented.
