[![Build Status](https://travis-ci.org/merifri/ansible-role-3proxy.svg?branch=master)](https://travis-ci.org/merifri/ansible-role-3proxy)

3proxy Ansible Role
=========

Install 3proxy from source

Requirements
------------

None.

Role Variables
--------------

```
proxy_version: "0.8.12"
proxy_source: "https://github.com/z3APA3A/3proxy/archive/{{ proxy_version }}.tar.gz"

proxy_config_path: "/etc/3proxy"
proxy_service_name: "3proxy"
proxy_system_user: "u3proxy"

proxy_users: []
#- name: test
#  type: CL
#  password: pass

proxy_enabled: True
proxy_log: "/dev/null"
proxy_daemon: True
proxy_allow: "*"
proxy_deny: ""
proxy_auth: "none"
proxy_nserver: []
proxy_nserver6: []
proxy_nscache: 65536
proxy_maxconn: 100

proxy_socks: True
proxy_socks_port: 1080
proxy_socks_options: ""
proxy_http: False
proxy_http_port: 3128
proxy_http_options: ""
```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  roles:
    - role: merifri.3proxy
```

License
-------

MIT
