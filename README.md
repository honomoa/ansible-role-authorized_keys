# Ansible Role: authorized_keys

Manage ssh authorized keys.

[https://www.ssh.com/ssh/authorized_keys/](https://www.ssh.com/ssh/authorized_keys/)

# Role Variables

```
add_keys: []
```

Public keys want to add.

```
remove_keys: []
```

Public keys want to remove.

# Example Playbook

```
- hosts: server
  vars:
    add_keys:
      - { user: ubuntu, key: ./files/server_new.pub }
    remove_keys:
      - { user: ubuntu, key: ./files/server.pub }
  roles:
    - { role: honomoa.authorized_keys }
```

# License
CC BY-SA 3.0
