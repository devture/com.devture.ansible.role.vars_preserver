# `vars.yml`-preserver Ansible role

This is an Ansible role which preserves (backs up) the `vars.yml` file for a given host to the server.

## Usage

Example playbook:

```yaml
- hosts: servers
  roles:
    - when: devture_vars_preserver_enabled | bool
      role: galaxy/com.devture.ansible.role.vars_preserver
      # Uncomment to make it run on some tags only, not always
      # tags:
      #  - setup-all
```

Example configuration (see `defaults/main.yml` for more):

```yaml
devture_vars_preserver_dst: /path/on-server/to/vars.yml
devture_vars_preserver_uid: 1000
devture_vars_preserver_gid: 1000
```
