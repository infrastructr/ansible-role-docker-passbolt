[![Build Status](https://travis-ci.org/infrastructr/ansible-role-docker-passbolt.svg?branch=master)](https://travis-ci.org/infrastructr/ansible-role-docker-passbolt)
[![Ansible Galaxy](https://img.shields.io/badge/role-infrastructr.docker_passbolt-blue.svg)](https://galaxy.ansible.com/infrastructr/docker_passbolt/)
[![Ansible Galaxy Quality Score](https://img.shields.io/ansible/quality/50434)](https://galaxy.ansible.com/infrastructr/docker_passbolt/)
[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/infrastructr/ansible-role-docker-passbolt)](https://galaxy.ansible.com/infrastructr/docker_passbolt)
[![Ansible Galaxy Downloads](https://img.shields.io/ansible/role/d/50434.svg?color=blue)](https://galaxy.ansible.com/infrastructr/docker_passbolt/)

# Ansible Role: Docker Passbolt

An Ansible Role that manages setup and configuration of [Passbolt](https://passbolt.com/) using [Docker](https://www.docker.com/).

## Role Variables

Available variables along with default values listed within [defaults/main.yml](defaults/main.yml).

## Dependencies

None.

## Example Playbook

    - name: Install role dependencies
      hosts: all
      vars:
        pip_package: python3-pip
        pip_install_packages:
          - name: docker
          - name: docker-compose
        docker_install_compose: true
      roles:
        - geerlingguy.pip
        - geerlingguy.docker

    - name: Install and configure Passbolt
      hosts: all
      roles:
        - infrastructr.docker_passbolt

## Development

Use [docker-molecule](https://github.com/infrastructr/docker-molecule) following the instructions to run [Molecule](https://molecule.readthedocs.io/en/stable/)
or install [Molecule](https://molecule.readthedocs.io/en/stable/) locally (not recommended, version conflicts might appear).

Provide Hetzner Cloud token:

    export HCLOUD_TOKEN=123abc456efg

Use following to run tests:

    molecule test --all

## Maintainers

- [build-failure](https://github.com/build-failure)

## License

See the [LICENSE.md](LICENSE.md) file for details.

## Author Information

This role was created in 2020 by [infrastructr](https://github.com/infrastructr) team.
