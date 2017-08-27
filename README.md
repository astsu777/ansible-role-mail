Ansible Role: Mail Server
=========

This role removes any mail server present and install Postfix instead.

In addition to the installation, Postfix is also configured to use a SMTP relay with SASL authentication. If you want another configuration, please modify this role.

Requirements
------------

No specific requirements for this role.

Role Variables
--------------

The variables for this role by default are the ones used to setup the SMTP relay.

You need to define the hostname of the relay server, as well as the port. You also need to provide the credentials for this relay.

Here is an example of variables:

```
relay_host: smtp.relay.com
relay_port: 25

relay_user: MyUser
relay_password: MyPassword
```

These variables should be defined in either group_vars or host_vars.

Dependencies
------------

No dependencies from other roles required.

Example Playbook
----------------

Here is a simple example playbook to use this role:

```
hosts: all
user: myuser
become: true
roles:
  - { role: mail, tags: [ 'mail' ] }
```

License
-------

MIT / BSD

Author Information
------------------

My name is Gaétan. You can follow me on [Twitter](https://twitter.com/gaetanict)

Website: [ICT Pour Tous](https://www.ictpourtous.com)
