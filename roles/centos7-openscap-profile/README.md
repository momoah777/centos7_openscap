Role Name
=========

This role adds the profiles that mainly exist in ssg-rhel7-ds.xml into ssg-centos7-ds.xml to allow CentOS 7 users to perform security auditing and compliance aginst profiles such as the CIS and Essential 8. 

Reference: https://github.com/ComplianceAsCode/content/discussions/7864 

Requirements
------------

This role is designed to work with an internet connection to be able to pull/download the latest ssg datastreams. It also needs a functioning package repository.

Role Variables
--------------

All variables used in this role are defined in default/main.yml. This was to allow the easier substitution of values if needed.

Dependencies
------------

Internet connection

Example Playbook
----------------

$ cat playbooks/centos7-openscap-profile.yml
---
# Ansible Role to create a CentOS7 OpenSCAP profile with extra profiles from RHEL7 

- hosts: localhost
  become: false
  roles:
    - role: centos7-openscap-profile 

$ ansible-playbook playbooks/centos7-openscap-profile.yml --ask-become-pass

License
-------

Apache/BSD

Author Information
------------------

1.0 Mohammad Ahmad &lt;momoah777@gmail.com&gt; - 2021-12-01 First release

