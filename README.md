# Overview 
This project serves as my personal ansible training library, please feel free to copy/modify/fork as desired.  In the spirit of open-source, it is the hope that this material helps other open-source users and communities learn about Ansible.  Thank you to those who have helped launch this project.

## Goals
- Teaching myself Ansible as a basis of system configuration and automation
- Providing examples for others to do the same
- Expansion past Fedora/CentOS into other distributions

## Assumptions
- The systems are running either Fedora, or CentOS 9 Stream # (for now)
- Each system has a known IP or DNS name
- Each system is online and accessible via SSH

## How to run/deployInstall Ansible:

### For CentOS Stream 9 users
Install EPEL:

```shell
$ sudo dnf install epel-release
```

### Install system requirements
```shell
$ sudo dnf install ansible git-core
```

### Provision an inventory file:
```shell
$ cp inventory-example.yml inventory.yml
$ nano inventory.yml # Set up this file to point to your hosts
```

### Run the playbook:
```shell
$ ansible-playbook -i inventory.yml --ask-pass --ask-become-pass playbook.yml
```

## Licensing
This is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, under version 3 of the License, or
(at your option) any later version.
This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.
You should have received a copy of the GNU General Public License
along with this program. If not, see http://www.gnu.org/licenses/.
