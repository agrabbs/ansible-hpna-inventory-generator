Ansible-HPNA Dynamic Inventory
=========

This role will build your host file based upon an HPNA group name.

Requirements
------------

Ansible and HPNA. 

Role Variables
--------------

`HPNA_USER`: Your HPNA Service Account 

`HPNA_PASS`: Your HPNA Service Account Password

`HPNA_GROUP`: The HPNA group you want to build your host file around.

`HPNA_API_URL`: The HPNA API URL.

Dependencies
------------

Your imagination.

Example Playbook
----------------

```
- hosts: all
  connection: local
  gather_facts: no
  vars_prompt:
    - name: "hostfile"
      prompt: "What do you want to name your hostfile?"
      private: no
    - name: "HPNA_GROUP"
      prompt: "What group are you looking for?"
      private: no
    - name: "HPNA_USER"
      prompt: "Service Account Username?"
      private: no
    - name: "HPNA_PASS"
      prompt: "Service Account Password?"
      private: yes
```

License
-------

BSD

Author Information
------------------

Andrew Grabbs

Andrew@AndrewGrabbs.com
