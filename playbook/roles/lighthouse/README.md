Role Name
=========

This role install lighthouse.

Dependencies
------------
[Nginx-role](https://github.com/SeNike/ansible-nginx.git)

Add next to requirements.yaml:

```requirements.yaml
  - src: git@github.com:SeNike/ansible-nginx.git
    scm: git
    version: "1.0.0"
    name: nginx 
```    

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: lighthouse }

License
-------

MIT

Author Information
------------------

Sergey Nikiforov
