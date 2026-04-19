# Security Audit Report – Botium Toys

## 📌 Audit Overview

### Scope
The scope of this audit includes the entire security program at Botium Toys. This covers:
- Employee devices and equipment
- Internal network infrastructure
- Systems, software, and services
- Data storage and management

### Goals
- Assess existing assets
- Evaluate current security controls
- Identify compliance gaps
- Recommend improvements to strengthen security posture

---

## 🏢 Company Assets

The IT department manages the following assets:

- On-premises office equipment
- Employee devices (laptops, desktops, smartphones, remote workstations)
- Peripheral devices (headsets, keyboards, docking stations, etc.)
- Surveillance systems (CCTV cameras)
- Retail products stored in warehouse and sold online
- Business systems (accounting, ecommerce, database, inventory, telecom)
- Internet access and internal network
- Data storage and retention systems
- Legacy systems requiring manual monitoring

---

## ⚠️ Risk Assessment Summary

- **Risk Score:** 8 / 10 (High)
- **Impact Level:** Medium (asset loss impact unknown)
- **Overall Risk:** High (due to lack of controls and compliance gaps)

### Key Risk Factors
- Poor asset management and lack of visibility
- Missing critical security controls
- Non-compliance with industry regulations (PCI-DSS, GDPR)

---

## 🔍 Detailed Findings

### 🔴 Critical Issues

- All employees have access to sensitive data, including customer PII and cardholder data
- No encryption is used to protect sensitive financial data
- No implementation of least privilege or separation of duties
- No intrusion detection system (IDS) in place
- No disaster recovery plan or data backups

---

### 🟡 Security Weaknesses

- Password policy exists but is weak and outdated
- No centralized password management system
- Legacy systems are inconsistently monitored
- Lack of asset classification and management

---

### 🟢 Existing Security Controls

- Firewall is properly configured and active
- Antivirus software is installed and monitored
- Data integrity and availability controls are implemented
- GDPR breach notification plan (72 hours) is in place
- Privacy policies are documented and enforced
- Physical security controls:
  - Locks
  - CCTV surveillance
  - Fire detection and prevention systems

---

## ⚖️ Compliance Status

### PCI-DSS (Payment Security)
❌ Not compliant
- No encryption of cardholder data
- Weak access control
- Insecure handling of payment data

---

### GDPR (EU Data Protection)
⚠️ Partially compliant
- Breach notification plan exists
- Privacy policies exist
- Data protection and classification are insufficient

---

### SOC Controls
⚠️ Partially implemented
- Data integrity and availability are supported
- Access control and confidentiality are weak

---

## ⚠️ Risks Identified

- High risk of data breaches due to lack of encryption
- Unauthorized access to sensitive customer data
- Regulatory fines (PCI-DSS and GDPR violations)
- Business disruption due to lack of backups and recovery plans

---

## ✅ Recommendations

To improve security posture, Botium Toys should:

- Implement encryption for sensitive and payment data
- Enforce strong password policies and introduce password management tools
- Apply least privilege and separation of duties
- Deploy an intrusion detection system (IDS)
- Establish regular data backups and disaster recovery planning
- Improve asset management and classification processes
- Strengthen compliance with PCI-DSS and GDPR
- Define structured monitoring procedures for legacy systems

---

## 📘 Conclusion

Botium Toys currently faces a high level of security risk due to missing and weak controls. While some foundational protections exist, critical gaps in data protection, access control, and compliance must be addressed.

---

## 📚 What I Learned

This project helped me understand how to:
- Perform a real-world security audit
- Identify risks and vulnerabilities
- Evaluate compliance requirements
- Recommend practical security improvements
