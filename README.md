ansible-homeassistant
=========
[![Build
Status](https://travis-ci.org/rmalleman/ansible-homeassistant.svg?branch=master)](https://travis-ci.org/rmalleman/ansible-homeassistant)

Installs [homeassistant](https://home-assistant.io/) to an ubuntu box.

Role Variables
--------------
# default variables
| variable | default value | description |
| --- | --- | --- |
| homeassistant_user | homeassistant | user to run homeassistant as |
| homeassistant_config| /home/{{ homeassistant_user }}/.homeassistant | config directory |
| homeassistant_virtualenv| /home/{{ homeassistant_user }}/.virutalenvironments/homeassistant | virtualenv location |

# optional variables
| variable | description |
| --- | --- |
| homeassistant_git_config | use a git repo as homeassistant config |
| homeassistant_environment_file | environment variable file to pass to systemd |
| homeassistant_additional_pip_dependencies | list of additional pip dependencies to install |
| homeassistant_additional_apt_dependencies | list ofadditional apt dependencies to install |

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-homeassistant}

License
-------

BSD

Author Information
------------------

matt alleman
