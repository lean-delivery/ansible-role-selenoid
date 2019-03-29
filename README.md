## Selenoid in docker

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
    - { role: ../ansible-role-selenoid, become: true }
---