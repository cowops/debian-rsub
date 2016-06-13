Debian-Rsub
============

Edit files from an ssh session in Sublime Text

Requirements
------------

This role requires a debian compliant system such as ubuntu.

Locally, you need to edit your `~/.ssh/config` in order to automatically create an ssh tunnel from remote port 52699 to local port 52698 such as :

```
Host *
  RemoteForward 52699 localhost:52698
```

Role Variables
--------------

- rsub:
  - ports:
    -  remote: 52699
    -  local: 52698

Dependencies
------------

- cowops.debian-rmate

None

Example Playbook
----------------

  - hosts: servers
    roles:
       - { role: cowops.debian-rsub }

Tasks
-----

  - Install rsub command

License
-------

BSD
