# 🌐 AWS CloudFront Interview Questions & Answers (DevOps)

This section contains **in-depth CloudFront Q&A with real DevOps usage and practical explanations**.

---

# 1. What is AWS CloudFront?

## Answer
AWS CloudFront is a **Content Delivery Network (CDN) service that delivers content with low latency using edge locations worldwide**.

## Real DevOps Usage
👉 Used to:
- serve static content (images, CSS, JS)
- improve website performance
- reduce load on backend servers

---

# 2. What is a CDN?

## Answer
CDN (Content Delivery Network) is a **network of distributed servers that deliver content closer to users**.

## Example
User in India → content served from Mumbai edge location

---

# 3. What is an Edge Location?

## Answer
Edge locations are **AWS data centers that cache content close to users**.

## DevOps Usage
👉 Reduces latency and improves speed

---

# 4. What is an Origin in CloudFront?

## Answer
Origin is the **source of content**, such as:

- S3 bucket
- EC2 instance
- Load Balancer

---

# 5. What is Distribution in CloudFront?

## Answer
A distribution is a **configuration that defines how content is delivered**.

Types:
- Web distribution (HTTP/HTTPS)
- RTMP (deprecated)

---

# 6. What is Caching in CloudFront?

## Answer
CloudFront caches content at edge locations to **reduce latency and improve performance**.

## DevOps Usage
👉 Reduces backend load and cost

---

# 7. What is TTL in CloudFront?

## Answer
TTL (Time To Live) defines **how long content is cached**.

---

# 8. What is Cache Invalidation?

## Answer
Invalidation removes cached content so users get updated data.

## Command:
```
aws cloudfront create-invalidation
```

## DevOps Usage
👉 Used after deployment to refresh content

---

# 9. What is Signed URL / Signed Cookie?

## Answer
Used to **restrict access to content**.

## DevOps Usage
👉 Used for:
- secure video streaming
- private content delivery

---

# 10. What is OAI (Origin Access Identity)?

## Answer
OAI allows CloudFront to **securely access S3 bucket**.

## DevOps Usage
👉 Prevents direct public access to S3

---

# 11. What is HTTPS in CloudFront?

## Answer
CloudFront supports HTTPS using SSL certificates.

## DevOps Usage
👉 Ensures secure data transfer

---

# 12. What is CloudFront with S3?

## Answer
CloudFront serves S3 content faster using caching.

---

# 13. What is CloudFront with ALB?

## Answer
CloudFront distributes traffic to ALB for dynamic applications.

---

# 14. What is Geo Restriction?

## Answer
Restricts content access based on user location.

## DevOps Usage
👉 Used for compliance or licensing

---

# 15. What is Lambda@Edge?

## Answer
Runs code at edge locations.

## DevOps Usage
👉 Used for:
- request modification
- authentication

---

# 16. What is CloudFront Logging?

## Answer
Logs user requests and responses.

## DevOps Usage
👉 Used for monitoring and analysis

---

# 17. What is Origin Failover?

## Answer
CloudFront switches to backup origin if primary fails.

---

# 18. What is Price Class?

## Answer
Controls which edge locations are used.

## DevOps Usage
👉 Cost optimization

---

# 19. What are common CloudFront use cases?

- static website hosting
- video streaming
- API acceleration
- global applications

---

# 20. Why is CloudFront important for DevOps?

CloudFront helps:

- improve performance  
- reduce latency  
- enhance security  
- optimize cost  

---

# 🎯 Interview Tip

If asked:

👉 “How do you use CloudFront in your project?”

Say:

- Used CloudFront with S3 to serve frontend  
- Used caching to improve performance  
- Used invalidation after deployment  
- Secured content using OAI  
- Integrated with ALB for backend  

---

# 🚀 Why This Section is Important

This shows:

✅ CDN understanding  
✅ Performance optimization knowledge  
✅ Real-world usage  
