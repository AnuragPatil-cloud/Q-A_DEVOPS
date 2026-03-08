# 🌐 Nginx & Apache Interview Questions (DevOps)

This section contains commonly asked **Nginx and Apache interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is a Web Server?

A web server is a **software that serves web content (HTML, CSS, JavaScript, images) to users over HTTP or HTTPS.**

Examples of web servers:

- Nginx
- Apache
- IIS

---

# 2. What is Nginx?

Nginx is a **high-performance web server and reverse proxy server** used to serve web applications, handle load balancing, and manage traffic efficiently.

Key features:

- High performance
- Low memory usage
- Reverse proxy
- Load balancing

---

# 3. What is Apache?

Apache HTTP Server is an **open-source web server used to serve web pages and applications.**

It is one of the **most widely used web servers on the internet.**

---

# 4. Difference between Nginx and Apache

Apache

- Process-based architecture
- Good for dynamic content
- Uses modules
- Higher memory usage

Nginx

- Event-driven architecture
- Very high performance
- Handles many connections efficiently
- Lower memory usage

---

# 5. What is Reverse Proxy?

A reverse proxy sits between **clients and backend servers** and forwards client requests to backend servers.

Benefits:

- Load balancing
- Security
- Caching
- SSL termination

Example architecture:

```
Client → Nginx → Application Server
```

---

# 6. What is Load Balancing?

Load balancing distributes incoming traffic across multiple backend servers.

Benefits:

- High availability
- Scalability
- Fault tolerance

Example:

```
User Request → Load Balancer → Multiple Servers
```

---

# 7. What is SSL/TLS?

SSL/TLS encrypts communication between client and server to ensure secure data transfer.

Example:

```
https://example.com
```

---

# 8. What is Virtual Host in Apache?

Virtual hosts allow **multiple websites to run on a single server**.

Example configuration:

```
<VirtualHost *:80>
    ServerName example.com
    DocumentRoot /var/www/html
</VirtualHost>
```

---

# 9. What is Nginx Configuration File?

Main configuration file:

```
/etc/nginx/nginx.conf
```

Example server block:

```
server {
    listen 80;
    server_name example.com;

    location / {
        root /var/www/html;
        index index.html;
    }
}
```

---

# 10. Apache Configuration File

Main configuration file:

```
/etc/apache2/apache2.conf
```

Virtual host configuration:

```
/etc/apache2/sites-available/
```

---

# 11. Default Ports for Web Servers

HTTP:

```
80
```

HTTPS:

```
443
```

---

# 12. How do you start Nginx?

```
systemctl start nginx
```

---

# 13. How do you restart Nginx?

```
systemctl restart nginx
```

---

# 14. How do you start Apache?

```
systemctl start apache2
```

---

# 15. How do you restart Apache?

```
systemctl restart apache2
```

---

# 16. How do you check Nginx status?

```
systemctl status nginx
```

---

# 17. How do you check Apache status?

```
systemctl status apache2
```

---

# 18. What is Caching in Nginx?

Caching stores frequently accessed data to **improve performance and reduce backend load.**

---

# 19. Real DevOps Scenario

### Problem

Application server cannot handle high traffic.

### Solution

Use Nginx as a **reverse proxy and load balancer** to distribute traffic across multiple backend servers.

---

# 20. Why Nginx & Apache are Important for DevOps

DevOps engineers use web servers for:

- Hosting applications
- Reverse proxy
- Load balancing
- SSL termination
- Handling web traffic

Common integrations:

- Docker
- Kubernetes
- CI/CD pipelines
- Cloud platforms
