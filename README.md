# Ansible Role: Server

Base Ansible role for a Nexcess "server".  This role should be common across all Ansible playbooks and provides basics including:

- Server update (toggable)
- Default "good" pathing (so things like SCL PHPs are in the default path)
- Common limit increases (file handles, memory, etc)
- Installs typical utilities we need (telnet, tcpdump, nc, etc)
- Installs our base repo + GPG keys and EPEL
- Sets up base NTP
- Provides a simple iptables based firewall interface with good default rules
- **IMPORTANT** - handles setting up of /etc/hosts for an entire project inventory.  This includes both internal and external IPs.  It follows the inventory standard of backnet_addr=xx.xx.xx.xx and frontnet_addr=yy.yy.yy.yy and will automatically add the "-int" to the end of your inventory short name.

## Role Variables

Lots, but just about everything is overridable.  See [defaults/main.yml](https://github.com/nexcess/ansible-role-server/blob/master/defaults/main.yml)


## Requirements
- Ansible-playbook 2.3 or greater.

## Dependencies

- nexcess.firewall
- nexcess.repo-epel
- nexcess.repo-remi
- nexcess.ntp

## License

MIT
