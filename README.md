[![CI](https://github.com/de-it-krachten/ansible-role-showinfo/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-showinfo/actions?query=workflow%3ACI)


# ansible-role-showinfo

Show basic platform information using facts 



## Dependencies

#### Roles
None

#### Collections
- community.general

## Platforms

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- CentOS 7
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 36
- Fedora 37
- Alpine 3

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# List of default variables to display
showinfo_vars:
  - ansible_distribution
  - ansible_distribution_version
  - ansible_distribution_release
  - ansible_distribution_major_version
  - ansible_os_family
  - cpu_virtualization_support
  - ansible_virtualization_type
  - ansible_virtualization_role
  - ansible_python_version
  - ansible_python_executable

# List of additional variables to display
# Add custom variabled to this list
showinfo_vars_additional: []
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'showinfo'
  hosts: all
  become: "yes"
  tasks:
    - name: Include role 'showinfo'
      ansible.builtin.include_role:
        name: showinfo
</pre></code>
