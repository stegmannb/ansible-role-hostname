# Ansible Template Role

[![License: MIT](https://img.shields.io/github/license/stegmannb/ansible-role-hostname)](https://github.com/stegmannb/ansible-role-hostname/blob/master/LICENSE)
[![Continuous Integration](https://github.com/stegmannb/ansible-role-hostname/actions/workflows/continuous-integration.yml/badge.svg)](https://github.com/stegmannb/ansible-role-hostname/actions/workflows/continuous-integration.yml)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

## Requirements

Ansible 2.6 or higher

## Role Variables

- `hostname_inject_hosts_file` - Set to true to inject lines into the `/etc/hosts` file. Defaults to `true`.
- `hostname_short` - Set to the short hostname for the host or `inventory`. If `inventory` this is set to `inventory_hostname_short`. Defaults to `inventory`.
- `hostname_fqdn` - Set to the FQDN hostname for the host or `inventory`. If `inventory` this is set to `inventory_hostname`. Defaults to `inventory`.
- `hostname_ip` - The IP address for the `/etc/hosts` file entry. Defaults to `127.0.1.1`.
- `hostname_aliases` - Optional list of aliases for the host to inject in the `/etc/hosts` file.

## Dependencies

None

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: server1
      roles:
         - role: stegmannb.hostname
           vars:
            hostname_fqdn: server1.example.domain.com

## License

MIT
