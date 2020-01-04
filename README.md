# Basic ansible setup for home computers administration

## Table of content

* [Add hosts.txt](#add-hoststxt)
* [Add group variables](#add-group-variables)
* [Check that ansible can connect to your machines](#check-that-ansible-can-connect-to-your-machines)

## Add hosts.txt
```
.
├── ansible.cfg
├── hosts.txt
└── README.md

```
Content:
```
[group_name]
machine_name ansible_host=192.168.0.255
```

## Add group variables

```
.
├── ansible.cfg
├── group_vars
│   └── group_name
├── hosts.txt
└── README.md
```
Content:
```
---
ansible_user: user_name
ansible_ssh_private_key_file: path_to_ssh_key
ansible_sudo_pass: password_if_user_will_use_sudo_cmd
```

## Check that ansible can connect to your machines

```
ansible-playbook playbooks/check-connections.yml -v
```

## Upgrade APT packages

```
ansible-playbook playbooks/upgrade-apt-pkgs.yml -v
```

