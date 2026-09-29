Changelog
=========

[1.2.0] - 2026-09-17
--------------------

### New Features

- feat: Argument spec implementation for trustee server role (#40)

### Other Changes

- ci: use commit hash for github action, add persist-credentials false [citest_skip] (#36)
- ci: refactor build_docs so that pandoc runs in isolated read-only job [citest_skip] (#37)
- ci: use exact match for systemroller instead of contains [citest_skip] (#38)
- ci(build_docs): fix pandoc container syntax [citest_skip] (#39)
- ci: [citest_skip] Bump codespell-project/actions-codespell from 2.1 to 2.2 (#41)
- ci: [citest_skip] Bump actions/download-artifact from 7.0.0 to 8.0.1 (#42)
- ci: [citest_skip] Bump myrotvorets/set-commit-status-action from 2774e1f040c82ed70a76b4b5cd53bb11ffaedd0a to c0f880c99d91381c6fdb97726f03feb8004409b4 (#43)
- refactor: Relax collection constraints, gate vendored modules by python version, update ci versions [citest_skip] (#44)
- ci: do not run ci tests by default, require citest comment or label [citest_skip] (#45)
- ci: replace weekly_ci with periodic_ci, stagger schedules [citest_skip] (#46)
- ci: update status when action triggered by issue comment (#47)

[1.1.0] - 2026-08-06
--------------------

### New Features

- feat: Write roles fingerprints to /var/log/sysroles.jsonl [citest_skip] (#34)

### Other Changes

- ci: Bump actions/checkout from 6 to 7 (#27)
- ci: Use our own pr_title_lint.py instead of NPM commitlint [citest_skip] (#28)
- ci: bump tox-lsr version to 3.20.0 to fix tox 4.58 api breakage [citest_skip] (#29)
- ci: Add support for Fedora 44 and drop Fedora 42 - use ansible-core 2.21 [citest_skip] (#31)
- ci: Bump actions/setup-python from 6 to 7 (#32)
- ci: ensure dependabot updates do not invoke ci tests [citest_skip] (#33)

[1.0.2] - 2026-06-24
--------------------

### Bug Fixes

- fix: do not use cert '-subj' with hostname to generate cert, use subjectAltName (#24)

### Other Changes

- refactor: use ansible.posix 2.1.X for EL7 compatibility [citest_skip] (#21)
- ci: Add config file for CodeRabbit with custom rules (#22)
- ci: Skip reviews for PRs with [citest_skip] in the title (#23)
- test: ensure podman volumes are removed (#25)

[1.0.1] - 2026-05-12
--------------------

### Bug Fixes

- fix: Use verbosity level 3 for no_log (#18)

### Other Changes

- refactor: use firewall role instead of module (#19)

[1.0.0] - 2026-05-07
--------------------

### New Features

- feat: Add Trustee quadlet and secret registration server (#2)
- feat: add role fingerprints to syslog (#13)
- feat: new variable `trustee_server_secure_logging` defaulting to `true` (#15)

### Other Changes

- ci: tox-lsr 3.17.0 - container test improvements, use ansible 2.20 for fedora 43 [citest_skip] (#1)
- ci: tox-lsr 3.17.1 - previous update broke container tests, this fixes them [citest_skip] (#3)
- test: ensure role gathers the facts it uses by having test clear_facts before include_role (#11)
- refactor: copy external files to role, copy containers to quay.io linux-system-roles (#12)
- ci: Bump actions/github-script from 8 to 9 (#14)
- docs: document role parameters [citest_skip] (#16)

