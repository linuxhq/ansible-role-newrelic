# ansible-role-newrelic

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-newrelic.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-newrelic)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-newrelic-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/newrelic)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - NewRelic RPM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    newrelic_arch: noarch
    newrelic_baseurl: "https://yum.newrelic.com/pub/newrelic/el5/{{ ansible_architecture }}"
    newrelic_disablerepo: []
    newrelic_enablerepo: []
    newrelic_fetch: "{{ newrelic_baseurl }}/{{ newrelic_release }}.{{ newrelic_arch }}.rpm"
    newrelic_packages: []
    newrelic_pkg: newrelic-repo
    newrelic_rel: 3
    newrelic_release: "{{ newrelic_pkg }}-{{ newrelic_ver }}-{{ newrelic_rel }}"
    newrelic_repository_newrelic: false
    newrelic_ver: 5

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.newrelic
          newrelic_repository_newrelic: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
