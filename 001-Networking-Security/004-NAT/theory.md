# Network Access Translation

Translates IP from private network to public IP addresses. 
Put into place to allow more IP addresses to access the internet to prevent / slow down IP address running out

## LAN - Local Area Network

Group of local nodes in a geographical area, controlled by a single source. 
Each node has its own private IP, and used to communicate within its network.

Seperate networks can use the same private IP as they don't talk

## NAT 

Nodes in two different networks communicate using the `internet`, they send the data as a `packet` which contains `source ip` and `destination ip`

Router used to send data from node to node, when it sees that the destination IP is not within the local network it sends it to the `firewall`

`firewall` takes the request and sends a duplicate to the internet with a seperate external IP address as the source IP

When the response is received it goes to the firewall, which remembers the private / public network and sends it to the correct local node.

## Tutorial

- Open up powershell / terminal
- ipconfig

compare private ip to external ip (what is my ip)



