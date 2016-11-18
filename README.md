Acme-Tiny
=========

This is an ansible role for getting digital certificates with "Let's Encrypt". It is highly influenced by this role: ganto.acme\_tiny. Many thanks [ganto](https://linuxmonk.ch/)!

Why we do not use one of the existing roles?

* For the first reason read the section "Promise" below. We need something reliable.
* This role will be used by [maestro](https://github.com/inofix/maestro) and must follow the logic used there. (Of course, the role can be used without maestro..)

Promise
-------

Sure this role may change in the future, but we will only expand features to not break backwards compatibility.

If radical changes should become necessary, a new role will be created, probably with an 'ng' or version suffix...

Installation
------------

 # ansible-galaxy install zwischenloesung.acme-tiny

Requirements
------------

* Ansible >2.0
* Python2/3 on target host
* Generic UNIX with FHS
* Sudo
* Systemd (per default)

Role Variables
--------------

* app\_\_acme\_\_tiny\_\_user (optional, string: default="acme")
* app\_\_acme\_\_tiny\_\_group (optional, string: default="acme")

Dependencies
------------

Example Playbook
----------------

    - hosts: servers
      roles:
         - zwischenloesung.acme-tiny

License
-------

GPLv3

Author Information
------------------

* Michael Lustenberger at [inofix.ch](http://www.inofix.ch)
