Sudo
====

This role helps to install and configure sudo.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:
'''
  sudo:
    - file: admins
      groups:
        - admins
      command: ALL=(ALL:ALL) ALL
      state: present
    - file: user
      users:
        - user
      command: ALL=(ALL:ALL) ALL
      state: present
'''

Variable 'state' is optional.


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: sudo, tags: sudo }

License
-------

BSD


