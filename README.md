# Ansible role to Install Forever

[![Build Status](https://img.shields.io/circleci/project/crushlovely/ansible-forever-app.svg?style=flat)](https://img.shields.io/circleci/project/crushlovely/ansible-forever-app.svg)
[![Current Version](http://img.shields.io/github/release/crushlovely/ansible-forever-app.svg?style=flat)](https://github.com/crushlovely/ansible-dotenv)

This Ansible role installs Forever and applies a working upstart script.
###NOTE: this role looks for the node bin file in the "current" directory as if an application were to be deployed with capistrano (eg. /home/ubuntu/application/current")###

## Installation

``` bash
$ ansible-galaxy install crushlovely.forever-app,v1.0.0
```

## Variables

``` yaml
app_name: test
app_path: /home/ubuntu/test
server_env: qa
app:
  user: ubuntu
  process_name: test
  forever_file: test
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
    - crushlovely.forever-app
```

## Dependencies

None

## License

MIT