# Ansible Role: awx

![MIT](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/racqspace/ansible-role-awx/Main?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/racqspace/ansible-role-awx?style=flat-square)
![GitHub Release Date](https://img.shields.io/github/release-date/racqspace/ansible-role-awx?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2022?style=flat-square)

Installing AWX through the AWX operator to provide a more Kubernetes-native installation method for AWX via an AWX Custom Resource Definition (CRD).

## Role Variables

Variable Name | Default Value | Description
------------ | ------------- | -------------
awx_cache_valid_time | 3600 | Cache update time for apt module.
awx_operator_version | 0.13.0 | Operator version used to deploy awx.
awx_namespace | awx | Target namespace for awx operator and instance.
awx_hostname |  | Hostname to expose awx via ingress.
awx_web_resource_requirements |  | Resource Requirements.

## Role Usage Examples

Example for installing awx with enabled ingress available at awx.example.com.

```yaml
- hosts: all
  roles:
  - role: racqspace.awx
    vars:
      awx_hostname: awx.example.com
```

## License

MIT

## Author Information

This role was created in 2021 by [Clemens Kaserer](https://www.ckaserer.dev/).

Contributions by:

- [@ckaserer](https://github.com/ckaserer)
