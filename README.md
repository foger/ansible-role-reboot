# Ansible role - Reboot

Ansible Role for rebooting servers

## Requirements

Tested:

- Debian 9, 10
- Ubuntu 16.04, 18.04
- CentOS 7.7
- Fedora 31
- FreeBSD 11

Ansible version >= 2.7

## Role Variables

### Defaults

`reboot_always` - Don't check if system needs to be restarted. Reboot always

`reboot_delay` - Wait <N> seconds before reboot

`reboot_check` - Check if host is up after <N> seconds

`reboot_message` - Show this message to users when reboot initiated

### Vars

`reboot_requirements` - Install `needs-restarting` utility for RedHat based distributions

`reboot_needs_restarting_command` - Command to check if OS needs restarting

## Dependencies

- No.

## Example Playbook

```yaml
- hosts: servers
  roles:
      - { role: reboot }
```

## License

MIT
