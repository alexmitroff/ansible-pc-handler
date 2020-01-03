# Basic ansible setup for home computers administration

## Table of content

* Add `hosts.txt`

## Add hosts.txt

```
[group_name]
machine_name ansible_host=192.168.0.255
```

## Add group variables

`group_vars/group_name`

```
---
ansible_user: user_name
ansible_ssh_private_key_file: path_to_ssh_key
```

## Check that ansible can connect to your machines

```
ansible-playbook playbooks/check-connections.yml
```
