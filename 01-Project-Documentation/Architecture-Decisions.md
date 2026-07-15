# Architecture Decisions

## Design Philosophy

The architecture was designed following Microsoft's Cloud Adoption Framework and Azure Well-Architected Framework principles.

---

## Key Design Decisions

### Resource Group

A dedicated Resource Group was created to logically organize all Azure resources.

Reason:
- Simplified management
- Easier access control
- Simplified resource lifecycle

---

### Virtual Network

A dedicated VNet was created.

Reason:

- Network isolation
- Future scalability
- Secure communication

---

### Separate Subnets

Two subnets were created.

- Web Subnet
- Database Subnet

Reason:

Separate workloads improve security and reduce lateral movement.

---

### Network Security Groups

Dedicated NSGs were associated with subnets.

Reason:

Traffic filtering

Least privilege access

Controlled inbound and outbound communication

---

### Azure Key Vault

Secrets were stored securely.

Reason:

Avoid storing passwords inside applications or virtual machines.

---

### Azure Monitor

Monitoring enabled.

Reason:

Centralized health monitoring

Performance tracking

Operational visibility

---

### Recovery Services Vault

Configured for Azure Backup.

Reason:

Business continuity

Disaster recovery

Point-in-time restoration

---

### Azure Policy

Policies assigned.

Reason:

Enforce organizational standards.

---

### Resource Locks

Delete locks configured.

Reason:

Prevent accidental deletion of production resources.

---

## Architecture Summary

The final architecture provides:

- Security
- Governance
- Monitoring
- Backup
- Cost Optimization
