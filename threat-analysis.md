# Threat Analysis Summary

This document summarizes the main threats identified in the threat modeling process for the **Online Banking System**, using the STRIDE framework. The analysis was performed using the Microsoft Threat Modeling Tool, focusing on identifying key risks and proposing mitigations.

---

# STRIDE Categories and Threat Summary

## Spoofing

### Threats Identified

* Attackers impersonating legitimate users to access accounts (via stolen credentials or phishing).
* Malicious actors impersonating the banking server or app to capture user data (man-in-the-middle attacks).

### Proposed Mitigations

* Enforce multi-factor authentication (MFA).
* Implement strong password policies and encourage periodic password updates.
* Use SSL/TLS certificates with proper certificate pinning to prevent fake server impersonation.

## Tampering

### Threats Identified

* Modification of transaction data during transmission.
* Unauthorized database changes or manipulation of stored records.

### Proposed Mitigations

* Use end-to-end encryption for all client-server communications.
* Apply input validation and cryptographic integrity checks (hashing).
* Implement strict access controls on APIs and databases.

## Repudiation

### Threats Identified

* Users denying they initiated a transaction or action.
* Employees denying system changes or administrative actions.

### Proposed Mitigations

* Use digital signatures or generate transaction receipts.
* Ensure non-repudiation by confirming critical actions with signed acknowledgments.

## Information Disclosure

### Threats Identified

* Exposure of sensitive data (e.g., account details, personal information) through unsecured channels, logs, or backups.
* Data leakage during transmission due to weak encryption.

### Proposed Mitigations

* Encrypt sensitive data both at rest and in transit.
* Apply least-privilege access controls to sensitive resources.
* Regularly audit and secure backup data.

## Denial of Service (DoS)

### Threats Identified

* Overloading the banking system with excessive requests (DDoS attacks).
* Resource exhaustion due to poorly optimized or vulnerable endpoints.

### Proposed Mitigations

* Apply rate limiting and throttling on APIs.
* Implement DDoS protection services and system redundancy.
* Set up proactive monitoring and automated alerting for system health.

## Elevation of Privilege

### Threats Identified

* Attackers exploiting software vulnerabilities to gain admin privileges.
* Insiders abusing elevated roles for unauthorized access.

### Proposed Mitigations

* Apply the principle of least privilege and enforce role-based access controls.
* Regularly patch and update all system components.
* Conduct periodic security reviews and privilege audits.

---

# Conclusion

The threat modeling process has helped identify critical security risks in the online banking system. By applying the outlined mitigations, the system can better protect against common attack vectors, safeguard customer data, and maintain trust and service availability.

For details, refer to the exported **threat-model.pdf** file linked in the repository.

## Tools Used

- **Microsoft Threat Modeling tool**.
- The model diagram was exported as `threat-model.pdf` and uploaded to the repository.