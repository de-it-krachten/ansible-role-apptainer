[![CI](https://github.com/de-it-krachten/ansible-role-apptainer/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-apptainer/actions?query=workflow%3ACI)


# ansible-role-apptainer

Installs apptainer (fka singularity)



## Dependencies

#### Roles
None

#### Collections
None

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
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 39
- Fedora 40

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>

</pre></code>

### defaults/family-RedHat.yml
<pre><code>
# List of RPM packages
apptainer_packages:
  - apptainer
</pre></code>

### defaults/Ubuntu.yml
<pre><code>
# APT repository location
apptainer_apt_url: https://ppa.launchpadcontent.net/apptainer/ppa/ubuntu

# APT signing key
apptainer_apt_key: "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0xf6b0f5193d4f3301ef491ff0afe36534fc6218ae"

# List of APT packages
apptainer_packages:
  - apptainer
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'apptainer'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'apptainer'
      ansible.builtin.include_role:
        name: apptainer
</pre></code>
