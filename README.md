# Ansible Role: OUI Lookup

This role fetches company information for MAC addresses using an API and writes them to a file.

## Requirements

- `jq` must be installed on the system where the role is executed.

## Role Variables

- `input_file`: Path to the file containing MAC addresses. Default is 'mac_addresses.yml'.
- `output_file`: Path where the output will be saved. Default is 'oui-lookup.txt'. Both of these files default in the role's root directory.

## Dependencies

None.

## Example Playbook

```yaml
---
- name: Execute OUI Lookup Role
  hosts: localhost
  gather_facts: no
  roles:
     - oui_lookup
