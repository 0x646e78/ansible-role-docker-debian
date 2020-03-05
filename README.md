Install docker-ce on Debian via ansible
===

This is an ansible role to install docker-ce from the official apt repo.

It's probably not very generic outside of Debian 10+, but please raise any 
Issues or PR for any Linux system.

Use
---

You can clone this repo directly into your ansible playbook by issuing

```
git clone https://github.com/auraltension/ansible-role-docker-debian.git roles/docker-debian
```

or alternatively as a submodule in much the same way

```
git submodule add https://github.com/auraltension/ansible-role-docker-debian.git roles/docker-debian
git submodule init roles/docker-debian
```

You can then include this role as part of a playbook such as:

```
---
- hosts: my_server
  roles:
    - docker-debian
```

A basic localhost playbook and execution:

vi `play.yml`
```
---

- hosts: localhost
  roles:
    - /path/to/docker-debian
  vars:
    ansible_python_interpreter: /usr/bin/python
```

    ansible-playbook play.yml --ask-become-pass


Variables
---

`iptables`: Set to false to disable iptables being controlled by Docker.


Licensing
---

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
