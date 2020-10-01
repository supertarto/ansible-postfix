# Ansible Postfix
[![Build Status](https://travis-ci.com/supertarto/ansible-postfix.svg?branch=master)](https://travis-ci.com/supertarto/ansible-postfix)
Install and configure Postfix with Ansible. This role is tested only with Debian, and is very simplistic.

## Requirements
None

## Tested plateform
* Debian 10 (Buster)

## Role variables
postfix_hostname let you define your mailname (your domain name, just after the "@"). I've only tested the smarthost, with a distant SMTP configuration.
```yml
postfix_hostname: "{{ ansible_fqdn }}"
postfix_main_mailer_type: "smarthost"
postfix_smtp: mysmtp
```

## Examples
```yml
---
- hosts: somehost
  roles:
    - supertarto.postfix
  vars:
    postfix_smtp: mysmtp@smtp.com

```

## Installation
```
ansible-galaxy install supertarto.postfix
```
## License
GPL V3.0
