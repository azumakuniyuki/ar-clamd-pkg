Ansible Role: clamd(pkg)
================================================================================
Install and configure clamd

- Install clamd using yum on CentOS 7
- Deploy the following files:
    - /etc/clamd.d/scan.conf
    - /etc/cron.d/clamav-update
    - /etc/freshclam.conf
    - /etc/logrotate.d/clamav-update
    - /etc/sysconfig/freshclam

Requirements
--------------------------------------------------------------------------------
None

Role Variables
--------------------------------------------------------------------------------
The following variables are defined in defaults/main.yml file.

```yaml
clamd:
  enabled: true
  started: true
  serverroot: "/var/lib/clamav"
  loggingdir: "/var/log/clam"
  syslog:
    facility: "LOCAL6"
```

Dependencies
--------------------------------------------------------------------------------
None

Example Playbook
--------------------------------------------------------------------------------
```yaml
- hosts: servers
  roles:
     - { role: azumakuniyuki.ar-clamd-pkg }
```

License
--------------------------------------------------------------------------------
BSD

Author Information
--------------------------------------------------------------------------------
[azumakuniyuki](https://nyaan.jp)

