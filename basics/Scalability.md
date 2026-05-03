# Scalability in System Design

## Interview Definition

Scalability is the ability of a system to handle increasing users, traffic, or data by adding resources without significantly affecting performance.

---

# Types of Scalability

## 1. Vertical Scaling (Scale Up)

Increasing the resources of a single server.

### Examples
- Increasing RAM
- Increasing CPU power
- Using faster SSD storage

### Architecture
```txt
Users → One Powerful Server → Database
```

### Advantages
- Easy to implement
- Less architectural complexity
- Good for small applications

### Disadvantages
- Hardware limitations
- Expensive after some point
- Single point of failure

---

## 2. Horizontal Scaling (Scale Out)

Adding multiple servers and distributing traffic among them.

### Architecture
```txt
Users
   ↓
Load Balancer
 ↓    ↓    ↓
S1   S2   S3
```

### Advantages
- Handles massive traffic
- High availability
- Fault tolerance
- Better for distributed systems

### Disadvantages
- Complex architecture
- Requires load balancing
- Data consistency challenges

---

# Real-Time Example

Suppose an application initially supports 1,000 users using one server.

If traffic increases to 10 lakh users:
- server may become overloaded
- response time increases
- application may crash

To solve this:
- increase server power (vertical scaling)
OR
- add more servers (horizontal scaling)

Large companies like Netflix, Amazon, and Instagram mainly use horizontal scaling.

---

# How Do We Know Scaling Is Needed?

Engineers monitor system metrics.

## Common Signs

- High CPU usage
- Increased response time
- Memory exhaustion
- Database slow queries
- Too many concurrent users
- Traffic spikes

---

# When to Use Vertical Scaling

Use when:
- application is small
- startup stage
- low traffic
- simple architecture required

### Examples
- College projects
- Admin dashboards
- Internal tools

---

# When to Use Horizontal Scaling

Use when:
- millions of users are expected
- high availability is required
- system cannot afford downtime

### Examples
- Social media platforms
- OTT applications
- Banking systems
- E-commerce applications

---

# Important Point

Scalability is not only about adding servers.

It also includes:
- Load balancing
- Database scaling
- Caching
- CDN
- Queue systems
- Distributed architecture

---

# Interview Closing Line

Scalability helps systems support future growth efficiently while maintaining performance, stability, and availability.