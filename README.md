nginx Ansible playbook
======================

[![Travis
CI](http://img.shields.io/travis/erasme/ansible-nginx.svg?style=flat)](http://travis-ci.org/erasme/ansible-ruby)
[![test-suite](http://img.shields.io/badge/ansible--roles--specs-ansible--nginx-blue.svg?style=flat)](https://github.com/erasme/ansible-roles-specs/tree/master/ansible-nginx/)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-erasme.nginx-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2909)

This role will install nginx but is very basic, and configuration pretty
limited.

Requirements
------------

erasme.php5-fpm is `nginx_mode` is set to `php5-fpm`.

Role Variables
--------------

  - nginx_root: web directory root for 'default' vhost (default: `/var/lib/nginx/`)
  - nginx_worker_connections: sets the maximum number of simultaneous connections that can be opened by a worker process (default: 1024)
  - nginx_mode: whether we'll run php5-fpm (default: php5-fpm)
  - nginx_add_default: do we add a default vhost (default: yes)

Tags
----

  - nginx

Dependencies
------------

  - [php5-fpm](https://github.com/erasme/ansible-php5-fpm) is `nginx_mode` is set to `php5-fpm`.

Example Playbook
----------------


License
-------

MIT

Author Information
------------------

Created for @erasme by @leucos.

