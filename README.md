# Azure Cloud Security Detection Library

A hands-on KQL detection library and cloud security lab portfolio built while
transitioning from SOC operations into Azure cloud security engineering.

## Background

3+ years in SOC operations across incident response, detection engineering,
SIEM monitoring, MSSP/MDR environments, and Microsoft Sentinel. This repo
documents practical cloud security skills built week by week.

**Current focus:** Azure IAM · Entra ID · Microsoft Sentinel · Defender for Cloud

---

## Repo structure

```
azure-cloud-security-lab/
├── detections/
│   ├── identity/          # Entra ID, PIM, Conditional Access
│   ├── network/           # NSG, Azure Firewall (Week 2)
│   └── defender-for-cloud/ # CSPM alerts (Week 3)
├── posture/               # Secure Score findings (Week 3)
├── compliance/            # NIST gap analysis (Week 3)
├── infrastructure/        # Terraform IaC (Week 9)
└── playbooks/             # Sentinel SOAR (Week 4)
```

---

## Detection library

| Category | Rules | MITRE techniques |
|---|---|---|
| Identity & Entra ID | 4 rules | T1078, T1098, T1556, T1621 |

*Growing weekly. Network, container, and multi-cloud detections coming soon.*

---

## Tools and platforms

- Microsoft Sentinel — KQL, analytics rules, SOAR playbooks
- Microsoft Entra ID — IAM, Conditional Access, PIM, Identity Protection
- Defender for Cloud — CSPM, CWPP, regulatory compliance
- Azure — VNet, NSG, Azure Firewall, Private Endpoints
- Terraform, Checkov, tfsec *(in progress)*
- MITRE ATT&CK for Cloud

---

## Lab environment

- Azure free tier subscription
- Entra ID P2 trial (Conditional Access + PIM)
- Microsoft Sentinel connected to Log Analytics workspace
- Test users, groups, and security policies deployed for lab scenarios

---

*Updated weekly as new lab modules are completed.*
