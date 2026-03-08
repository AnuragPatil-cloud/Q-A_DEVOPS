# 📊 Grafana Interview Questions & Answers (DevOps)

This section contains commonly asked **Grafana interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Grafana?

Grafana is an **open-source monitoring and visualization tool** used to create dashboards and graphs from monitoring data.

It helps visualize metrics collected from different monitoring systems.

---

# 2. What is Grafana mainly used for?

Grafana is used for:

- Monitoring infrastructure
- Visualizing metrics
- Creating dashboards
- Alerting
- Observability

---

# 3. What are Grafana Data Sources?

A data source is the **system from which Grafana retrieves monitoring data**.

Examples of data sources:

- Prometheus
- Elasticsearch
- InfluxDB
- MySQL
- AWS CloudWatch
- Loki

---

# 4. What is a Grafana Dashboard?

A dashboard is a **collection of panels used to visualize system metrics and data**.

Examples:

- CPU usage dashboard
- Kubernetes monitoring dashboard
- Application performance dashboard

---

# 5. What are Grafana Panels?

Panels are **individual visualizations inside a dashboard**.

Examples:

- Graph
- Table
- Gauge
- Bar chart
- Stat panel

---

# 6. What are Grafana Alerts?

Grafana alerts notify users when certain conditions are met.

Example:

- CPU usage > 80%
- Memory usage > 90%

Alerts can be sent via:

- Email
- Slack
- PagerDuty
- Webhooks

---

# 7. What is Grafana Loki?

Loki is a **log aggregation system designed to work with Grafana**.

It collects logs from applications and infrastructure.

---

# 8. What is Grafana Tempo?

Tempo is a **distributed tracing backend used with Grafana**.

It helps trace requests across microservices.

---

# 9. What is the default port for Grafana?

Grafana runs by default on:

```
3000
```

Example access:

```
http://server-ip:3000
```

---

# 10. What is Grafana Explore?

Explore is a feature used to **query and analyze data interactively**.

It helps troubleshoot issues quickly.

---

# 11. What are Grafana Variables?

Variables allow **dynamic dashboards** by changing values such as:

- Server name
- Namespace
- Environment

Example variable:

```
$server
```

---

# 12. How does Grafana integrate with Prometheus?

Prometheus collects metrics and stores them as time-series data.

Grafana connects to Prometheus as a **data source** and displays the metrics in dashboards.

Workflow:

Application → Prometheus → Grafana Dashboard

---

# 13. What are Grafana Plugins?

Plugins extend Grafana functionality.

Types:

- Panel plugins
- Data source plugins
- App plugins

Example plugins:

- Kubernetes plugin
- AWS plugin
- Zabbix plugin

---

# 14. Real DevOps Scenario

### Problem

Production server CPU usage is high.

### Solution

1. Check Grafana dashboard
2. Identify CPU spike
3. Investigate application logs
4. Scale infrastructure if needed

---

# 15. Benefits of Grafana

- Real-time monitoring
- Easy dashboard creation
- Supports multiple data sources
- Alerting capabilities
- Open-source

---

# 🚀 Why Grafana is Important for DevOps

Grafana helps DevOps teams:

- Monitor infrastructure
- Visualize metrics
- Detect system issues early
- Improve system reliability

Common integrations:

- Prometheus
- Kubernetes
- Docker
- AWS CloudWatch
- Elasticsearch
