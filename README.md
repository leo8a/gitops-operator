# Ansible Role: GitOps operator

[![CI](https://github.com/leo8a/gitops-operator/actions/workflows/ci.yml/badge.svg)](https://github.com/leo8a/gitops-operator/actions/workflows/ci.yml)

Installs the [GitOps](https://github.com/redhat-developer/gitops-operator.git) operator on OpenShift clusters.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    gitops:
      enable_telco_ztp: no

## Dependencies

This role requires the `kubernetes.core` collection, and have been tested on an OpenShift cluster version 4.10.

## Example Playbook

    - hosts: localhost
      gather_facts: false
      roles:
        - leo8a.gitops_operator

To patch GitOps operator for Telco ZTP, the `enable_telco_ztp` var can be adjusted as follows:

    - hosts: localhost
      gather_facts: false
      roles:
        - leo8a.gitops_operator
      vars:
        - gitops:
            enable_telco_ztp: yes

## License

This role is released under the Apache 2.0 license. See the [LICENSE](LICENSE).

## Author Information

This role was created in 2022 by [Leo Ochoa](https://github.com/leo8a/).

## Contributors

This is the current list of folks in the `gitops_operator` hall of ~~fame~~ contributors 🏆!

<a href="https://github.com/leo8a/gitops-operator/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=leo8a/gitops-operator"  alt=""/>
</a>

> Made with [contributors-img](https://contrib.rocks).
