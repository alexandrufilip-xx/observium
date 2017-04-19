Observium
=========

An Ansible Role for deploying Observium  http://www.observium.org/

Requirements
------------

Ubuntu Trusty
Ansible 2.2.*


Role Variables
--------------
'''
observium_db_host: localhost
observium_db_user: observium_db_user
observium_db_pass: observium_db_pass
observium_db_name: observium_db_name
observium_snmp_community: public

observium_users:
  - name: Admin
    password: freeaccess
    level: 10
'''


Dependencies
------------

roles:
 - mysqldb


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - observium


Author Information
------------------

Alexandru Filip @ 2017
