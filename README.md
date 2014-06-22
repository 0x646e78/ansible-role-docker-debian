ansible-role-docker-debian
==========================

Ansible role to set up docker on Debian

Use
---

You can clone this repo directly into your ansible playbook by issuing

```
git clone https://github.com/auraltension/ansible-role-docker-debian.git roles/docker-debian
```

or alternatively as a submodule in much the same way

```
git submodule add https://github.com/auraltension/ansible-role-docker-debian.git roles/docker-debian
```

You can then include this role as part of a playbook such as:

```
---
- hosts: my_server
  roles:
    - docker-debian
```

Credits
-------

The install process for docker mostly guided by https://scottlinux.com/2014/05/04/how-to-install-and-run-docker-on-debian-wheezy/
