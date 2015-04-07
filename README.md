aspects_mysql_client
========

Ensure that the mysql command line client tools are installed. This does not install the server.

Requirements
------------

Set ```hash_behaviour=merge``` in your ansible.cfg file.

Tasks will not run unless ```aspects_mysql_client_enabled``` is set to ```True```.

Role Variables
--------------

```yaml
aspects_mysql_client_package_name:
  Debian: "mysql-client"
  RedHat: "mysql"
```
Simply override the ```aspects_mysql_client_packge_name``` dictionary in your local vars files, if you need to change package names.

### aspects_mysql_client_enabled
True or False, determines if the role tasks are run or not.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - aspects_mysql_client
      vars:
        aspects_mysql_client_enabled: True

License
-------

MIT
