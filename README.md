# RoastOps Distribution  
## Hybrid Cloud Modernization Initiative

---

## 1. Company Overview

RoastOps Distribution is a mid-sized coffee roasting and logistics company serving:

- Regional wholesale clients (cafés and grocery chains)
- Direct-to-consumer subscription customers
- Corporate bulk order accounts

The company operates a single primary warehouse and roasting facility. All operational systems are currently hosted on-premises at the warehouse location.

Over the past three years, the company has experienced steady growth, resulting in increased infrastructure strain and operational risk.

---

## 2. Current Technical Environment (On-Premises)

The warehouse location currently hosts:

- Warehouse Management System (WMS) application server
- On-premises relational database server
- Local file storage for invoices and shipping records
- Barcode scanners and label printers
- Firewall/router providing internet connectivity
- Limited remote administrative access

### Current State Characteristics

- All core warehouse operations depend on the on-premises data center.
- Backups are performed manually and stored locally.
- No off-site redundancy exists.
- Monitoring and logging capabilities are minimal.
- Hardware infrastructure is approaching end-of-life.

---

## 3. Business Challenges

### 3.1 Operational Risk

Warehouse fulfillment must continue even during internet outages. However, there is currently no structured disaster recovery plan.

### 3.2 Data Protection

Database and file backups are manual and stored on-site, exposing the company to data loss risk in the event of hardware failure or ransomware.

### 3.3 Scalability Constraints

On-premises infrastructure is difficult and expensive to scale. Growth in order volume is stressing existing systems.

### 3.4 Lack of Centralized Monitoring

There is no centralized monitoring solution for:

- Infrastructure health
- Database performance
- Network connectivity
- Security events

### 3.5 Analytics Limitations

Leadership requires improved reporting on:

- Inventory turnover
- Subscription growth trends
- Shipping performance
- Order volume forecasting

Current reporting processes are manual and slow.

---

## 4. Business Objectives

RoastOps leadership has approved a hybrid cloud initiative with the following objectives:

- Maintain reliable, low-latency warehouse operations
- Establish secure connectivity between on-premises infrastructure and AWS
- Implement off-site backups and disaster recovery capability
- Centralize logging and monitoring
- Move analytics workloads to the cloud
- Modernize infrastructure gradually without full migration

The company does not intend to fully migrate all systems to the cloud at this stage.

---

## 5. Project Scope Assumptions

The following assumptions guide this design:

- One physical warehouse location
- Limited internal IT staff
- Budget-conscious implementation
- VPN-based hybrid connectivity (no dedicated private circuit)
- Single AWS region deployment
- Multi-AZ architecture permitted
- Some systems may remain permanently on-premises

---

## 6. Architectural Direction (To Be Defined)

Before designing the final architecture, the following strategic decision must be made:

1. AWS will host analytics, backups, and monitoring only.
2. AWS will host a public-facing web application while warehouse systems remain on-premises.
3. AWS will host analytics and a partially migrated application tier.

The selected option will determine:

- Network topology
- Routing design
- Security boundaries
- Availability planning
- Cost considerat
