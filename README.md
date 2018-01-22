emacs
=====

[![Build Status](https://travis-ci.org/shellbro/ansible-role-emacs.svg?branch=master)](https://travis-ci.org/shellbro/ansible-role-emacs)

Ansible role for installing GNU Emacs from sources on CentOS 7. This is useful if Emacs version newer than available in repository is needed. As for this writing, the latest version of Emacs available in *updates* repo is 24.3.

Requirements
------------

None

Role Variables
--------------

- version - version of Emacs to be installed (required)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - shellbro.emacs
          version: 25.3

License
-------

BSD

Author Information
------------------

Jakub Gorczyca
