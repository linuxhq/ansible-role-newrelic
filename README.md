# ansible-role-newrelic

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-newrelic.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-newrelic)

RHEL/CentOS - NewRelic RPM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    newrelic_pkg: newrelic-repo
    newrelic_ver: 5
    newrelic_rel: 3
    newrelic_arch: noarch
    newrelic_baseurl: "https://yum.newrelic.com/pub/newrelic/el5/{{ ansible_architecture }}"
    newrelic_release: "{{ newrelic_pkg }}-{{ newrelic_ver }}-{{ newrelic_rel }}"
    newrelic_fetch: "{{ newrelic_baseurl }}/{{ newrelic_release }}.{{ newrelic_arch }}.rpm"
    newrelic_repos:
      newrelic: False

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.newrelic
          newrelic_repos:
            newrelic: True

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
