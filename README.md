Caddy Ansible Role
==================

This role will install caddy web server with php 7.4 support. It's managed as a systemd service and a simple configuration file is provided for caddy to work. Once it has finished, you can test it by pointing your browser to:

http://[hostname]:[port]/phpinfo.php


Requirements
------------
None

Role Variables
--------------
Tne default variables included in this role are:
```yaml
caddy_user:         caddy           # system account
caddy_group:        caddy           # System account primary group
root_folder:        /var/www/html   # Location of web server root folder
caddy_log_folder:   /var/log/caddy  # Log file folder
caddy_version:      2.2.0           # Caddy software version
caddy_home:         /usr/bin        # Location for caddy binary
php_version:        7.4             # PHP version
```
All of them are already defined in /defaults/main.yml, feel free to overwrite them

Dependencies
------------
None

Example Playbook
----------------
Register the role in requirements.yml:
```yaml
    - src: capitanh.caddy_ansible_role
      name: caddy
```
Include it in your playbooks:
```yaml
    - hosts: servers
      roles:
      - caddy
```
License
-------
BSD

