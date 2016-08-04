Role Name
=========

  Install NPM and trigger to install plugins.

Requirements
------------

  Ansible >= 1.2
  Better is linux

Role Variables
--------------

  npm_packages: list of packages that you need to install after NPM is installed finished. Default: empty (no install).
  npm_file: file path of package.json for install after NPM is installed. Default: empty (no install).

Dependencies
------------

  None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ledongthuc.ansible.npm, npm: [express,hook.io], npm_file: package.json }

License
-------

  Apache 2.0

Author Information
------------------
  Thuc Le ( ledongthuc[at]gmail.com )
