# 🌐 AWS CloudFront Scenario-Based DevOps Interview Questions (Basic + Advanced)

This section contains **real-world CloudFront troubleshooting scenarios** with **in-depth explanations and solutions**.

---

# 🔰 BASIC SCENARIOS

---

# Scenario 1: Website Not Updating After Deployment

## Problem
New changes deployed but users still see old content.

## Explanation
CloudFront caches content at edge locations.

## Troubleshooting

- Check cache behavior
- Verify TTL settings

## Root Cause

- Cached old content

## Fix

Invalidate cache:

```
aws cloudfront create-invalidation --distribution-id <id> --paths "/*"
```

---

# Scenario 2: Website Slow Despite CloudFront

## Problem
High latency even with CDN.

## Root Causes

- Cache miss (content not cached)
- Incorrect origin configuration

## Fix

- Enable caching  
- Optimize TTL  
- Check origin performance  

---

# Scenario 3: Access Denied from S3 via CloudFront

## Problem
Getting 403 error.

## Root Causes

- S3 bucket not accessible
- Missing OAI permission

## Fix

- Configure OAI (Origin Access Identity)  
- Update bucket policy  

---

# Scenario 4: HTTPS Not Working

## Problem
SSL errors when accessing site.

## Root Causes

- SSL certificate not configured
- Domain mismatch

## Fix

- Use ACM certificate  
- Attach to CloudFront  

---

# Scenario 5: Domain Not Resolving via CloudFront

## Problem
Custom domain not working.

## Root Causes

- DNS not configured
- Route53 record missing

## Fix

- Add CNAME/Alias record  
- Point to CloudFront distribution  

---

# 🚀 ADVANCED PRODUCTION SCENARIOS

---

# Scenario 6: API Returning Old Data

## Problem
Backend updated but API still returns old response.

## Explanation
CloudFront caching API responses.

## Fix

- Disable caching for API  
OR  
- Use cache-control headers  

---

# Scenario 7: High CloudFront Cost

## Problem
Unexpected high billing.

## Root Causes

- Too many requests
- Large data transfer

## Fix

- Optimize caching  
- Use compression  
- Adjust price class  

---

# Scenario 8: CloudFront Not Routing to ALB

## Problem
Backend not reachable.

## Troubleshooting

- Check origin configuration  
- Verify ALB health  

## Fix

- Correct origin DNS  
- Ensure ALB is healthy  

---

# Scenario 9: Need Secure Access to Content

## Problem
Content should not be public.

## Solution

- Use Signed URLs / Cookies  

---

# Scenario 10: Users from Certain Country Cannot Access

## Problem
Region-specific access issue.

## Root Cause

- Geo restriction enabled

## Fix

- Update geo restriction settings  

---

# Scenario 11: Cache Invalidation Taking Too Long

## Problem
Content update delay.

## Root Causes

- Large invalidation requests

## Fix

- Use versioned file names  
Example:
```
app_v2.js
```

---

# Scenario 12: 502/503 Errors from CloudFront

## Problem
Users get server errors.

## Root Causes

- Origin not responding
- ALB unhealthy

## Fix

- Check backend health  
- Verify origin settings  

---

# Scenario 13: Static Website Works Without CloudFront but Fails With It

## Problem
Direct S3 works but CDN fails.

## Root Causes

- Incorrect origin config
- Missing permissions

## Fix

- Verify S3 origin  
- Configure OAI  

---

# Scenario 14: Need Multi-Origin Setup

## Problem
Frontend + Backend routing needed.

## Solution

Use behaviors:

- `/api/*` → backend  
- `/*` → frontend  

---

# Scenario 15: Need Zero Downtime Deployment

## Problem
Deploy new version without affecting users.

## Solution

- Use versioned files  
- Gradual invalidation  

---

# 🎯 FINAL INTERVIEW ANSWER

If interviewer asks:

👉 “How do you troubleshoot CloudFront issues?”

Answer:

1. Check cache behavior  
2. Verify origin configuration  
3. Check DNS (Route53)  
4. Review logs  
5. Use invalidation if needed  

---

# 🚀 Why This Section is Important

This proves:

✅ CDN understanding  
✅ Performance optimization skills  
✅ Troubleshooting ability  
✅ Production-level DevOps knowledge  
