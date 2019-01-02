shellbro.emacs
==============

[![Build Status](https://travis-ci.org/shellbro/ansible-role-emacs.svg?branch=master)](https://travis-ci.org/shellbro/ansible-role-emacs)

Ansible role for installing GNU Emacs from sources on CentOS 7.

This is useful if Emacs version newer than available in repository is needed. As
for this writing, the latest version of Emacs available in *updates* repo is
*24.3*.

Requirements
------------

None

Role Variables
--------------

* source_url - URL to Emacs source code archive (required)
* source_dir - directory on the system to store downloaded source code (by
default `/root/src`)
* config_url - URL to init.el config file (required if users list is not empty)
* users - list of users for whom configure Emacs (by default empty list)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - shellbro.emacs
          source_url: https://ftp.gnu.org/pub/gnu/emacs/emacs-26.1.tar.gz
          config_url: https://raw.githubusercontent.com/shellbro/dotfiles/master/.emacs.d/init.el
          users:
            - shellbro

License
-------

BSD

Author Information
------------------

Jakub Gorczyca
