# Threat Analysis Summary

This threat model for the online banking system was created using the STRIDE framework. It includes key system components like the user interface, API gateway, authentication server, and database.

## Identified Threats and Mitigations

### 1. **Spoofing**
- **Threat**: An attacker impersonates a user to gain unauthorized access.
- **Mitigation**: Enforce strong authentication using 2FA and implement login attempt throttling.

### 2. **Tampering**
- **Threat**: An attacker modifies transaction data in transit.
- **Mitigation**: Use end-to-end encryption (TLS 1.2+) and integrity checks with digital signatures.

### 3. **Repudiation**
- **Threat**: A user denies performing a transaction.
- **Mitigation**: Maintain tamper-proof transaction logs with audit trails.

### 4. **Information Disclosure**
- **Threat**: Exposure of sensitive account data.
- **Mitigation**: Encrypt sensitive data in transit and at rest. Apply strict access control policies.

### 5. **Denial of Service (DoS)**
- **Threat**: Overloading the system to make it unavailable to users.
- **Mitigation**: Use load balancers and implement rate limiting and IP blacklisting.

### 6. **Elevation of Privilege**
- **Threat**: A user gains unauthorized admin access.
- **Mitigation**: Apply role-based access control (RBAC) and regular privilege audits.

## Tools Used

- **Microsoft Threat Modeling tool**.
- The model diagram was exported as `threat-model.pdf` and uploaded to the repository.