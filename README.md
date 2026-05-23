[![CI](https://github.com/de-it-krachten/ansible-role-showinfo/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-showinfo/actions?query=workflow%3ACI)


# ansible-role-showinfo

Show basic platform information using facts 



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- Red Hat Enterprise Linux 10<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- RockyLinux 10
- OracleLinux 8
- OracleLinux 9
- OracleLinux 10
- AlmaLinux 8
- AlmaLinux 9
- AlmaLinux 10
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Ubuntu 26.04 LTS
- Fedora 43
- Fedora 44<sup>1</sup>
- Alpine 3

Note:
<sup>1</sup> : no automated testing is performed on these platforms


## Role Variables
### defaults/main.yml
<pre><code>
# List of default variables to display
showinfo_vars:
  - ansible_facts.distribution
  - ansible_facts.distribution_version
  - ansible_facts.distribution_release
  - ansible_facts.distribution_major_version
  - ansible_facts.os_family
  - ansible_facts.memtotal_mb
  - ansible_facts.processor_vcpus
  - ansible_facts.virtualization_type
  - ansible_facts.virtualization_role
  - ansible_facts.python_version
  - ansible_facts.python.executable
  - ansible_facts.powershell_version
  - ansible_local.cpu.virtualization_support

# List of additional variables to display
# Add custom variabled to this list
showinfo_vars_additional: []
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'showinfo'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'showinfo'
      ansible.builtin.include_role:
        name: showinfo
</pre></code>
