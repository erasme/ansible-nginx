nginx Ansible playbook
======================

[![Travis
CI](http://img.shields.io/travis/erasme/ansible-nginx.svg?style=flat)](http://travis-ci.org/erasme/ansible-nginx)
[![test-suite](http://img.shields.io/badge/ansible--roles--specs-ansible--nginx-blue.svg?style=flat)](https://github.com/erasme/ansible-roles-specs/tree/master/ansible-nginx/)
[![Ansible
Galaxy](http://img.shields.io/badge/galaxy-erasme.nginx-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2964)

This role will install nginx from the nginx PPA. It is very basic, and the
possible configuration pretty limited.

The intent is to have a basic config in place. Later, in your specific roles,
you just need to add entries in `/etc/nginx/sites-available`, link the file in
`/etc/nginx/sites-enable` and restart nginx.

[php5-fpm](https://github.com/erasme/ansible-php5-fpm) can be used in conjunction with this role.

Requirements
------------

None

Role Variables
--------------

  - `nginx_root`: web directory root for 'default' vhost (default: `/var/lib/nginx/`)
  - `nginx_worker_connections`: sets the maximum number of simultaneous connections that can be opened by a worker process (default: 1024)
  - `nginx_mode`: whether we'll run php5-fpm (default: php5-fpm)
  - `nginx_add_default`: do we add a default vhost (default: yes)

Tags
----

  - nginx

Dependencies
------------

None

Example Playbook
----------------

Specs
-----

To run tests locally in a Vagrant machine, just hit:

    vagrant up
    vagrant ssh -c specs

If you want to run the test playbook fast (i.e., without re-installing Ansible),
just run:

    vagrant ssh -c 'specs -p'

There is a sample Guardfile if you want to work on the role in TDD mode. You need to install guard and guard-shell gems, and then run guard:

    gem install guard
    gem install guard-shell
    guard

Now the specs will run whenever you save a file in the role, the specs will be run.

License
-------

MIT

Author Information
------------------

Created for @erasme by @leucos.

