[![CI](https://github.com/ngine-io/ansible-role-blocky-dns/actions/workflows/ci.yml/badge.svg)](https://github.com/ngine-io/ansible-role-blocky-dns/actions/workflows/ci.yml)

# Ansible Role: Blocky DNS

Installs and manages [Blocky DNS](https://0xerr0r.github.io/blocky).

## Requirements

None.

## Installation

Via `requirements.yml`:

```yaml
---
# file: requirements.yml
roles:
  - name: ngine_io.blocky_dns
    version: v0.1.0
```

To install:

```
ansible-galaxy install -r requirements.yml
```

## Dependencies

None.

## Example Playbooks

```yaml
- hosts: dns
  # Ensures that only one DNS host is changed at a time.
  serial: 1
  roles:
    - role: ngine_io.blocky_dns
```
Enable inventory hosts to custom DNS:

```yaml
- hosts: dns
  vars:
    blocky__hosts_dns_enabled: true
    # Optionally append a domain but note the '.' prefix
    blocky__hosts_dns_domain: ".local.example.com"
  roles:
    - role: ngine_io.blocky_dns
```

## License

MIT / Apache2

## Author Information

This role was created in 2024 by [René Moser](https://renemoser.net).
