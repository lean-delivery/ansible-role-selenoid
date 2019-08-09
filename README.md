## Selenoid in docker

[![License](https://img.shields.io/badge/license-Apache-green.svg?style=flat)](https://raw.githubusercontent.com/lean-delivery/ansible-role-selenoid/master/LICENSE)
[![Build Status](https://travis-ci.org/lean-delivery/ansible-role-selenoid.svg?branch=master)](https://travis-ci.org/lean-delivery/ansible-role-selenoid)
[![Build Status](https://gitlab.com/lean-delivery/ansible-role-selenoid/badges/master/pipeline.svg)](https://gitlab.com/lean-delivery/ansible-role-selenoid/pipelines)
[![Galaxy](https://img.shields.io/badge/galaxy-lean__delivery.selenoid-blue.svg)](https://galaxy.ansible.com/lean_delivery/selenoid)
![Ansible](https://img.shields.io/ansible/role/d/42610.svg)
![Ansible](https://img.shields.io/badge/dynamic/json.svg?label=min_ansible_version&url=https%3A%2F%2Fgalaxy.ansible.com%2Fapi%2Fv1%2Froles%2F42610%2F&query=$.min_ansible_version)

Set up [selenoid](https://github.com/lean-delivery/ansible-role-selenoid) in docker

#### Requirements

* `python`
* `docker`

#### Variables

* `selenoid_cm_version`: [Default: `1.3.1`] Install configuration manager version
* `selenoid_version`: [Default: `1.4.0`] Install selenoid version
* `selenoid_docker_api_version`: [Default: `1.24`] Docker api version (for Selenoid)

#### Example

```yaml
---
- hosts: all
  roles:
  - selenoid
```

## Dependencies

* [grid-router](https://github.com/iqoption/gridrouter-ansible)
 - ansible role lean_delivery.docker  [![Galaxy](https://img.shields.io/badge/galaxy-lean__delivery.docker-blue.svg)](https://galaxy.ansible.com/lean_delivery/docker)

grid-router may help you generate browser.xml (using sctl and ./files/input.json in grid-router repo).

## Contributing
1. Fork it;
2. Create your feature branch: `git checkout -b my-new-feature`;
3. Commit your changes: `git commit -am 'Add some feature'`;
4. Push to the branch: `git push origin my-new-feature`;
5. Submit a pull request.

## License
See LICENSE

## Author Information
authors:

  - Lean Delivery Team team@lean-delivery.com


#### Example playbook for packer
---
- hosts: all
  gather_facts: no
  roles:
    - role: ansible-role-selenoid
---