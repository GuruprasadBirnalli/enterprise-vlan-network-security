Network Configuration
VLAN Configuration
VLAN	Department
10	HR
20	Finance
30	IT
Router-on-a-Stick

The router uses subinterfaces on GigabitEthernet0/0 for inter-VLAN routing.

HR
interface GigabitEthernet0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
Finance
interface GigabitEthernet0/0.20
encapsulation dot1Q 20
ip address 192.168.20.1 255.255.255.0
IT
interface GigabitEthernet0/0.30
encapsulation dot1Q 30
ip address 192.168.30.1 255.255.255.0
ACL Security

HR and Finance are isolated from each other using an extended ACL.

10 deny ip 192.168.10.0 0.0.0.255 192.168.20.0 0.0.0.255
20 deny ip 192.168.20.0 0.0.0.255 192.168.10.0 0.0.0.255
30 permit ip any any
Meaning
HR → Finance: denied
Finance → HR: denied
Other traffic: permitted
Port Security

Port security was configured on departmental access ports to restrict unauthorized devices.

Verification Commands
show vlan brief
show interfaces trunk
show ip interface brief
show access-lists
show ip interface GigabitEthernet0/0.10
