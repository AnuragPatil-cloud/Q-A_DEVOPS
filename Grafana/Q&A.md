# 📊 Grafana Interview Questions & Answers (DevOps)

This section contains commonly asked **Grafana interview questions** for DevOps engineers.

---

# 1. What is Grafana?

Grafana is an **open-source visualization and monitoring tool used to create dashboards for metrics and logs from multiple data sources**.

---

# 2. What is Grafana used for?

Grafana is used for:

- data visualization
- monitoring infrastructure
- analyzing logs and metrics
- creating dashboards

---

# 3. What are Grafana dashboards?

Dashboards are **collections of panels used to visualize data in graphs, charts, and tables**.

They provide a centralized view of system performance.

---

# 4. What is a panel in Grafana?

A panel is a **single visualization unit within a dashboard**.

Examples:

- graph
- table
- gauge
- heatmap

---

# 5. What are data sources in Grafana?

Data sources are **external systems from which Grafana retrieves data**.

Examples:

- Prometheus
- Elasticsearch
- InfluxDB
- MySQL

---

# 6. What is Prometheus in Grafana?

Prometheus is a **monitoring tool commonly used as a data source for Grafana to collect metrics**.

---

# 7. What is a Grafana query?

A query is used to **fetch data from a data source and display it in a panel**.

Example:

```
rate(http_requests_total[5m])
```

---

# 8. What is alerting in Grafana?

Grafana alerting allows you to **trigger alerts when certain conditions are met in metrics**.

Example:

```
CPU usage > 80%
```

---

# 9. What is Grafana alert rule?

An alert rule defines:

- condition
- threshold
- evaluation time

When condition is met, an alert is triggered.

---

# 10. What are notification channels in Grafana?

Notification channels are used to **send alerts to users**.

Examples:

- email
- Slack
- webhook

---

# 11. What is Grafana Loki?

Loki is a **log aggregation system used with Grafana to collect and query logs**.

---

# 12. What is Grafana Tempo?

Tempo is used for **distributed tracing in microservices architectures**.

---

# 13. What is Grafana Explore?

Explore is a feature that allows **ad-hoc querying and troubleshooting of logs and metrics**.

---

# 14. What is a time range in Grafana?

Time range defines **the period of data displayed on the dashboard**.

Example:

```
Last 5 minutes
Last 1 hour
Last 24 hours
```

---

# 15. What is a variable in Grafana?

Variables allow **dynamic filtering in dashboards**.

Example:

```
Select server → filter dashboard data
```

---

# 16. What is Grafana provisioning?

Provisioning is used to **automatically configure dashboards, data sources, and alerts using configuration files**.

---

# 17. What is Grafana authentication?

Grafana supports authentication methods such as:

- basic auth
- LDAP
- OAuth
- SSO

---

# 18. What is the difference between Grafana and Kibana?

| Feature | Grafana | Kibana |
|---|---|---|
Use Case | Metrics visualization | Log analysis |
Data Sources | Multiple | Elasticsearch |

---

# 19. What are common Grafana use cases?

- infrastructure monitoring
- application monitoring
- log analysis
- performance tracking

---

# 20. Why is Grafana important for DevOps?

Grafana helps DevOps teams:

- visualize system performance
- monitor applications
- detect issues early
- improve observability
