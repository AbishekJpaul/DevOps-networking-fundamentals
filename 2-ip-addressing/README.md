# IP Address

An IP (Internet Protocol) Address is a unique identifier assigned to a device connected to a network.

## Why do we need IP addresses?

- To uniquely identify devices.
- To enable communication between systems.
- To monitor and troubleshoot network activity.
- To route packets across networks.

### Example

- 172.16.3.4
- 10.1.2.4

# IPv4

IPv4 consists of 32 bits divided into four octets.

### Example:

192.168.1.10

Each octet ranges from:

|0 - 255  | 0-255 | 0-255 | 0-255 |
|  8bits  | 8bits | 8bits |  8bits|

### Example:

192 = 128(2^7) + 64(2^6)


# CIDR 

CIDR (Classless Inter-Domain Routing) is used to define network ranges.

### Example:

172.16.3.0/24

- /24 means 24 bits are reserved for the network.
- Remaining 8 bits are used for hosts.

### Host Calculation:

2^(32-24) = 256 addresses

# Private IP Ranges

RFC1918 defines the following private IP ranges:

| Range | CIDR |
|------|------|
| 10.0.0.0 - 10.255.255.255 | /8 |
| 172.16.0.0 - 172.31.255.255 | /12 |
| 192.168.0.0 - 192.168.255.255 | /16 |

These addresses are commonly used inside organizations and cloud environments such as AWS VPCs.
