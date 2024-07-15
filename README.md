CNI plugins
===========

An Ansible role to install and configure CNI (Container Network Interface) plugins.

Requirements
------------

- Supported version of Ansible: 2.12 and highter.
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

- `cni_plugins_version` The version of CNI plugins to install (default: `1.5.1`).
- `cni_plugins_archive_name` The CNI plugins archive name (default: `cni-plugins-linux-amd64-v1.5.1.tgz`).
- `cni_plugins_download_url` The CNI plugins archive download URL (default: `https://github.com/containernetworking/plugins/releases/download/v1.5.1`).
- `cni_plugins_download_path` Local path to download and extract the archive (default: `/tmp`).
- `cni_plugins_install_path` The CNI plugins installation directory (default: `/opt/cni/bin`).
- `cni_plugins_config_path` The CNI plugins directory, that contains configuration files (default: `/etc/cni/net.d`).
- `cni_plugins_config_files` This variable defines the configuration files for plugins, including options. See the example below and the official [documentation](https://github.com/containernetworking/cni/blob/main/SPEC.md).

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
