# Devices on the network:

1. Router:<br>

    Router0 - ISR4331<br>
    gigabitEthernet0/0/0:<br>
    IP: 168.90.0.1<br>
    Subnet Mask: 255.255.0.0<br>

    gigabitEthernet0/0/1:<br>
    IP: 210.3.14.1<br>
    Subnet Mask:255.255.255.0<br>

2. Switches:<br>
Switch0 - 2960 IOS15<br>
Switch1 - 2960 IOS15<br>

3. Devices connected to first switch:<br>
- PC0 - PC-PT<br>
IP: 168.90.0.3<br>
Subnet Mask: 255.255.0.0<br>

- PC1 - PC-PT<br>
IP: 168.90.0.5<br>
Subnet Mask: 255.255.0.0<br>

- PC3 - PC-PT<br>
IP: 168.90.0.5<br>
Subnet Mask: 255.255.0.0<br>

- Laptop0 - Laptop-PT<br>
IP: 168.90.0.2<br>
Subnet Mask 255.255.0.0<br>

- Server0 - Server-PT<br>
IP: 168.90.0.4<br>
Subnet Mask: 255.255.0.0<br>

4. Devices connected to second switch:<br>
- PC2 - PC-PT<br>
IP: 210.3.14.4<br>
Subnet Mask: 255.255.255.0<br>

- PC4 - PC-PT<br>
IP: 210.3.14.5<br>
Subnet Mask: 255.255.255.0<br>

- Server1 - Server-PT<br>
IP: 210.3.14.2<br>
Subnet Mask: 255.255.255.0<br>

- Server2 - Server-PT<br>
IP: 210.3.14.3<br>
Subnet Mask: 255.255.255.0<br>
<br>

## DHCP setup:
To set up DHCP, I used the following commands on the router's CLI:<br>
Router> enable
Router# Configure terminal   
Router(config)# interface GigabitEthernet0/0/0<br>
Router(config-if)# ip address 168.90.0.1 255.255.0.0<br>
Router(config-if)# no shutdown<br>
Router(config)# interface GigabitEthernet0/0/1<br>
Router(config-if)# ip address 210.3.14.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>