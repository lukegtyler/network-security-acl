# Network Security ACL Lab

## Overview
This project demonstrates the implementation of extended access control lists (ACLs) in Cisco Packet Tracer. The lab was completed as part of Cisco Networking Academy coursework and focuses on configuring and applying security policies to control network traffic.

## Project Demonstration

This lab includes a working Packet Tracer file and configuration demonstrating how ACLs enforce security policies by permitting and denying specific traffic types.

## Key Features

* Extended IPv4 ACL configuration
* Traffic filtering by protocol (HTTP, HTTPS, FTP, ICMP)
* Host-based access control
* Interface-based ACL application
* Default deny behavior with explicit permit rules

## Technologies Used

* Cisco Packet Tracer
* Extended IPv4 ACLs
* TCP/UDP/ICMP filtering
* Interface-level security policies

## Topology

<img width="649" height="325" alt="image" src="https://github.com/user-attachments/assets/0d16abab-1469-46a8-a6a2-29af2b0eafcf" />


## Key Configurations

* Denied HTTP and HTTPS access from specific host
* Denied FTP access from specific host
* Denied ICMP traffic from specific host
* Allowed all remaining traffic using permit statement

## Sample Configuration

```bash
ip access-list extended ACL
 deny tcp host 172.31.1.101 host 64.101.255.254 eq 80
 deny tcp host 172.31.1.101 host 64.101.255.254 eq 443
 deny tcp host 172.31.1.102 host 64.101.255.254 eq 21
 deny icmp host 172.31.1.103 host 64.101.255.254
 permit ip any any
```

## Testing & Validation

- Verified blocked HTTP/HTTPS traffic using browser tests
- Confirmed FTP access was denied for specified host
- Tested ICMP restrictions with ping commands
- Ensured permitted traffic remained functional

## What I Learned

* How ACL rule order affects traffic behavior
* How to restrict specific protocols between hosts
* How to apply security policies at the interface level
* How default deny impacts network communication

## Notes
This lab was completed as part of Cisco Networking Academy coursework and adapted into a documented project to demonstrate practical ACL configuration and traffic control.

## Files Included

- [Download Packet Tracer Lab](lab/Tyler_8.5.13-packet-tracer---configure-extended-ipv4-acls---scenario-2.pka)
- [View Configuration File](configs/acl-configs.txt)
- Network topology screenshot (above)
