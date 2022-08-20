sssdad Role
=========

This role will install the sssd tool and pre-requisites for joining an active directory domain, then it will join the domain using the realm commands.

[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-neoloc.sssdad-blue.svg)](https://galaxy.ansible.com/neoloc/ansible-role-sssdad/)


Requirements
------------

None

Role Variables
--------------

Refer to default/main.yml file.

```yaml
sssdad_configure: true
sssdad_realm: somedomain.tld
sssdad_user: admin_user
sssdad_pass: admin_password
sssdad_conf_default_shell: /bin/bash
sssdad_conf_fallback_homedir: /home/%d/%u
sssdad_conf_ad_gpo_ignore_unreadable: true
```

It is recommended to use a vault password for the sssd_user and sssd_pass variables.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - neoloc.sssdad

License
-------

See license.md

Author Information
------------------

[![Github](https://img.shields.io/badge/Github-neoloc-blue.svg)](https://github.com/neoloc)
