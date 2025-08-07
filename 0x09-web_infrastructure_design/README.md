# Web Infrastructure Design

This repository contains conceptual designs and explanations for four stages of building and improving a web infrastructure, from a basic single-server setup to a fully scaled and monitored architecture.

---

## **0. Simple Web Stack**

### **Overview**
A basic single-server setup where all components run on one machine.

## image link 
- [Simple Web Stack](https://imgur.com/a/R2yHXIp)

**Components:**
- **DNS**: Resolves domain name to IP.
- **Single Server**: Hosts web server, application, and database together.
- **Web Server (Nginx/Apache)**: Handles HTTP requests and serves static content.
- **Application Code**: Runs backend logic.
- **Database (MySQL/PostgreSQL)**: Stores and retrieves application data.

**Pros:**
- Easy to set up and maintain.
- Low cost.

**Cons:**
- Single point of failure.
- Limited scalability and performance.
  

---

## **1. Distributed Web Infrastructure**

### **Overview**
A more robust setup by introducing redundancy and traffic distribution.
## image link
- [Distributed Web Infrastructure](https://imgur.com/a/FZ0znOS)

**Components:**
- **Load Balancer**: Distributes incoming traffic across multiple web servers.
- **Multiple Web Servers**: Each runs both the web server and application code.
- **Database Setup**:
  - **Primary (Master)**: Handles writes.
  - **Replica (Slave)**: Handles reads and provides failover backup.

**Pros:**
- Higher availability.
- Handles more traffic.

**Cons:**
- Still has single points of failure in load balancer and primary database.
- More complex to maintain.

---

## **2. Secured & Monitored Web Infrastructure**

### **Overview**
Improves security and operational visibility by adding firewalls, SSL, and monitoring.

## image link
[Secured & Monitored Web Infrastructure](https://imgur.com/a/dQs4Pta)

**Added Components:**
- **Firewalls (Network & Application Level)**: Restrict unauthorized access.
- **SSL Certificates**: Encrypt user traffic (HTTPS).
- **Monitoring Tools**: Track server health, uptime, and performance.

**Benefits:**
- Protects against external attacks.
- Detects issues before they cause downtime.
- Increases user trust with encrypted connections.

**Issues with This Setup:**
1. **Single Points of Failure**: Load balancer and primary database still risk downtime.
2. **Security Gaps**: End-to-end encryption may be missing if SSL terminates at the load balancer.
3. **Database Limitations**: Write bottleneck and replication lag.
4. **Monitoring Blind Spots**: Agent failures and lack of synthetic monitoring.
5. **Scaling Challenges**: Database writes still limited to one node.
6. **Operational Risks**: No disaster recovery or auto-healing.

---

## **3. Scale-Up Web Infrastructure**

### **Overview**
Splits the architecture into dedicated layers and clusters load balancers to handle high traffic with resilience.

## image link
[Scale-Up Web Infrastructure](https://imgur.com/a/ogC2ik2)

**Architecture Flow:**
