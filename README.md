Rails Stack w/ Vagrant and Ansible
==========================================================

Requirements
--------------

- Vagrant 1.8.6 or later
- Ansible 2.1 or later
- VirtualBox 5.1.6
- UNIX compatible System(Mac, Linux, etc.)

Components
-------------

- Ruby on Rails 5
- JavaScript runtime: Node.js
- Ruby 2.3.1
- CentOS 7.2.1511
- RDBMS
  - PosgreSQL 9.6
  - MariaDB 5.5.50
- Redis
- Nginx

Usage
-------

### First Boot

Simply,

```
vagrant up
```

### Provision After boot up

If you edit Ansible Playbook, provision following:

```
vagrant provision
```

Start Rails
-------------

```
bundle exec rails new aaaaaa -d postgresql
cd aaaaaa
bin/rake db:create
bin/rails server --bind 0.0.0.0
```

Then open a browser, and access or type following URL.

http://localhost:3000/

Make sure all works fine.
To Shutdown Rails server, type Ctrl+C.

WEBRick is not used in Rails5 generation.

```
=> Booting Puma
=> Rails 5.0.0.1 application starting in development on http://0.0.0.0:3000
=> Run `rails server -h` for more startup options
Puma starting in single mode...
* Version 3.6.0 (ruby 2.3.1-p112), codename: Sleepy Sunday Serenity
* Min threads: 5, max threads: 5
* Environment: development
* Listening on tcp://0.0.0.0:3000
Use Ctrl-C to stop
Started GET "/" for 10.0.2.2 at 2016-10-09 10:01:19 +0000
Cannot render console from 10.0.2.2! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by Rails::WelcomeController#index as HTML
  Parameters: {"internal"=>true}
  Rendering vendor/bundle/ruby/2.3.0/gems/railties-5.0.0.1/lib/rails/templates/rails/welcome/index.html.erb
  Rendered vendor/bundle/ruby/2.3.0/gems/railties-5.0.0.1/lib/rails/templates/rails/welcome/index.html.erb (2.7ms)
Completed 200 OK in 25ms (Views: 5.9ms | ActiveRecord: 0.0ms)
```

More detail information for Ruby on Rails

- [Ruby on Rails Guides](http://guides.rubyonrails.org/)

And few later, you should know RDBMS PostgreSQL or MariaDB, .etc.

1. [PostgreSQL: Documentation: 9.6: PostgreSQL 9.6.0 Documentation](https://www.postgresql.org/docs/9.6/static/index.html)
1. [Learn - MariaDB.org](https://mariadb.org/learn/)
