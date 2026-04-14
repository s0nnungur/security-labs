# Access Control Assessment – Authentication, Authorization, and Accounting

## Context

This document summarizes a simulated access control review focused on
authentication, authorization, and account lifecycle management within a
small organization.

The goal of the assessment was to identify weaknesses in identity and access controls that could lead to unauthorized actions on sensitive systems.

## Observed Issue

During log review of payroll-related activity, an administrative action was
recorded from an account associated with a former external contractor.

Key observations included:
- The account belonged to a contractor whose engagement had ended several years earlier.
- The account remained active and retained administrative privileges.
- The action originated from an external IP address associated with the former
  contractor.

This indicated a failure in account deprovisioning and privilege management.

## Risk Analysis

The presence of an active, high-privilege account tied to a former contractor
represents a serious security risk:

- Unauthorized access to sensitive financial systems
- Abuse of administrative privileges
- Difficulty detecting malicious activity if actions appear legitimate
- Increased insider threat risk, even after employment termination

Such issues are commonly exploited in real-world breaches due to poor identity lifecycle management.

## Recommended Controls

### 1. Account Deprovisioning Procedures
- Implement formal offboarding processes to disable or remove accounts when employees or contractors leave.
- Periodically audit inactive or legacy accounts.

**Benefit:**  
Reduces the risk of unauthorized access from former staff or contractors.

---

### 2. Principle of Least Privilege
- Restrict administrative privileges to roles that strictly require them.
- Limit payroll and financial system access to approved personnel only.

**Benefit:**  
Minimizes the potential impact of compromised or misused accounts.

---

### 3. Approval and Monitoring Controls
- Require secondary approval for sensitive actions (e.g., payroll or banking
  changes).
- Monitor and alert on privileged account activity, especially from unusual
  locations or devices.

**Benefit:**  
Improves detection of anomalous behavior and reduces time to response.

## Key Takeaways

- Identity and access management failures are a common root cause of breaches
- Account lifecycle management is as important as authentication strength
- Monitoring privileged actions is critical for early incident detection
