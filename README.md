*Raspbridge!*
=========

Introducing *Raspbridge*, an easy way to turn your Raspberry Pi into a iPhone to Ethernet Bridge.

Requirements
------------

* Raspberry Pi with Raspbian Jesse
* An iPhone with the Personal Hotspot feature enabled
* A USB to Lighting cable

Role Variables
--------------
All variables are defined in `defaults/main.yml` and can be changed or overridden to suit your needs, though you shouldn't *need* to. This is assuming the Raspberry Pi's network card is `eth0` and the iphone bridge shows up as `eth1`.
###### defaults/main.yml
```
bridge_interface: eth0
bridge_interface_address: 172.24.1.1
bridge_netmask: 255.255.255.0
bridge_network: 172.24.1.0
bridge_broadcast: 172.24.1.255
bridge_cidr: 24
dns_server: 8.8.8.8
dhcp_range: 172.24.1.5,172.24.1.15
iphone_interface: eth1
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: raspberrypi
      roles:
         - ansible-raspbridge

License
-------

BSD

Author Information
------------------

[Tom Reeb](https://www.tomreeb.com)
