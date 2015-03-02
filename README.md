etherpad Ansible playbook
=========================

[![Travis
CI](http://img.shields.io/travis/erasme/ansible-etherpad.svg?style=flat)](http://travis-ci.org/erasme/ansible-etherpad)
[![test-suite](http://img.shields.io/badge/ansible--roles--specs-ansible--etherpad-blue.svg?style=flat)](https://github.com/erasme/ansible-roles-specs/tree/master/ansible-etherpad/)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-erasme.etherpad-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2998)

This playbook will install etherpad from source.

Requirements
------------

The following packages will be installed by this role :
  - gzip
  - git-core
  - curl
  - python
  - libssl-dev
  - pkg-config
  - build-essential

Role Variables
--------------

  - `etherpad_deploy_user`: user to deploy application to; application will be deployed in ~user/etherpad (default: `etherpad`)
  - `etherpad_log_parent_dir`: parent log directory; the role will create and etherpad subdirectory for logging purposes (default: `/var/log`)
  - `etherpad_port`: the port etherpad will listen to (default: 9001)
  - `etherpad_session_key`: a random session key (default: )
  - `etherpad_version`: which version to deploy (default: `master`)
  - `etherpad_path`: the URI path under which etherpad will be served; if the path is not '/' (default), `nginx` role will be installed to route the application.
  - `etherpad_repos`: the git repos for etherpad (default: https://github.com/ether/etherpad-lite.git)

Tags
----

  - `etherpad` : applies to the whole role

Dependencies
------------

None

Example Playbook
----------------

This is mainly used as a dependency in your existing playbooks, like:

    dependencies:
      - { role: etherpad }

License
-------

MIT

Author Information
------------------

Created for @erasme by @leucos.

