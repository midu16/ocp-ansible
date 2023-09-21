Ansible Role: Display Host OS Distribution
=========

This Ansible role is designed to perform the following tasks:

- Display the distribution of the host operating system.
- Install required packages and pip packages based on the host OS distribution.
- Install roles from Ansible Galaxy.
- Configure an offline registry, if needed.
- Template the `imageset-config.yaml` file.
- Start the mirroring process for offline registry and prepare the internal release.


Requirements
------------

This Ansible role requires the following:

- Ansible should be installed on the system where this role is executed.
- This role is intended to work on RedHat and Fedora distributions.



Role Variables
--------------

The following role variables are available for customization:

- `registry_data_dir`: The directory for registry data.
- `registry_auth_dir`: The directory for registry authentication.
- `registry_certs_dir`: The directory for registry SSL/TLS certificates.
- `imageset_directory`: The directory for storing imageset files.
- `system_user_username`: The desired owner for various directories.
- `system_user_group`: The desired group for various directories.
- `cert_c`, `cert_s`, `cert_l`, `cert_o`, `cert_ou`, `cert_cn`: Certificate details for self-signed certificates.
- `host_fqdn`: Fully qualified domain name for the host.
- `registry_username`: Username for the registry authentication.
- `registry_password`: Password for the registry authentication.
- `registry_fqdn`: Fully qualified domain name for the registry.
- `registry_port`: Port for the registry.


Dependencies
------------

This Ansible role has dependencies on the following:

- containers.podman
- community.crypto
- community.general
- podman
- httpd-tools
- python3.11
- python3-pip
- libselinux-python3
- openshift
- pyyaml
- kubernetes
- passlib
- pyOpenSSL

For these dependencies the playboook will make sure that are installed in your Ansible environment.


Example Playbook
----------------

Here's an example of how to use this Ansible role in a playbook:

```yaml
Copy code
- name: Disable chronyd on master nodes
  hosts: localhost
  gather_facts: false
  environment:
    KUBECONFIG: <path_to_kubeconfig>
  collections:
    - community.kubernetes
    - kubernetes.core
  roles:
    - role: ocp-mirror
```


License
-------

Apache License 2.0

Author Information
------------------

midu16
