# Ansible role to Install Forever

[![Build Status](http://img.shields.io/travis/crushlovely/ansible-forever-app.svg?style=flat)](https://travis-ci.org/crushlovely/ansible-forever-app)
[![Current Version](http://img.shields.io/github/release/crushlovely/ansible-forever-app.svg?style=flat)](https://galaxy.ansible.com/list#/roles/1180)

This Ansible role installs Forever and applies a working upstart script.

## Installation

``` bash
$ ansible-galaxy install crushlovely.forever-app
```

## Variables

``` yaml
app_process_name:
server_env:
app_name:
app_path:
main_forever_file:
```
You can also add a vars folder to your project folder and have your variables served by adding them to a file and calling it in your playbook.

```yaml
- hosts: localhost
...
  vars_files:
    - vars/default_vars.yml
...
```

## Usage

Once this role is installed on your system, include it in the roles list of your playbook.

``` yaml
- hosts: localhost
  roles:
    - { role: crushlovely.forever-app }
```

## Dependencies

None

## License

MIT