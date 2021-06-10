Create User
=========

Create a basic user and upload ssh public key for remote authentication.

Requirements
------------

No specific required Ansible
Need a default ssh public key or a specific key needs to be called out in a variable

Role Variables
--------------
#define a user you would like to create
user_name: default
#define the user state present or absent
user_state: present
#define the path to ssh public key
ssh_key: ~/.ssh/id_rsa.pub

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

None

Example Playbook
----------------

---
- hosts: all
  become: yes
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/id_rsa.pub

License
-------

MIT

Author Information
------------------

rev@revraikes.com
