teleport_update
=========

Role to upgrade teleport

Requirements
------------

For using molecule tests:

```text
molecule-podman==2.1.0
molecule==5.0.0
ansible==2.14.5
```

and python 3.9+

 For using role:

```text
ansible==2.14.5
```

Role Variables
--------------

```yaml
# This means that the teleport service needs to be restarted.
teleport_service_enabled: false
# Means that it is necessary to restart also the second teleport service.
second_service_enabled: false
# Name of the second service
second_service_name: app_teleport
```

Dependencies
------------

installed teleport on hosts

Example Playbook
----------------

```yaml
---
- hosts: all
  roles:
   - teleport_update
```

License
-------

BSD-3-Clause

Author Information
------------------

[IlyaPvd](https://github.com/IlyaPvd)