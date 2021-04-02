Ansible NTP Role
=========

Simple Ansible role for configuring default NTP settings using chronyd. 

Current iteration just installs chronyd from YUM, sets up a basic default /etc/chrony.conf file, and enables + starts the service. Future additons will accept variables for the NTP server pool to provide more modular functionality. 


Example Playbook
----------------

Using the role is fairly simple right now. You will just need to create a basic playbook and include it in the roles section:

    - hosts: servers
      roles:
         - ansible-ntp-role

License
-------

BSD

