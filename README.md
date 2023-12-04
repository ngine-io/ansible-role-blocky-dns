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

## Example Playbook

```yaml
- hosts: dns
  roles:
    - role: ngine_io.blocky_dns
```

## License

MIT / Apache2

## Author Information

This role was created in 2024 by [René Moser](https://renemoser.net).
