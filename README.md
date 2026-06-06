# Data Center Critical Infrastructure Operations & Incident Management Lab

![Data Center Operations](https://img.shields.io/badge/Domain-Data%20Center%20Operations-blue)
![Critical Infrastructure](https://img.shields.io/badge/Focus-Critical%20Infrastructure-red)
![ITIL](https://img.shields.io/badge/Framework-ITIL%20v4-green)
![Schneider DCCA](https://img.shields.io/badge/Cert-Schneider%20DCCA-orange)

---

## 📋 Project Overview

This project simulates a full enterprise data center operations environment — documenting operational procedures, incident response playbooks, change management workflows, and capacity planning frameworks aligned with industry best practices.

Built to demonstrate operational readiness for:
- ✅ Data Center Operations Engineer roles
- ✅ Critical Infrastructure Engineer roles
- ✅ NOC Engineer roles
- ✅ Facilities Engineer roles

---

## 🏗️ Real World Foundation

This documentation is informed by hands-on management of a production rack environment including:

- **Dell PowerEdge R430 & R740** rack-mounted servers
- **D-Link managed switching** infrastructure
- **MTN fiber** connectivity and structured CAT6 cabling
- **UPS systems** for critical power protection
- ---

## 🔧 Infrastructure Components Covered

| Component | Details |
|---|---|
| UPS Systems | Monitoring, battery health, load management, failover |
| Generators | Startup procedures, testing, failover validation |
| PDUs | Power distribution, load balancing, circuit management |
| CRAC/CRAH Units | Temperature thresholds, airflow management, maintenance |
| Switchgear | Protection schemes, electrical safety procedures |
| Network Infrastructure | Switch management, connectivity monitoring |
| Environmental Monitoring | Temperature, humidity, water detection alerts |

---

## 📊 Monitoring & Alerting Framework

| Alert Type | Threshold | Severity | Response Time |
|---|---|---|---|
| UPS Battery Low | Below 20% | P1 — Critical | Immediate |
| UPS on Battery | Any | P1 — Critical | Immediate |
| Generator Startup | Auto-transfer | P1 — Critical | Immediate |
| Cooling Unit Failure | Any CRAC offline | P1 — Critical | Immediate |
| Temperature High | Above 80°F inlet | P2 — High | 15 minutes |
| Temperature Warning | Above 75°F inlet | P3 — Medium | 30 minutes |
| PDU Load High | Above 80% capacity | P2 — High | 15 minutes |
| Humidity Out of Range | Below 40% or above 60% | P3 — Medium | 30 minutes |

---

## 🚨 Incident Severity Classification

| Severity | Definition | Examples | Response Time |
|---|---|---|---|
| P1 — Critical | Complete service outage or imminent failure | Power outage, UPS on battery, cooling failure | Immediate |
| P2 — High | Significant degradation or single point of failure | PDU overload, high temperature, generator fault | 15 minutes |
| P3 — Medium | Partial impact or warning threshold breach | Humidity warning, battery health degraded | 30 minutes |
| P4 — Low | Informational or scheduled maintenance | Routine alerts, capacity warnings | Next business day |

---

## 📋 Key Runbooks

### UPS Failure Response
1. Verify UPS status on monitoring dashboard
2. Check bypass status and load transfer
3. Notify on-call engineer and management
4. Assess battery runtime remaining
5. Initiate generator startup if runtime below 10 minutes
6. Contact UPS vendor for emergency support
7. Document all actions in incident ticket

### Generator Failover Procedure
1. Confirm utility power loss via monitoring
2. Verify automatic transfer switch (ATS) status
3. Confirm generator startup — allow 30 second stabilization
4. Verify load transfer complete on monitoring dashboard
5. Check all critical systems still operational
6. Notify stakeholders of generator operation
7. Monitor fuel level — minimum 75% for extended outage
8. Document start time and fuel consumption

### Cooling Failure Response
1. Identify failed CRAC/CRAH unit on dashboard
2. Check inlet temperatures across all zones
3. Activate backup cooling unit if available
4. Implement emergency airflow procedures
5. Set temperature alert thresholds to P1 immediately
6. Contact cooling vendor for emergency support
7. Prepare for graceful shutdown if temperature exceeds 95°F
8. Document all actions and temperatures throughout

---

## 🔄 Change Management Framework

| Change Type | Approval Required | Lead Time | Examples |
|---|---|---|---|
| Standard | Pre-approved | None | Routine patching, monitoring updates |
| Normal | Change Advisory Board | 5 business days | Hardware upgrades, config changes |
| Emergency | Immediate manager | None | Critical security patches, outage recovery |

---

## 📐 Capacity Planning Metrics

| Metric | Target | Warning | Critical |
|---|---|---|---|
| Power Utilization | Below 70% | 70–80% | Above 80% |
| Cooling Capacity | Below 70% | 70–85% | Above 85% |
| Rack Space | Below 75% | 75–90% | Above 90% |
| PUE Target | Below 1.5 | 1.5–1.8 | Above 1.8 |

---

## 🛠️ Tools & Technologies

![Prometheus](https://img.shields.io/badge/Prometheus-Monitoring-orange)
![Grafana](https://img.shields.io/badge/Grafana-Dashboards-orange)
![Datadog](https://img.shields.io/badge/Datadog-Infrastructure%20Monitoring-purple)
![DCIM](https://img.shields.io/badge/DCIM-Infrastructure%20Management-blue)
![ITIL](https://img.shields.io/badge/ITIL%20v4-Service%20Management-green)
![Schneider](https://img.shields.io/badge/Schneider-DCCA-green)

---

## 📜 Standards & Frameworks Referenced

- **Uptime Institute** — Tier Standards for redundancy and availability
- **ASHRAE TC 9.9** — Thermal guidelines for data center environments
- **ITIL v4** — Incident, change, and problem management frameworks
- **NFPA 70E** — Electrical safety in the workplace
- **IEC 62040** — UPS systems standards
- **IEEE 3006** — Recommended practices for industrial power systems

---

## 👤 Author

**George Amankwaa Sarpong**
Data Center Operations & Critical Infrastructure Engineer
📍 Accra, Ghana.
🔗 [LinkedIn](https://linkedin.com/in/georgesarpong)
🌐 [GitHub Portfolio](https://github.com/GeorgeSarpong)

---

*This project is part of a broader portfolio demonstrating readiness for Data Center Operations, Critical Infrastructure, and NOC Engineer roles in the US market.*
- **Remote server management** coordinating with Koch engineering teams in Germany
- Supporting **nationwide branch operations** across Ghana

---

## 📁 Repository Structure
