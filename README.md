[![Build Status](https://travis-ci.org/ledongthuc/ansible.npm.svg?branch=master)](https://travis-ci.org/ledongthuc/ansible.npm)

Role Name
=========

  Install NPM and trigger to install plugins.

Requirements
------------

  Ansible >= 1.2. 
  Better is linux

Role Variables
--------------

  | Name          | Default          | Description  |
  | ------------- |:---------------- |:------------ |
  | packages      | [] (empty list)  | List packages that you want to install. It supports from file or package's name |

  Each item in packages are defined in http://docs.ansible.com/ansible/npm_module.html

  Example installation stanalone package:
  
    packages:
    - name: coffee-script
      global: false
      version: 1.6.1
      path: /srv/my-website

  Example installation from package.json

    packages:
    - path: /srv/my-website
      global: false

  Example global installation

    packages:
    - name: coffee-script
      global: true 
      version: 1.6.1
      path: /srv/my-website

Dependencies
------------

  None

Example Playbook
----------------

    - hosts: all 
      roles:
      - role: ledongthuc.npm
        packages:
        - global: false
          name: coffee-script
          version: 1.6.1
          path: /srv/my-website
        - global: false
          path: /srv/my-website

License
-------

  Apache 2.0

Author Information
------------------
  Thuc Le - ledongthuc[at]gmail.com
