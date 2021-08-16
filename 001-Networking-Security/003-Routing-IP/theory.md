# Routing and IP

IP addresses similar to post code, way to identify a specific node
Each IP address can be assigned to one device at a time 

## IPv4
IPv4 are 32-bit binary addresses
4 octets each containing 8 bits

127.0.0.1 = 01111111.00000000.00000000.00000001

Each 1 from right to left adds base 2 (same as multiplying by 10, but multiplying by 2)

01111111 = 1 + (1 x 2) + (1 x 4) + (1 x 8) + (1 x 16) + (1 x 32) + (1 x 64) + (0 x 128) = 127

10^0 = 1
10^1 = 10
10^2 = 100
10^3 = 1000

2^0 = 1
2^1 = 2
2^2 = 4
2^3 = 8
2^7 = 

max number = 255
min = 0
total combinations = 256
256 * 256 * 256 * 256 = number of IP addresses
4,294,967,296 IP addresses 2^32

Exercise convert your IP address into binary (manually)
81.103.99.1
(divide by 2 and keep the remainder) 81 / 2 = 40 r1 
_ _ _ _ _ _ _ 1
40 / 2 = 20
_ _ _ _ _ _ 0 1 20
_ _ _ _ _ 0 0 1 10
_ _ _ _ 0 0 0 1 5
_ _ _ 1 0 0 0 1 2
0 0 0 1 0 0 0 1 0

1010001

81 / 2 = 40 
40 / 2 = 20
20 / 2 = 10
10 / 2 = 5
5 / 2 = 2
2 / 2 = 1 

## CIDR

Majority of devices in a network begin with the same octet(s)

81.103.99.1
81.103.206.72
81.103.150.27

IP consists of:
- Network Prefix  - What is the network
- Host identifier - What is the specific device on this network

Length of network prefix and host identifier is dependant on CIDR
Classless Inter-Domain Routing Notation

81.103.0.0 / 16
81.103.206.72 / 16
First 16 bits (out of 32 (8 bits * 4)) are fixed - leaving 16 bits for devices
256 * 256 possible devices

https://www.ipaddressguide.com/cidr

81.103.0.0 / 17 
Min - 81.103.0.0
Max - 81.103.127.255 (third can be between 0 and 127) 

81.103.200.0 / 17 
Min - 81.103.128.0
Max - 81.103.255.255 (third can be between 0 and 127) 
Demonstrate with graphical bits

290.158.70.0 / 25 
First 3 octates are fixed, final octate has 1 bit fixed, half of the IPs are allowed (0 - 127)

### Exercise

What is the minimum, maximum IP addresses AND number of addresses 

41.142.34.0 / 24
4.102.0.0 / 17
67.249.196.0 / 26
136.70.0.75 / 19
121.151.0.100 / 25
200.35.193.43 / 20

## Ports

An ip address is a node (which is the entire device)
Most of the time you use a `service` which is a self contained process using some of the node.

Within a node there are 65,535 ports, with the most common ones being
22    - SSH
25   - email
80   - http
8000 - Development
8080 - Java
Accessing generally any website is using <ip address>:<80>

other services are using the other ports

Each Port on a node can be used for one thing, multiple services on one node cant use the same port, ports can also be modified if you need two java apps running etc.


## IPv4 address exhaustion 

(IANA) Internet Assigned Numbers Authority gives out IP addresses for companies to use, 2011 was the first time IANA ran out of IPs to assign. ISPs still have IP addresses to use, but no more IP addresses that aren't cliamed by anyone

- IPv4 addresses in Europe are now all claimed, with ISPs able to transfer unused IP addresses
- Some ISPs and companies transferring to IPv6 (which has a lot more addresses)

## IPv6

Ipv4 - 32 bits of data
IPv6 - 32 * 2 * 2 128 bits of data
340,282,366,920,938,463,463,374,607,431,768,211,456 IPv6 addresses.. a lot

hexidecimal base 16 
0,1,2,3..9, A, B, C, D, E, F
binary base 2 
0, 1
Denary base 10 
0,1,2,3.. 

8 groups of 4 hexadecimal digits seperated by a colon

0000:1234:abcd:0012:1234:1111:5555:ef12 etc.

Any 0's that are at the beginning or end of a group can be removed
0000 - whole group removed
0120 - 12
0101 - 101







