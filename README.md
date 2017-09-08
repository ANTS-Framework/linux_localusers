linux localusers
=========

[![Build Status](https://travis-ci.org/ANTS-Framework/linux_localusers.svg?branch=master)](https://travis-ci.org/ANTS-Framework/linux_localusers)

Take a list of users and use the ansible [user module](http://docs.ansible.com/ansible/latest/user_module.html) to manage local accounts.

Password hashes for most linux distributions can be generated as documented
[here](http://docs.ansible.com/ansible/latest/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module)

Role Variables
--------------

```yml
    linux_localusers__users:
        - {user: 'localadmin', comment: 'Local Administrator', state: 'present', groups: 'wheel', password: '$6$YPQXqTxJc6IEhaSl$of8UJUO6sXkAri2920MzGySrJ.uvHFYNd0ycLtwCmngQyIjg3EY9VG3uUyAfspPOV6eMBO5sVSrBYaDFz7Hxz0'}
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
    - hosts: classroom
      roles:
         - linux_localusers
```

License
-------

GPLv3

Author Information
------------------
Part of the [ANTS Framework](https://ants-framework.github.io/)
