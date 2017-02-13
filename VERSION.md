Ansible Role: Utils
=========
| Master branch | Developer branch | 
|:---:|:---:|
|[![Build Status](https://travis-ci.org/insspb/ansible-role-utils.svg?branch=master)](https://travis-ci.org/insspb/ansible-role-utils) | [![Build Status](https://travis-ci.org/insspb/ansible-role-utils.svg?branch=develop)](https://travis-ci.org/insspb/ansible-role-utils)|

Versions:
------------
##### v3.0: Big update. Prepared to work with Rundeck
- Readme updated
- Versions file updated
- bash-completion added for CentOS systems
- RedHat Playbook: EPEL Key fixed
- RedHat Playbook: Become instructions added to run under not root user. become_method should be specified in inventory.
- Ubuntu Playbook: Separated from Debian playbook, become method updated to sudo
- Ubuntu/Debian Playbooks: Always checks for aptitude present before soft update (Not intalled by default in Ubuntu 16.04/Debian 8, used by ansible module)
- Vars: Vars files is now OS dependent, so var names now identical for Redhat/Debian/Ubuntu
- All playbooks: Ansible syntax update
- bash-completion added to CentOS basic tools
##### v2.3: Software list update
- net-tools added for CentOS 7.

##### v2.2: Software list update
- Git app added. 

##### v2.1: Ansible 2.1 support
- Role internal structure updated
- with_items updated to get rid of Ansible 2.1 deprecation messages
- Telnet app added. 

##### v2.0: MultiOS Support
 - Debian support, tests passed
 - Centos support, tests passed
 - Epel repository install on CentOS systems
 - RepoForge repository install on CentOS 5 systems

##### v1.0: First release. Publishing to Ansible Galaxy ready
 - Ubuntu support, tests passed
 - System updates included
 - List on/off function
 - Custom list included
