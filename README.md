typesafe-activator
========
[![Ansible Role](https://img.shields.io/ansible/role/11845.svg?maxAge=2592000)](https://galaxy.ansible.com/tlehoux/typesafe-activator/)

This is an Ansible role to install typesafe-activator / Play Framework! > 2.3.x.

Typesafe activator must be on a location where you have write access. Running activator writes some files to directories within the distribution. Therefore, this role will install activator in the home directory of the given user.

Requirements
------------

Ansible 1.6

Role Variables
--------------

|Variable|Description|Default|
|---|---|---|
|```activator_version```| see https://www.playframework.com/download#older-versions |1.3.10|
|```activator_offline_dist```|The “offline distribution” comes with all of Activator’s possible dependencies included. It’s a much larger initial download, but installing the offline distribution means that that starting up a new Play project is much faster, as all the dependencies are already resolved.|false|

Dependencies
------------

This role has no dependency. However, Play requires Java 1.8. If you don’t have the JDK, you have to install it.


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: tlehoux.typesafe-activator }
License
-------

BSD

Author Information
------------------

Thomas Lehoux
