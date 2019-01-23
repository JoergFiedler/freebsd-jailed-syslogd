freebsd-jailed-syslogd
======================

[![Build Status](https://travis-ci.org/JoergFiedler/freebsd-jailed-syslogd.svg?branch=master)](https://travis-ci.org/JoergFiedler/freebsd-jailed-syslogd)

This role provides a jailed syslogd server. Nothing more.

Requirements
------------

This role is intent to be used with a fresh FreeBSD 11.2 installation. There is a Vagrant Box with providers for VirtualBox and EC2 you may use.

Role Variables
--------------

##### syslogd_net

The network mask the jail accepts syslog messages from. Default: `'{{ jail_net_ip }}/24'`.

Dependencies
------------

- [JoergFiedler.freebsd-jailed](https://galaxy.ansible.com/joergfiedler/freebsd-jailed)

Example Playbook
----------------

    - include_role:
        name: 'JoergFiedler.freebsd-jailed-syslogd'
      vars:
        jail_net_ip: '10.1.0.10'
        jail_name: 'syslogd'
        jail_freebsd_release: '11.2-RELEASE'

License
-------

BSD

Author Information
------------------

If you like it or do have ideas to improve this project, please open an issue on Github. Thanks.
