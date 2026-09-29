Changelog
=========

[1.1.0] - 2026-08-06
--------------------

### New Features

- feat: Write roles fingerprints to /var/log/sysroles.jsonl [citest_skip] (#24)

### Other Changes

- ci: Bump actions/checkout from 6 to 7 (#17)
- ci: Use our own pr_title_lint.py instead of NPM commitlint [citest_skip] (#18)
- ci: bump tox-lsr version to 3.20.0 to fix tox 4.58 api breakage [citest_skip] (#19)
- ci: Add support for Fedora 44 and drop Fedora 42 - use ansible-core 2.21 [citest_skip] (#21)
- ci: Bump actions/setup-python from 6 to 7 (#22)
- ci: ensure dependabot updates do not invoke ci tests [citest_skip] (#23)

[1.0.2] - 2026-06-24
--------------------

### Other Changes

- refactor: use ansible.posix 2.1.X for EL7 compatibility [citest_skip] (#10)
- ci: Add config file for CodeRabbit with custom rules (#11)
- ci: Skip reviews for PRs with [citest_skip] in the title (#12)
- test: use ausearch --input-logs when running on localhost (#13)
- chore: add ostree packages-runtime.txt [citest_skip] (#14)
- test: use openat instead of open - supported on all arches - skip b32 on ppc64le (#15)

[1.0.1] - 2026-05-08
--------------------

### Other Changes

- refactor: use min_ansible_version 2.9 to be consistent with other roles [citest_skip] (#8)

[1.0.0] - 2026-05-07
--------------------

### New Features

- feat: auditd - new role - initial commit (#1)
- feat: add role fingerprints to syslog (#6)

### Other Changes

- ci: add ci workflows and config files (#2)
- ci: Bump actions/github-script from 8 to 9 (#3)

