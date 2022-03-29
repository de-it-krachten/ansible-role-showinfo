[![CI](https://github.com/de-it-krachten/ansible-role-showinfo/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-showinfo/actions?query=workflow%3ACI)


# ansible-role-showinfo

Show basic platform information using facts

Platforms
--------------

Supported platforms

- CentOS 7
- RockyLinux 8
- AlmaLinux 8
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS



Role Variables
--------------
<pre><code>

</pre></code>


Example Playbook
----------------

<pre><code>
- name: sample playbook for role 'showinfo'
  hosts: all
  vars:
  tasks:
    - name: Include role 'showinfo'
      include_role:
        name: showinfo
</pre></code>
