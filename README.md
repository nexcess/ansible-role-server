Role Name
=========

Base Ansible role for a Nexcess "server".  This role should be common across all Ansible playbooks and provides basics including:

- Server update (toggable)
- Default "good" pathing (so things like SCL PHPs are in the default path)
- Common limit increases (file handles, memory, etc)
- Installs typical utilities we need (telnet, tcpdump, nc, etc)
- Installs our base repo + GPG keys and EPEL
- Sets up base NTP
- Provides a simple iptables based firewall interface with good default rules
- **IMPORTANT** - handles setting up of /etc/hosts for an entire project inventory

Variables
---------

Lots, but just about everything is overridable.  See [defaults/main.yml](https://github.com/clwells/ansible-role-server/blob/master/defaults/main.yml)

Dependencies
------------

- mikegleasonjr.firewall
- geerlingguy.repo-epel
- geerlingguy.ntp

License
-------

MIT
