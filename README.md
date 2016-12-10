Role Name
=========

Installs homeassistant to an ubuntu box

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
# default variables
| variable | default value | description |
| --- | --- | --- |
| homeassistant_user | homeassistant | user to run homeassistant as |
| homeassistant_config| /home/{{ homeassistant_user }}/.homeassistant | config directory |
| homeassistant_virtualenv| /home/{{ homeassistant_user }}/.virutalenvironments/homeassistant | virtualenv location |
| homeassistant_systemd| true | install a systemd file for homeassistant | 

# optional roles
| variable | description |
| --- | --- |
| homeassistant_git_config | use a git repo as homeassistant config |
| homeassistant_environment_file | environment variable file to pass to systemd |

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-homeassistant}

License
-------

BSD

Author Information
------------------

matt alleman
