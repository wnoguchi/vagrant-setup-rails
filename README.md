Rails Stack w/ Vagrant and Ansible
==========================================================

Requirements
--------------

- Vagrant 1.8.6 or later
- Ansible 2.1 or later
- VirtualBox 5.1.6
- UNIX compatible System(Mac, Linux, etc.)

Usage
-------

### First impression

Simply,

```
vagrant up
```

### Provision After bootup

If you edit Ansible Playbook, provision following:

```
vagrant provision
```

Start Rails
-------------

```
bundle exec rails new aaaaaa -d postgresql
cd aaaaaa
bundle exec rake db:create
bundle exec rails server -b 0.0.0.0
```

Then open a browser, and access or type following URL.

http://localhost:3000/

Make sure all works fine.
To Shutdown Rails server, type Ctrl+C.

More detail information for Ruby on Rails

- [Ruby on Rails Guides](http://guides.rubyonrails.org/)

And few later, you should know RDBMS PostgreSQL or MariaDB, .etc.

1. [PostgreSQL: Documentation: 9.6: PostgreSQL 9.6.0 Documentation](https://www.postgresql.org/docs/9.6/static/index.html)
1. [Learn - MariaDB.org](https://mariadb.org/learn/)
