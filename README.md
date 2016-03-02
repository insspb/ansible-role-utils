Ansible Role: Utils
=========
| Master branch | Developer branch | 
|:---:|:---:|
|[![Build Status](https://travis-ci.org/insspb/ansible-role-utils.svg?branch=master)](https://travis-ci.org/insspb/ansible-role-utils) | [![Build Status](https://travis-ci.org/insspb/ansible-role-utils.svg?branch=develop)](https://travis-ci.org/insspb/ansible-role-utils)|

Description
------------

This role installs some must-have utilities. Have several lists inside, so you can disable anything you want. 

##### The list of basic utilities includes:
- **command-not-found**: suggest installation of packages in interactive bash sessions **Not available on CentOS**
- **dstat**: tool for generating system resource statistics
- **htop**: interactive process viewer for Linux
- **atop**: another interactive process viewer for Linux
- **smem**: provides numerous reports on memory usage
- **unzip**: tool to unpack zip archives
- **zip**: tool to pack zip archives
- **gzip**: tool to work wih gzip archives
- **bzip2**: tool to work wih bzip2 archives
- **nano**: basic text editor
- **vim**: advanced text editor **Failed on CentOS 5 (already installed as vi)**

##### The list of network utilities includes:
- **curl**: command line tool for transferring data with URL syntax
- **iftop**: display bandwidth usage on an interface
- **mtr**: a network diagnostic tool
- **tshark**: dump and analyze network traffic
- **nmap**: Security Scanner For Network Exploration & Hacking
- **wget**: Download manager
- **telnet**: This is telnet

##### The list of file system utilities includes:
- **iotop**: display io usage on behalf of which process on an interface
- **ncdu**: interactive console disk usage visualizer
- **lsof**: list open files
- **tree**: recursive directory listing program
- **mc**: old file manager

##### The list of developer utilities includes:
- **pstack**: attaches to the active processes named by the pids on the command line , and prints out an execution stack trace
- **strace**: trace system calls and signals
- **ltrace**: library call tracer

Platforms:
------------
 - CentOS
 - RedHat
 - Debian
 - Ubuntu

Requirements
------------

No requiments yet.

Role Variables
--------------

```yaml
# Role behavior:
utils_install_basic: True               # If set to true role will install basic tools list.
utils_install_network: True             # If set to true role will install network tools list.
utils_install_filesystem: True          # If set to true role will install file system tools list.
utils_install_dev: False                # If set to true role will install developer tools list.
utils_install_user: True                # If set to true role will install list of user configured packages

# Role lists:
utils_list_basic: []                    # Placeholder for list item. Look at vars/main.yml
utils_list_network: []                  # Placeholder for list item. Look at vars/main.yml
utils_list_filesystem: []               # Placeholder for list item. Look at vars/main.yml
utils_list_dev: []                      # Placeholder for list item. Look at vars/main.yml
utils_list_user: []                     # Placeholder for list item. Look at vars/main.yml

# Apt behavior:
utils_update_cache: True                # If set to true role will update application cache before execution.
utils_upgrade_software: True            # If set to true role will upgrade installed soft
utils_cache_valid: "3600"               # How long cache will be valid after update.
utils_upgrade_type: "safe"              # Default upgrade type. You can use:
                                        # If yes or safe, performs an aptitude safe-upgrade
                                        # If full, performs an aptitude full-upgrade
                                        # If dist, performs an apt-get dist-upgrade
```

Dependencies
------------

Independent role.

Example Playbook
----------------
```yaml
- hosts: localhost
  roles:
    - { role: insspb.utils }
```
Development information
----------------
This role is developed with community help. 
Process of development follows this rule: 

 - You are free to add any pool request to develop branch. All request will be answered in timely manner. 
 - If you want to made any contribution, but do not know where to start - check issues.
 - Master branch updated just after significant changes in develop.
 - Please include documentation for new features. 
 - Please use variables.
 - Please do not forget to set defaults.
 - Please do your best to keep backward compatibility if possible.
 - Please use packet installation as default software installation method. Source installation must be optional anywhere if possible.
 - Please use official software developers repositories instead of general Debian/Ubuntu/Centos etc. 
 - Do you best to keep role independent from any other roles. User must have the way to choose what roles to use.

License
-------

MIT

Author Information
------------------

This role is contributed and maintained by [Andrey Shpak](http://www.ashpak.ru). I am always available for [hire](https://www.upwork.com/o/profiles/users/_~01a780866aa29e4429/).
