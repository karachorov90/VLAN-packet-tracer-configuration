Packet Tracer lab for better understanding VLANs


This VLAN example, has a router connecting four different networks, that are on a VLAN management. The VLAN on the right side, network 192.168.15.0 operates on VLAN 15 on the switch, which is configured to be in a range of 20th to 24th port in the switch. This network is isolated from 192.168.5.0 network and yet they both are connected to the same router. The same goes for the devices on the left side. Every device is able to ping its neighbours on the same network, plus its default gateway but, cannot ping the devices from the other networks. The router has its fast ethernet interfaces divided into two channels, this is called router-on-a-stick. Those interfaces are configured with 802.1Q standard protocol. VLAN is also suitable for multi switching, which will decrease the cost of devices. There is Wi-Fi option as well, in case of need, connected to VLAN network 10, fully able to ping the main router.
A router-on-a-stick is an inter-VLAN routing technique in which the router and switch are linked by a single physical interface, thus the name. This technique is used in the majority of contemporary inter-VLAN routing implementations. Router-on-stick does not require numerous physical interfaces on both the router and the switch, in contrast to the conventional inter-VLAN routing technique. Instead, it is possible to configure the router's operating system to operate the router interface as a trunk link, which is then connected to a switch port that is set up in trunk mode. This suggests that switching between different VLANs may be accomplished using a router and switch with a single physical interface. Multi-vendor VLAN support is provided via the IEEE 802.1Q (Dot1q) protocol, which establishes a system of VLAN tagging for Ethernet packets. Several proprietary protocols, including Cisco Inter-Switch Link (ISL) and 3Com's Virtual LAN Trunk (VLT), were in use before the 802.1Q standard was introduced. [18] [20]
Those are the basic commands and steps for creating a VLAN:
Enter privileged EXEC mode:
“enable”.
Configure VLANs:
“configure terminal”.
Create VLANs:
“vlan 10”.
“name FirstDepartment”.
“vlan 20”.
“name SecondDepartment”
Assign VLANs to switch ports:
“interface range FastEthernet0/1-11”. Enters the configuration on the block of ports 1 till 11.
“switchport mode access”. Goes to access mod.
“switchport access vlan 10”. Makes all those ports on VLAN 10.
“interface range FastEthernet0/12-24”. Enters the configuration on the block of ports 12 till 24.
“switchport mode access”. Goes to access mod.
“switchport access vlan 20”. Makes all those ports on VLAN 20.

“interface GigabitEthernet0/1”. Goes to gigabit interface 0/1
“switchport mode trunk”. Makes this interface to act as a trunk. This is the interface, where the switch is connected to the router.
