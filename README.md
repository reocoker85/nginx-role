Nginx-role
=========

Install nginx for proper work lighthouse.

Requirements
------------

- OS Fedora 37 on managed nodes.

Role Variables
--------------

- lighthouse_user: "root" 

Dependencies
------------
Install on vm's with lighthouse.

Templates
--------------
nginx.conf.j2 - configuration file nginx.

Example Playbook
----------------

Install role :

- Create file ```requirements.yml``` with:
```yaml
- src: git@github.com:reocoker85/nginx-role.git      
  scm: git
  version: "main"
  name: nginx-role
```
- use command ```ansible-galaxy install -r requirements.yml -p roles``` for downloading role in directory roles.

Use role ( playbook example):

```yaml
- name: Install nginx
  hosts: lighthouse
  become: true
  roles:
    - nginx-role
  tags: nginx
```

Author Information
------------------

### KIG
