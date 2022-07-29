Henry.Starrocks
=========

Install and manage StarRocks automatically

Prepare
------------
1. Install ansible
2. Download it from https://www.starrocks.com/zh-CN/download/community to directory (henry.starrocks/files).
3. Add hosts in /etc/ansible/hosts
e.g:
```
[cluster1.all]
192.168.30.128
192.168.30.129
192.168.30.130

[cluster1.frontends]
192.168.30.128
192.168.30.129

[cluster1.master]
192.168.30.128

[cluster1.follower]
192.168.30.129

[cluster1.backends]
192.168.30.128
192.168.30.129
192.168.30.130

[cluster1.brokers]
192.168.30.128
192.168.30.129
192.168.30.130
```


Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

```yml
- hosts: cluster1.all
  roles:
    - henry.starrocks
```

License
-------

MIT

Author Information
------------------

Henry Yu <haoyuanfen81@gmail.com>
