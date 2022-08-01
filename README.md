Henry.Starrocks
=========

Install and manage StarRocks automatically

Prepare
------------
1. Installed the JAVA on all FE
2. Installed the Mysql client on the master of all FE
3. Set up SSH without passwords
4. Download it from https://www.starrocks.com/zh-CN/download/community to directory (henry.starrocks/files)
5. Add hosts in /etc/ansible/hosts
e.g:
```
[dorisdb_all]
192.168.30.128
192.168.30.129
192.168.30.130

[dorisdb_frontends]
192.168.30.128
192.168.30.129

[dorisdb_master]
192.168.30.128

[dorisdb_follower]
192.168.30.129

[dorisdb_backends]
192.168.30.128
192.168.30.129
192.168.30.130

[dorisdb_brokers]
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
- hosts: dorisdb_all
  roles:
    - henry.starrocks
```

License
-------

MIT

Author Information
------------------

Henry Yu <haoyuanfen81@gmail.com>
