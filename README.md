# packages

Ansible role to handle packages (installation / removal).

## Requirements

None.

## Role Variables

- packages_del
  predefined in `defaults/main.yml`. Use it to specify packages to delete for all servers.

- packages_add
  predefined in `defaults/main.yml`. Use it to specify common packages for all servers.

- packages_extra
  predefined in `host_vars/\*` or `group_vars/\*` to add specific extra packages.

## Dependencies

None.

## Install this role as submodule in a git repository

`git submodule add https://git.sekoya.org/mb/packages.git roles/packages`

## Example Playbooks

    - hosts: servers
      roles:
         - packages

or

    - hosts: servers
      roles:
         - { role: packages, packages_extra: [ 'uuid', 'xinetd' ] }

## License

GPLv3

## Author Information

http://www.sekoya.org
