# Ansible Admin User Role

## Actions of the Role

* Create a Linux admin user and set the authorized_keys.

## Common Usage


```yaml
roles:
- { role: francomile.admin-user,
    admin_user_username: "admin",
    admin_user_ssh_pubkey: "{{ lookup('url', 'https://github.com/francomile.keys', split_lines=False) }}",
    tags: ["admin-user"]
  }
```

## Run the playbook

```shell
ansible-playbook -i inventory playbook.yaml --tags "admin-user"
```
