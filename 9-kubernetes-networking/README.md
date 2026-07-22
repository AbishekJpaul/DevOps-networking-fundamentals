# Kubernetes Networking

Kubernetes Networking enables communication between Pods, Services, and external users within a Kubernetes cluster. It follows a simple principle:

> Every Pod can communicate with every other Pod without NAT.

## Why Kubernetes Networking?

- Enables Pod-to-Pod communication.
- Provides Service discovery.
- Supports Load Balancing.
- Ensures scalability and high availability.
- Simplifies microservices communication.

---

## Kubernetes Networking Model

Kubernetes networking consists of:

1. Pod Networking
2. Service Networking
3. Cluster Networking
4. Ingress Networking

---

## 1. Pod Networking

- Every Pod gets a unique IP address.
- Pods communicate directly with each other.
- No NAT is required.

### Example

```text
Pod A (10.244.1.10)
        |
        |
        v
Pod B (10.244.1.20)
```

---

## 2. Service Networking

Services provide a stable endpoint for Pods.

### Types of Services

| Type | Description |
|------|-------------|
| ClusterIP | Internal communication |
| NodePort | Exposes application externally |
| LoadBalancer | Cloud Load Balancer |
| ExternalName | Maps to external DNS |

### Example

```bash
kubectl expose deployment nginx \
--type=NodePort \
--port=80
```

---

## 3. Cluster Networking

A Kubernetes cluster consists of:

- Master Node
- Worker Nodes
- Pods
- Services

```text
Cluster
   |
   +-- Worker Node 1
   |      |
   |      +-- Pod A
   |
   +-- Worker Node 2
          |
          +-- Pod B
```

---

## 4. Ingress Networking

Ingress manages external access to services.

### Benefits

- Single entry point
- SSL/TLS termination
- Path-based routing
- Host-based routing

### Example

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: app-ingress
```

---

## Kubernetes Networking Components

### kube-proxy

- Handles network routing.
- Maintains Service rules.

### CNI (Container Network Interface)

Popular CNI Plugins:

- Calico
- Flannel
- Cilium
- Weave Net

---

## Common Kubernetes Commands

### View Services

```bash
kubectl get svc
```

### View Pods

```bash
kubectl get pods -o wide
```

### Describe Service

```bash
kubectl describe svc nginx
```

### View Ingress

```bash
kubectl get ingress
```

---

## Real-World Example

Microservices Application:

```text
Ingress
   |
Frontend Service
   |
Backend Service
   |
Database Service
```

Communication Flow:

1. User accesses the application.
2. Ingress receives the request.
3. Service forwards traffic.
4. Pod processes the request.
5. Response is returned to the user.

---

## Interview Questions

1. What is Kubernetes Networking?
2. Explain the Kubernetes networking model.
3. What is a CNI plugin?
4. Difference between ClusterIP and NodePort?
5. What is Ingress?
6. What is kube-proxy?
7. How do Pods communicate across nodes?

---

## Key Takeaways

- Every Pod receives a unique IP.
- Services provide stable access to Pods.
- Ingress manages external traffic.
- CNI plugins enable networking.
- Kubernetes networking is essential for scalable microservices architectures.
