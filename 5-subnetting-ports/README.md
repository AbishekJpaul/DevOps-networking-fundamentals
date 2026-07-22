# Subnetting

## What is Subnetting?

Subnetting is the process of dividing a large network into multiple smaller networks (subnets). It helps improve network performance, security, and efficient IP address utilization.

### Why Subnetting?

- Reduces network congestion.
- Improves security by isolating networks.
- Efficient utilization of IP addresses.
- Easier network management.
- Helps in scaling infrastructure.

## Key Terms

| Term | Description |
|------|-------------|
| IP Address | Unique address assigned to a device. |
| Subnet Mask | Identifies the network and host portions of an IP address. |
| CIDR | Classless Inter-Domain Routing notation (e.g., /24). |
| Network ID | Identifies the network. |
| Host ID | Identifies the device within the network. |
| Broadcast Address | Used to communicate with all devices in a subnet. |

## Common CIDR Values

| CIDR | Subnet Mask | Hosts |
|------|-------------|------|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |

## Example

Suppose we have:

- IP Address: 192.168.1.0/24

We can divide it into two subnets:

1. 192.168.1.0/25
2. 192.168.1.128/25

Each subnet contains 126 usable host IP addresses.

## Subnetting Formula

- Number of Subnets = 2^n
- Number of Hosts = 2^h - 2

Where:

- `n` = Number of borrowed bits.
- `h` = Number of host bits.

## Real-World Example

An organization has:

- HR Department
- Finance Department
- IT Department

Instead of placing all devices in a single network, subnetting creates separate networks:

- HR: 192.168.1.0/26
- Finance: 192.168.1.64/26
- IT: 192.168.1.128/26

This improves security and network management.

## Subnetting in AWS

Subnetting is widely used in AWS VPC.

- Public Subnet:
  - Contains Load Balancers, Bastion Hosts.
  - Connected to an Internet Gateway.

- Private Subnet:
  - Contains EC2 instances, Databases.
  - No direct internet access.

### Example AWS Architecture

```
VPC (10.0.0.0/16)
│
├── Public Subnet (10.0.1.0/24)
│   └── Load Balancer
│
└── Private Subnet (10.0.2.0/24)
    └── EC2 + RDS
```

## Interview Questions

1. What is subnetting?
2. Why do we use subnetting?
3. What is CIDR notation?
4. Difference between public and private subnet?
5. What is a subnet mask?
6. How many hosts are available in a /24 network?
7. Explain subnetting in AWS VPC.

## Conclusion

Subnetting is a fundamental networking concept used to divide networks into smaller segments for better performance, security, and scalability. Every DevOps Engineer should understand subnet masks, CIDR notation, and AWS VPC subnetting.


# Ports

A port is a logical communication endpoint used by applications.

### Examples:

| Service | Port |
|--------|------|
| HTTP | 80 |
| HTTPS | 443 |
| SSH | 22 |
| DNS | 53 |
| Jenkins | 8080 |
| MySQL | 3306 |

### Example:

172.16.3.19:8080

### Where:

- 172.16.3.19 = Host
- 8080 = Application Port
