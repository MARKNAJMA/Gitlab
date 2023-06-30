# Gitlab
CCNP configuration on a switch
hostname R1
interface GigabitEthernet0/0
description To R2
ip address 192.168.1.1 255.255.255.0
interface GigabitEthernet0/1
description To R3
ip address 192.168.2.1 255.255.255.0
router ospf 1
router-id 1.1.1.1
network 192.168.1.0 0.0.0.255 area 0
network 192.168.2.0 0.0.0.255 area 0
line console 0
password cisco
login
This configuration will configure the switch with the following settings:
* The hostname will be R1.
* The interface GigabitEthernet0/0 will be configured with an IP address of 192.168.1.1 and a subnet mask of 255.255.255.0.
* The interface GigabitEthernet0/1 will be configured with an IP address of 192.168.2.1 and a subnet mask of 255.255.255.0.
* OSPF will be enabled with a router ID of 1.1.1.1.
* OSPF will be configured to advertise the networks 192.168.1.0/24 and 192.168.2.0/24 in area 0.
* The console port will be configured with a password of cisco and will require login.
