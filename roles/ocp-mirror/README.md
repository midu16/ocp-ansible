Role Name
=========

This role scope its to deploy a local environment Offline Registry and mirror the newly release

Requirements
------------

You might already have this collection installed if you are using the ansible package. It is not included in ansible-core. To check whether `podman_container` it is installed, run ansible-galaxy collection list.

To install it, use: 

```bash
ansible-galaxy collection install containers.podman
ansible-galaxy collection install community.crypto
ansible-galaxy collection install community.general
```


Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

Apache License 2.0

Author Information
------------------

midu16
