Ansible role to install docker ce (and/or compose) on Debian.
=========

This is an ansible role to install docker-ce, from the official apt repo, with various options, such as installing docker-compose and disabling the docker iptables dynamic rules.

It's probably not very generic outside of Debian 10+, but please raise any 
Issues or PR for any Debian based distro and version.

To install using ansible-galaxy:

```
ansible-galaxy install 0x646e78.docker_debian
```

Alternatively, you could add this repo as a submodule:

```
git submodule add https://github.com/auraltension/ansible-role-docker-debian.git roles/docker-debian
git submodule init roles/docker_debian
```

Requirements
------------

Probably nothing, raise an issue if you find something.

Role Variables
--------------

- `iptables: true` - Set to false to disable docker controlled iptables rules.
- `install_compose: false` - Set to true to install docker-compose

Dependencies
------------

None

Example Playbook
----------------


```
---
- hosts: my_server
  roles:
    - { role: docker_debian, iptables: false }
```

License
-------

GPL-2.0

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

Author Information
------------------

DNX - [blog](http://blog.ghostinashell.com) - [Docker Hub](https://hub.docker.com/r/ectoplasm/plantuml) - [Ansible Galaxy](https://galaxy.ansible.com/0x646e78)
