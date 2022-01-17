# Ports

Computers access nodes across a network (local or internet) through ports

Think of the computer as a garden with an infinite hedge across all sides. 
Without building a gate you cannot see any other peoples gardens and no one can see yours

A gate allows entry and exit for one person at once and lets communication happen

## Specific ports

Computers have 65,535 ports they can use, meaning there at most can be 65,000 different 
openings and exits where communication can happen, which is plenty of communcation

Some common ports: 
20 / 21  - File transfer 
22       - SSH
25       - Simple Mail Transfer Protocol (email)
80       - HTTP (Websites) 
443      - HTTPS (Secure websites)

and a bunch of others

*generally* ports 8000 and upwards are reserved for software development, we will normally use these ports within programming

What happens if you use a port already used?? What happens if two people try to walk through the gate at the same time? 

How to see the ports

Using git bash / power

`netstat a`