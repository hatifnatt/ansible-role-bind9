# bind9

Ansible role to setup ISC Bind9.

What this role can do:

* manage system service - enable / disable / start
* create main configuration files
* manage ddns keys and ddns key files
* create forward zones
* create reverse zones
* create rpz zones
* update zone records via DDNS
* reference zones in named.conf.local configuration

## Requirements

None

## Role Variables

Check out [defaults/main.yml](defaults/main.yml) and [vars_example.yml](vars_example.yml) for reference and examples.

## Dependencies

None

## Example Playbook

```yaml
---
- name: Setup bind9
  hosts: dns_servers
  roles:
    - role: hatifnatt.bind9
      become: true
```

## License

MIT

## Credits

Somewhat inspired by [systemli ansible-role-bind9](https://github.com/systemli/ansible-role-bind9/tree/main) role.

## TODO

* reload individual zones with rndc after update
* make sure to restart only when necessary
