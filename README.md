Ansible NTP Role
=========

Simple Ansible role for configuring default NTP settings using chronyd. 

Current iteration just installs chronyd from YUM, sets up a basic default /etc/chrony.conf file, and enables + starts the service. Future additons will accept variables for the NTP server pool to provide more modular functionality. 


Example Playbook
----------------

![ansible-ntp-role](
https://raw.githubusercontent.com/cozyviking/ansible-ntp-role/main/files/ansible-ntp-role.gif)

Using the role is fairly simple right now. You will just need to create a basic playbook and include it in the roles section:

```YAML
    - hosts: servers
      become: yes
      roles:
         - ansible-ntp-role
```

Example NTP Output
----------------

Running `chronyc sources` and `chronyc tracking` on the target server(s) should successfully return synchronized NTP output after applying the Ansible role:

![chronyc](
https://raw.githubusercontent.com/cozyviking/ansible-ntp-role/main/files/chronyc-sources.gif)


