CNI plugins
===========

An Ansible role to install and configure CNI (Container Network Interface) [plugins](https://github.com/containernetworking/plugins).

Requirements
------------

- Supported version of Ansible: 2.12 and higher. Systems with Python versions below than 3.7 are not compatible with ansible-core 2.17 (see [ansible/ansible#83357](https://github.com/ansible/ansible/issues/83357#issuecomment-2150254754)).
- Supported platforms:
  - Debian
    - 10
    - 11
    - 12
  - Fedora
    - 39
    - 40
  - RHEL
    - 7
    - 8
    - 9
  - Ubuntu
    - 18.04
    - 20.04
    - 22.04

Role Variables
--------------

All variables that can be overridden are stored in the [defaults/main.yml](https://github.com/antmelekhin/ansible-role-cni-plugins/blob/main/defaults/main.yml) file.
Please refer to the [meta/argument_specs.yml](https://github.com/antmelekhin/ansible-role-cni-plugins/blob/main/meta/argument_specs.yml) file for a description of the available variables.
Similarly, descriptions and defaults for preset variables can be found in the [vars/main.yml](https://github.com/antmelekhin/ansible-role-cni-plugins/blob/main/vars/main.yml) file.

Dependencies
------------

None.

Example Playbook
----------------

Install CNI plugins:

```yaml
---
- name: 'Install CNI plugins'
  hosts: all

  roles:
    - role: antmelekhin.cni_plugins
```

Install CNI plugins and configure bridge interface:

```yaml
---
- name: 'Install CNI plugins'
  hosts: all

  roles:
    - role: antmelekhin.cni_plugins
      cni_plugins_config_files:
        - filename: '10-bridge.conf'
          content:
            cniVersion: '0.3.1'
            name: 'mynet'
            type: 'bridge'
            bridge: 'mynet0'
            isDefaultGateway: true
            forceAddress: false
            ipMasq: true
            hairpinMode: true
            ipam:
              type: 'host-local'
              subnet: '10.10.0.0/16'
```

License
-------

MIT

Author Information
------------------

Melekhin Anton.
