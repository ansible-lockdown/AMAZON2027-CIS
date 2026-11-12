# AMAZON 2027 CIS

## Configure an AMAZON 2027 machine to be [CIS](https://www.cisecurity.org/cis-benchmarks/) compliant

### Beta 0.0.1, based on [CIS Amazon Linux 2023 Benchmark v2.0.0 - 27-10-2026](https://www.cisecurity.org/cis-benchmarks/)

**Beta: CIS has not yet published an Amazon Linux 2027 benchmark.** Until it does, this role follows the control numbering and content of the CIS Amazon Linux 2023 Benchmark v2.0.0, adapted for Amazon Linux 2027. Use it for testing only. The role will move to the official benchmark when CIS releases it.

---

## Public Repository

![Org Stars](https://img.shields.io/github/stars/ansible-lockdown?label=Org%20Stars&style=social)
![Stars](https://img.shields.io/github/stars/ansible-lockdown/AMAZON2027-CIS?label=Repo%20Stars&style=social)
![Forks](https://img.shields.io/github/forks/ansible-lockdown/AMAZON2027-CIS?style=social)
![Followers](https://img.shields.io/github/followers/ansible-lockdown?style=social)
[![X URL](https://img.shields.io/twitter/url/https/x.com/AnsibleLockdown.svg?style=social&label=Follow%20%40AnsibleLockdown)](https://x.com/AnsibleLockdown)
![Discord Badge](https://img.shields.io/discord/925818806838919229?logo=discord)

![License](https://img.shields.io/github/license/ansible-lockdown/AMAZON2027-CIS?label=License)

## Lint & Pre-Commit Tools

![YamlLint](https://img.shields.io/badge/yamllint-Present-brightgreen?style=flat&logo=yaml&logoColor=white)
![Ansible-Lint](https://img.shields.io/badge/ansible--lint-Present-brightgreen?style=flat&logo=ansible&logoColor=white)

## Community Release Information

![Release Branch](https://img.shields.io/badge/Release%20Branch-Main-brightgreen)
![Release Tag](https://img.shields.io/github/v/tag/ansible-lockdown/AMAZON2027-CIS?label=Release%20Tag&&color=success)
![Main Release Date](https://img.shields.io/github/release-date/ansible-lockdown/AMAZON2027-CIS?label=Release%20Date)
![Benchmark Version Main](https://img.shields.io/endpoint?url=https://ansible-lockdown.github.io/github_linux_IaC/badges/AMAZON2027-CIS/benchmark-version-main.json)
![Benchmark Version Devel](https://img.shields.io/endpoint?url=https://ansible-lockdown.github.io/github_linux_IaC/badges/AMAZON2027-CIS/benchmark-version-devel.json)

[![Main Pipeline Status](https://github.com/ansible-lockdown/AMAZON2027-CIS/actions/workflows/main_pipeline_validation.yml/badge.svg?)](https://github.com/ansible-lockdown/AMAZON2027-CIS/actions/workflows/main_pipeline_validation.yml)

[![Devel Pipeline Status](https://github.com/ansible-lockdown/AMAZON2027-CIS/actions/workflows/devel_pipeline_validation.yml/badge.svg?)](https://github.com/ansible-lockdown/AMAZON2027-CIS/actions/workflows/devel_pipeline_validation.yml)


![Devel Commits](https://img.shields.io/github/commit-activity/m/ansible-lockdown/AMAZON2027-CIS/devel?color=dark%20green&label=Devel%20Branch%20Commits)
![Open Issues](https://img.shields.io/github/issues-raw/ansible-lockdown/AMAZON2027-CIS?label=Open%20Issues)
![Closed Issues](https://img.shields.io/github/issues-closed-raw/ansible-lockdown/AMAZON2027-CIS?label=Closed%20Issues&&color=success)
![Pull Requests](https://img.shields.io/github/issues-pr/ansible-lockdown/AMAZON2027-CIS?label=Pull%20Requests)

---

## Subscriber Release Information

![Private Release Branch](https://img.shields.io/endpoint?url=https://ansible-lockdown.github.io/github_linux_IaC/badges/Private-AMAZON2027-CIS/release-branch.json)
![Private Benchmark Version](https://img.shields.io/endpoint?url=https://ansible-lockdown.github.io/github_linux_IaC/badges/Private-AMAZON2027-CIS/benchmark-version.json)

[![Private Remediate Pipeline](https://img.shields.io/endpoint?url=https://ansible-lockdown.github.io/github_linux_IaC/badges/Private-AMAZON2027-CIS/remediate.json)](https://github.com/ansible-lockdown/Private-AMAZON2027-CIS/actions/workflows/main_pipeline_validation.yml)

![Private Pull Requests](https://img.shields.io/endpoint?url=https://ansible-lockdown.github.io/github_linux_IaC/badges/Private-AMAZON2027-CIS/prs.json)
![Private Closed Issues](https://img.shields.io/endpoint?url=https://ansible-lockdown.github.io/github_linux_IaC/badges/Private-AMAZON2027-CIS/issues-closed.json)

---

## Looking for support?

[Lockdown Enterprise](https://www.lockdownenterprise.com#GH_AL_AMAZON2027_cis)

[Ansible support](https://www.mindpointgroup.com/cybersecurity-products/ansible-counselor#GH_AL_AMAZON2027_cis)

### Community

On our [Discord Server](https://www.lockdownenterprise.com/discord) to ask questions, discuss features, or just chat with other Ansible-Lockdown users

### Contributing

Bug reports and feature requests are welcome from everyone, please raise an issue.

Pull requests are accepted from approved contributors only. To be onboarded, join the [Discord Server](https://www.lockdownenterprise.com/discord) and request contributor access. See [CONTRIBUTING.md](CONTRIBUTING.md) for the full process.

---

## Caution(s)

This role **will make changes to the system** which may have unintended consequences. This is not an auditing tool but rather a remediation tool to be used after an audit has been conducted.

- Testing is the most important thing you can do.

- Check Mode is not guaranteed! The role will complete in check mode without errors, but it is not supported and should be used with caution.

- This role was developed against a clean install of the Operating System. If you are implementing to an existing system please review this role for any site specific changes that are needed.

- To use release version please point to main branch and relevant release for the cis benchmark you wish to work with.

- Did we mention testing??

---

## Coming From A Previous Release

CIS release always contains changes, it is highly recommended to review the new references and available variables. This have changed significantly since ansible-lockdown initial release.
This is now compatible with python3 if it is found to be the default interpreter. This does come with pre-requisites which it configures the system accordingly.

Further details can be seen in the [Changelog](./Changelog.md)

---

## Matching a security Level for CIS

It is possible to only run level 1 or level 2 controls for CIS.
This is managed using tags:

- level1-server
- level1-workstation
- level2-server
- level2-workstation

The control found in defaults main also need to reflect this as this control the testing that takes place if you are using the audit component.

---

## Requirements

**General:**

- Basic knowledge of Ansible, below are some links to the Ansible documentation to help get started if you are unfamiliar with Ansible

  - [Main Ansible documentation page](https://docs.ansible.com)
  - [Ansible Getting Started](https://docs.ansible.com/ansible/latest/user_guide/intro_getting_started.html)
  - [Tower User Guide](https://docs.ansible.com/ansible-tower/latest/html/userguide/index.html)
  - [Ansible Community Info](https://docs.ansible.com/ansible/latest/community/index.html)
- Functioning Ansible and/or Tower Installed, configured, and running. This includes all of the base Ansible/Tower configurations, needed packages installed, and infrastructure setup.
- Please read through the tasks in this role to gain an understanding of what each control is doing. Some of the tasks are disruptive and can have unintended consequences in a live production system. Also familiarize yourself with the variables in the defaults/main/ directory.

**Technical Dependencies:**

Amazon Linux 2027 - other versions are not supported.

- ansible-core 2.21.0 or newer: Amazon Linux 2027 ships without python3-rpm and python3-libdnf5, and earlier releases cannot gather package facts or manage packages without them
- Collections listed in [collections/requirements.yml](collections/requirements.yml): `community.general`, `ansible.posix`
- Python 3.14 on the managed host (the Amazon Linux 2027 system python)
- python3-libselinux
- If using the audit: access to download or add the syver binary and audit content to the system (other options are
  available for getting the content onto the host)

---

## Auditing

This can be turned on or off within defaults/main/audit.yml with the variable run_audit. The value is false by default, please refer to the wiki for more details. The defaults file also populates the audit checks to check only the controls that have been enabled in the ansible role.

This is a much quicker, very lightweight, checking (where possible) config compliance and live/running settings.

The audit uses a small go binary called [syver](https://github.com/krameff/syver), the continuation of [goss](https://github.com/krameff/goss), along with the relevant configurations to check. Without the need for infrastructure or other tooling.
Syver is a signed fork that is regularly updated. The audit content needs syver 0.16.0 or later: tests that do not apply to the host are reported as skipped with a reason. Set `audit_bin_verify_signature: true` to verify the release signature before the binary is downloaded.
This audit will not only check the config has the correct setting but aims to capture if it is running with that configuration also trying to remove [false positives](https://www.mindpointgroup.com/blog/is-compliance-scanning-still-relevant/) in the process.

Refer to [AMAZON2027-CIS-Audit](https://github.com/ansible-lockdown/AMAZON2027-CIS-Audit).

## Example Audit Summary

This is based on a vagrant image with selections enabled. e.g. No Gui or firewall.
Note: More tests are run during audit as we check config and running state.

```txt

ok: [testhost] => {
    "msg": [
        "The pre remediation audit results are: Count: 564, Failed: 156, Skipped: 18, Duration: 4.176s",
        "The post remediation audit results are: Count: 564, Failed: 55, Skipped: 15, Duration: 4.280s",
        "Full breakdown can be found in /opt"
    ]
}

PLAY RECAP *******************************************************************************************************************************************
testhost                   : ok=396  changed=143  unreachable=0    failed=0    skipped=155  rescued=0    ignored=0
```

## Documentation

- [Read The Docs](https://ansible-lockdown.readthedocs.io/en/latest/)
- [Getting Started](https://www.lockdownenterprise.com/docs/getting-started-with-lockdown#GH_AL_AMAZON2027_cis)
- [Customizing Roles](https://www.lockdownenterprise.com/docs/customizing-lockdown-enterprise#GH_AL_AMAZON2027_cis)
- [Per-Host Configuration](https://www.lockdownenterprise.com/docs/per-host-lockdown-enterprise-configuration#GH_AL_AMAZON2027_cis)
- [Getting the Most Out of the Role](https://www.lockdownenterprise.com/docs/get-the-most-out-of-lockdown-enterprise#GH_AL_AMAZON2027_cis)

## Role Variables

This role is designed that the end user should not have to edit the tasks themselves. All customizing should be done via the defaults/main/ files or with extra vars within the project, job, workflow, etc.

## Tags

There are many tags available for added control precision. Each control has its own set of tags noting what level, what OS element it relates to, whether it's a patch or audit, and the rule number. Additionally, NIST references follow a specific conversion format for consistency and clarity.

### Conversion Format for NIST References:

  1. Standard Prefix:
    - All references are prefixed with "NIST".

  2. Standard Types:
    - "800-53" references are formatted as NIST800-53.
    - "800-53r5" references are formatted as NIST800-53R5 (with 'R' capitalized).
    - "800-171" references are formatted as NIST800-171.

  3. Details:
    - Section and subsection numbers use periods (.) for numeric separators.
    - Parenthetical elements are separated by underscores (_), e.g., IA-5(1)(d) becomes IA-5_1_d.
    - Subsection letters (e.g., "b") are appended with an underscore.
Below is an example of the tag section from a control within this role. Using this example if you set your run to skip all controls with the tag services, this task will be skipped. The opposite can also happen where you run only controls tagged with services.

```sh
      tags:
      - level1-server
      - level1-workstation
      - scored
      - avahi
      - services
      - patch
      - rule_2.2.4
```

## Community Contribution

We encourage you (the community) to contribute to this role. Please read the rules below.

- Your work is done in your own individual branch. Make sure to Signed-off-by and GPG sign all commits you intend to merge.
- All community Pull Requests are pulled into the devel branch
- Pull Requests into devel will confirm your commits have a GPG signature, Signed-off-by, and a functional test before being approved
- Once your changes are merged and a more detailed review is complete, an authorized member will merge your changes into the main branch for a new release

## Pipeline Testing

uses:

- ansible-core 2.16
- ansible collections - pulls in the latest version based on requirements file
- runs the audit using the devel branch
- This is an automated test that occurs on pull requests into devel
- self-hosted runners using OpenTofu

## Known Issues

EPEL and many third-party or cloud provider repositories do not support gpgcheck (rule_1.2.1.2) or repo_gpgcheck (rule_1.2.1.3). This will cause issues during the playbook unless a workaround is found.

## Local Testing

### example

```bash
molecule test -s default
molecule converge -s wsl -- --check
molecule verify -s localhost
```

local testing uses:

- ansible-core
- molecule 4.0.1
- molecule-docker 2.0.0
- molecule-podman 2.0.2
- molecule-vagrant 1.0.0
- molecule-azure 0.5.0

## Credits and Thanks

Massive thanks to the fantastic community and all its members.

This includes a huge thanks and credit to the original authors and maintainers.

Mark Bolwell, George Nalen, Steve Williams, Fred Witty
