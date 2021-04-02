Ansible NTP Role
=========

Simple Ansible role for configuring default NTP settings using chronyd. 

Current iteration just installs chronyd from YUM, sets up a basic default /etc/chrony.conf file, and enables + starts the service. Future additons will accept variables for the NTP server pool to provide more modular functionality. 


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-ntp-role

License
-------

BSD

