# Docker Networking

Docker Networking enables communication between containers, the host machine, and external networks. It is one of the core concepts every DevOps Engineer should understand.

## Why Docker Networking?

- Enables container-to-container communication.
- Allows containers to access external services.
- Isolates application components.
- Supports scalable microservices architecture.

---

## Types of Docker Networks

### 1. Bridge Network

- Default Docker network.
- Allows communication between containers on the same host.
- Automatically created during Docker installation.

### Example

```bash
docker network ls
docker run -d --name nginx nginx
docker inspect nginx
```

### Use Cases

- Local development
- Single-host applications

---

### 2. Host Network

- Container shares the host's network stack.
- No network isolation.

### Example

```bash
docker run --network host nginx
```

### Use Cases

- High-performance applications
- Monitoring tools

---

### 3. None Network

- Completely disables networking for a container.

### Example

```bash
docker run --network none alpine
```

### Use Cases

- Security testing
- Isolated workloads

---

### 4. Overlay Network

- Enables communication between containers across multiple Docker hosts.
- Commonly used with Docker Swarm.

### Use Cases

- Multi-host deployments
- Container orchestration

---

### 5. Macvlan Network

- Assigns a MAC address to containers.
- Containers appear as physical devices on the network.

### Use Cases

- Legacy applications
- Network appliances

---

## Docker Network Commands

### List Networks

```bash
docker network ls
```

### Create a Network

```bash
docker network create my-network
```

### Inspect a Network

```bash
docker network inspect bridge
```

### Connect a Container

```bash
docker network connect my-network nginx
```

### Disconnect a Container

```bash
docker network disconnect my-network nginx
```

### Remove a Network

```bash
docker network rm my-network
```

---

## Docker Networking Architecture

```text
Client
   |
   v
Host Machine
   |
   +-- Bridge Network
   |      |
   |      +-- Container A
   |      +-- Container B
   |
   +-- Host Network
   |
   +-- Overlay Network
          |
          +-- Docker Host 1
          +-- Docker Host 2
```

---

## Real-World Example

Consider a three-tier application:

- Frontend (React)
- Backend (Node.js)
- Database (MySQL)

Docker Networking allows:

- Frontend → Backend communication
- Backend → Database communication
- Isolation between services

---

## Interview Questions

1. What is Docker Networking?
2. Explain Bridge, Host, and Overlay networks.
3. What is the default Docker network?
4. How do containers communicate with each other?
5. What is the difference between Host and Bridge networking?
6. What is Docker Swarm Overlay Networking?

---

## Key Takeaways

- Docker provides multiple networking options.
- Bridge is the default network type.
- Overlay networks enable multi-host communication.
- Host networking provides maximum performance.
- Understanding Docker Networking is essential for containerized applications.
