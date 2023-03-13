ssh_auth
=========

Manage SSH authorized keys for users.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    ssh_users
    ssh_blocked_users

Dependencies
------------

None.

Example Playbook
----------------

    - name: Assure authorized keys for users
      hosts: managed
      roles:
        - role: ssh_auth
          vars:
            ssh_users:
              - user: root
                key: ssh_keys/root.pub
              - user: sudo_user1
                key: ssh_allow/sudo_user1.pub

            ssh_blocked_users:
              - user: root
                key: ssh_deny/ex_user.pub

License
-------

All rights reserved.

Author Information
------------------

This role was created in 2022 by Anthony Pagan.
