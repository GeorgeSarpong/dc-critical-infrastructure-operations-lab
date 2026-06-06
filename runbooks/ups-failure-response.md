# UPS Failure Response Runbook

**Document Type:** Incident Response Runbook
**Severity:** P1 — Critical
**Author:** George Amankwaa Sarpong
**Last Updated:** June 2026

---

## Purpose
This runbook provides step-by-step procedures for responding to UPS system failures in a data center environment ensuring minimal downtime and maximum protection of critical infrastructure.

---

## Pre-Requisites
- Access to monitoring dashboard (Prometheus/Grafana/DCIM)
- UPS management interface credentials
- On-call contact list
- Generator startup authorization

---

## Trigger Conditions
- UPS on battery alert fired
- UPS bypass mode activated
- Battery health below 20%
- UPS fault alarm on monitoring dashboard

---

## Response Procedure

### Phase 1 — Immediate Assessment (0–2 minutes)
1. Acknowledge alert on monitoring dashboard
2. Log incident ticket with timestamp
3. Check UPS management interface for fault code
4. Verify utility power status at main distribution panel
5. Check estimated battery runtime remaining
6. Notify on-call supervisor immediately

### Phase 2 — Stabilization (2–10 minutes)
1. Verify all critical loads still powered
2. Check PDU status across all racks
3. Monitor battery runtime countdown
4. If runtime below 15 minutes — initiate generator startup
5. Alert all stakeholders via defined communication plan
6. Begin documenting all actions with timestamps

### Phase 3 — Generator Transition (if required)
1. Confirm generator auto-start via ATS
2. Allow 30-second generator stabilization period
3. Verify automatic transfer switch completes load transfer
4. Confirm all critical systems operational post-transfer
5. Monitor generator fuel level — minimum 75% required
6. Contact fuel supplier if level below 50%

### Phase 4 — Resolution & Recovery
1. Contact UPS vendor for emergency support
2. Document fault codes and battery readings
3. Arrange emergency maintenance if hardware failure confirmed
4. Test utility power restoration before transferring back
5. Complete post-incident review within 24 hours

---

## Escalation Matrix

| Timeline | Action | Contact |
|---|---|---|
| 0 minutes | Acknowledge alert | On-call Engineer |
| 2 minutes | Assess and notify | On-call Supervisor |
| 5 minutes | Generator decision | Operations Manager |
| 15 minutes | Vendor contact | UPS Vendor Emergency Line |
| 30 minutes | Executive notification | Data Center Director |

---

## Post-Incident Actions
- Complete incident report within 24 hours
- Root cause analysis within 48 hours
- Review and update runbook if gaps identified
- Schedule preventive maintenance review
