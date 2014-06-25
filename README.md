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

Licensing
---------

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or (at
your option) any later version.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, refer to: 
https://www.gnu.org/licenses/gpl-2.0.html

Credits
-------

The install process for docker mostly guided by https://scottlinux.com/2014/05/04/how-to-install-and-run-docker-on-debian-wheezy/

