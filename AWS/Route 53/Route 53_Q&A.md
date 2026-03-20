# 🌍 AWS Route 53 Interview Questions & Answers (DevOps)

This section contains commonly asked **AWS Route 53 interview questions** for DevOps engineers.

---

# 1. What is AWS Route 53?

AWS Route 53 is a **scalable Domain Name System (DNS) web service used to route internet traffic to applications**.

It translates domain names into IP addresses.

---

# 2. Why is it called Route 53?

Route 53 gets its name from:

```
Port 53 → used for DNS services
```

---

# 3. What is DNS?

DNS (Domain Name System) is a **system that converts human-readable domain names into IP addresses**.

Example:

```
google.com → 142.250.183.14
```

---

# 4. What is a Hosted Zone in Route 53?

A hosted zone is a **container for DNS records of a domain**.

Types:

- Public Hosted Zone
- Private Hosted Zone

---

# 5. What is the difference between Public and Private Hosted Zone?

| Public Hosted Zone | Private Hosted Zone |
|---|---|
Accessible from internet | Accessible within VPC |
Used for public websites | Used for internal applications |

---

# 6. What are DNS Records?

DNS records define **how domain traffic is routed**.

Common types:

- A record
- CNAME
- MX
- TXT

---

# 7. What is an A Record?

An A record maps:

```
Domain → IPv4 address
```

Example:

```
example.com → 192.168.1.1
```

---

# 8. What is a CNAME Record?

CNAME maps:

```
Domain → Another domain
```

Example:

```
www.example.com → example.com
```

---

# 9. What is an Alias Record?

Alias record is similar to CNAME but used for AWS resources like:

- Load Balancer
- CloudFront
- S3

---

# 10. What is TTL in DNS?

TTL (Time To Live) defines **how long DNS records are cached by resolvers**.

---

# 11. What is Routing Policy in Route 53?

Routing policies determine **how traffic is routed to resources**.

Types include:

- Simple Routing
- Weighted Routing
- Latency-Based Routing
- Failover Routing
- Geolocation Routing

---

# 12. What is Weighted Routing?

Weighted routing distributes traffic **based on assigned weights**.

Example:

```
Server A → 70%
Server B → 30%
```

---

# 13. What is Latency-Based Routing?

Latency-based routing directs traffic to the **region with the lowest latency** for the user.

---

# 14. What is Failover Routing?

Failover routing provides **high availability by switching traffic to a backup resource if the primary fails**.

---

# 15. What is Health Check in Route 53?

Health checks monitor the **health of resources and route traffic only to healthy endpoints**.

---

# 16. What is Geolocation Routing?

Geolocation routing directs traffic based on **user location**.

Example:

```
India → India server
US → US server
```

---

# 17. What is DNS Propagation?

DNS propagation is the **time required for DNS changes to update globally**.

---

# 18. What are common use cases of Route 53?

- domain management
- traffic routing
- high availability
- disaster recovery
- global load balancing

---

# 19. What is Domain Registration in Route 53?

Route 53 allows users to **register domain names directly within AWS**.

---

# 20. Why is Route 53 important for DevOps?

Route 53 helps DevOps teams:

- manage DNS efficiently
- implement failover strategies
- improve application availability
- route traffic globally
