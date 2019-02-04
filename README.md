shellbro.emacs
==============

[![Build Status](https://travis-ci.org/shellbro/ansible-role-emacs.svg?branch=master)](https://travis-ci.org/shellbro/ansible-role-emacs)

Ansible role for installing GNU Emacs from sources on CentOS 7.

This is useful if Emacs version newer than available in repository is needed. As
of this writing, the latest version of Emacs available in *updates* repo is
*24.3*.

Requirements
------------

None

Role Variables
--------------

* version - version of Emacs to be installed (required)
* source_dir - directory on the system to store downloaded source code, it will
be created if does not exist (by default `/usr/local/src`)
<!-- -->
* config_url - URL to Emacs config file (required)
* config_dir - directory on the system to store downloaded config file, it will
be created if does not exist (required)
* config_owner - owner of the config dir and config file (required)
* config_group - group of the config dir and config file (if not specified, by
default the same as `config_owner`)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: shellbro.emacs
          version: 26.1
          config_url: https://raw.githubusercontent.com/shellbro/dotfiles/master/.emacs.d/init.el
          config_dir: /home/user/.emacs.d
          config_owner: user

License
-------

BSD

Author Information
------------------

Jakub Gorczyca
