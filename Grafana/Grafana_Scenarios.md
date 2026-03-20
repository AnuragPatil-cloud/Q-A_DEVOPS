# 📊 Grafana Scenario-Based DevOps Interview Questions

This section contains **real-world Grafana troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Dashboard Not Showing Data

### Problem
Grafana dashboard panels show **No Data**.

### Possible Causes

- data source not configured
- incorrect query
- time range issue

### Solution

Check:

- data source connection
- query syntax
- dashboard time range

---

# Scenario 2: Prometheus Not Connected to Grafana

### Problem
Grafana cannot fetch metrics from Prometheus.

### Possible Causes

- wrong Prometheus URL
- network connectivity issue
- Prometheus not running

### Solution

Verify data source configuration:

```
Grafana → Data Sources → Prometheus
```

Check Prometheus status and connectivity.

---

# Scenario 3: Alerts Not Triggering

### Problem
Alert rule defined but no alert is triggered.

### Possible Causes

- incorrect threshold
- wrong query
- evaluation interval issue

### Solution

Check alert configuration:

- condition
- threshold
- evaluation time

Test alert manually.

---

# Scenario 4: Incorrect Metrics Displayed

### Problem
Dashboard shows wrong or unexpected values.

### Cause

Incorrect query or aggregation.

### Solution

Verify query:

```
sum(rate(http_requests_total[5m]))
```

Check filters and labels.

---

# Scenario 5: Dashboard Loading Slowly

### Problem
Grafana dashboards take too long to load.

### Possible Causes

- heavy queries
- large data range
- inefficient data source

### Solution

- optimize queries
- reduce time range
- use caching if available

---

# Scenario 6: Logs Not Appearing in Grafana Loki

### Problem
Logs are missing in Grafana Loki.

### Possible Causes

- Loki not receiving logs
- log agent (Promtail) misconfigured

### Solution

Check:

- Loki service status
- Promtail configuration
- log ingestion pipeline

---

# Scenario 7: Need Dynamic Dashboard Filtering

### Problem
User wants to filter dashboards by server or environment.

### Solution

Use **variables**.

Example:

```
$instance
```

Add variable in dashboard settings.

---

# Scenario 8: Authentication Issues in Grafana

### Problem
Users cannot log in.

### Possible Causes

- incorrect credentials
- authentication misconfiguration

### Solution

Check authentication settings:

- LDAP
- OAuth
- local users

---

# Scenario 9: Multiple Teams Need Access Control

### Problem
Different teams need different dashboard access.

### Solution

Use:

- roles
- organizations
- permissions

---

# Scenario 10: Need Centralized Monitoring

### Problem
Monitor multiple environments in one place.

### Solution

Connect multiple data sources:

- Prometheus
- Loki
- databases

Create unified dashboards.

---

# 🎯 Why Grafana Scenarios Are Important for DevOps

DevOps engineers must troubleshoot:

- monitoring issues
- alert failures
- data source problems
- dashboard performance

Understanding these scenarios helps maintain **effective observability and monitoring systems**.
