# Fapolicyd

Fapolicyd System Role

## Requirements

This role is only supported on RHEL8.1+/CentOS8.1+ and Fedora distributions. Consider reading fapolicyd documentation before setting it up.

### Collection requirements

If you want to manage `rpm-ostree` systems with this role, you will need to
install additional collections.  Please run the following command line to
install the collection.

```bash
ansible-galaxy collection install -vv -r meta/collection-requirements.yml
```

## Role Variables

### fapolicyd_setup_enable_service

Default `true` - if set to `false` the variable makes the service stopped
and disabled.

### fapolicyd_setup_trust

Default `rpmdb,file` - there can be list of sources for trust option `file`, `rpmdb` or `deb`(if compiled with debian support).
The option specifies which sources of trust a loaded and in which order.

### fapolicyd_setup_integrity

Default `none` - there are four supported types of integrity. No integrity `none`, defined by `size` of the file, defined by hash of the file `sha256` and defined by hashes of files but generated from `ima` kernel subsystem. Note that IMA needs to be set up separately and this system role does not cover it.

### fapolicyd_setup_permissive

Default `false` - if set to `true` deploys the daemon in permissive mode.

### fapolicyd_add_trusted_paths

Default empty - list of files and directories that will be marked as trusted.
Note that you cannot specify an empty directory.

### fapolicyd_add_trusted_file

Deprecated alias for `fapolicyd_add_trusted_paths`.  If `fapolicyd_add_trusted_paths`
is not set, the role uses `fapolicyd_add_trusted_file` instead.  Prefer
`fapolicyd_add_trusted_paths` in new playbooks.

## Example Playbook

```yaml
---
- name: Example fapolicyd role invocation
  hosts: all
  vars:
    fapolicyd_setup_enable_service: true
    fapolicyd_setup_integrity: sha256
    fapolicyd_setup_trust: rpmdb,file
    fapolicyd_add_trusted_paths:
      - /etc/passwd
      - /etc/fapolicyd/fapolicyd.conf
      - /etc/krb5.conf
      - /opt/myapplication/bin  # a directory - must not be empty
  roles:
    - fapolicyd
```

## rpm-ostree

See README-ostree.md

## License

MIT

## Author Information

Radovan Sroka @rsroka

Marko Myllynen @myllynen

[![ansible-lint.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/ansible-lint.yml) [![ansible-test.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/ansible-test.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/ansible-test.yml) [![codespell.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/codespell.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/codespell.yml) [![markdownlint.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/markdownlint.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/markdownlint.yml) [![qemu-kvm-integration-tests.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/qemu-kvm-integration-tests.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/qemu-kvm-integration-tests.yml) [![tft.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/tft.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/tft.yml) [![tft_citest_bad.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/tft_citest_bad.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/tft_citest_bad.yml) [![woke.yml](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/woke.yml/badge.svg)](https://github.com/fedora.linux_system_roles.fapolicyd/actions/workflows/woke.yml)
