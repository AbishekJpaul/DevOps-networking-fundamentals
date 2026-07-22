## Network

A network is a collection of devices connected together to communicate and share resources such as files, printers, and internet access.

### Examples of devices in a network:

* Computers
* Servers
* Routers
* Switches
* Mobile devices

## Switch

### What is a Switch?

A switch is a networking device used to connect multiple devices within a Local Area Network (LAN).

### Functions

* Connects multiple computers
* Forwards data to the correct device
* Enables communication within the same network

### Example

```
PC1 ----|
PC2 ----|---- Switch
PC3 ----|
PC4 ----|
```

## LAN(Local Area Network)

### LAN (Local Area Network)

A LAN is a network that connects devices within a limited geographical area.

### Examples

* Home network
* School network
* Office network

### Characteristics

* High speed
* Low latency
* Limited coverage area

```
PC ----\
PC ----- Switch ----- PC
PC ----/
```

## WAN(Wide Area Network)

### WAN(Wide Area Network)

A WAN is a network that spans large geographical areas and connects multiple LANs.

### Examples

* Internet
* Corporate branch networks
* Global cloud infrastructure

### Characteristics

* Covers large distances
* Connects multiple LANs
* Uses routers and ISP networks

Office LAN -----> Internet -----> Branch LAN

## Gateway

### Gateway

A gateway acts as the entry and exit point of a network.

### Purpose

* Connects a LAN to external networks
* Allows access to the internet
* Routes traffic between different networks

Computer → Switch → Router/Gateway → Internet

## Client-Server Moedel

### Client-Server Model

The Client-Server model is a communication architecture where a client sends a request and a server processes it and returns a response.

### Real-Life Example

Imagine a restaurant:

* Customer = Client
* Waiter = Communication Channel
* Kitchen = Server
* Food = Response

### Web Example

### When you open Google:

1. Browser sends a request
2. Server receives the request
3. Server processes it
4. Server sends back the webpage

Browser (Client)--> Request-->Server-->Response-->Browser (Client)

## Node

### Node

A node is any device connected to a network.

### Examples

* Computer
* Laptop
* Server
* Printer
* Router
* Switch

## Protocol

### Protocol

A protocol is a set of rules that devices follow to communicate over a network.

### Common Protocols

|Protocol|Purpose|
|--------|-------|
|HTTP| Web communication|
|HTTPS|Secure web communication|
|TCP|Reliable data transfer|
|UDP|Fast data transfer|
|DNS|Domain name resolution|


## OSI Model
The OSI (Open Systems Interconnection) Model explains how data travels from one device to another.
### 7 Layers
|Layer|       Name       |       Function           |
|-----|------------------|--------------------------|
|7    |Application       |User interaction          |
|6    |Presentation      |Encryption & formatting   |
|5    |Session           |Session management        |
|4    |Transport         |TCP/UDP, segmentation     |
|3    |Network           |IP addressing & routing   |
|2    |Data Link         |MAC addressing & switching|
|1    |Physical          |Cables & signals          |

## TCP Three-Way Handshake

TCP establishes a reliable connection using three steps:

```
Client  ---- SYN ----> Server

Client <--- SYN-ACK --- Server

Client ---- ACK ----> Server
```

After the handshake, data transfer begins.

## Data Flow Through OSI Model

When a user visits a website:

```
Application Layer   → HTTPS Request
Presentation Layer  → Encryption (SSL/TLS)
Session Layer       → Session Management
Transport Layer     → TCP/UDP
Network Layer       → IP Addressing
Data Link Layer     → MAC Addressing
Physical Layer      → Electrical/Optical Signals
```

## Key Takeaways

* A network connects devices for communication.
* Switches connect devices within a LAN.
* WAN connects multiple LANs over large distances.
* Gateways provide internet access.
* Client-Server architecture follows a Request-Response model.
* Protocols define communication rules.
* The OSI model explains how data moves through a network.
* TCP uses a 3-way handshake to establish reliable communication.

