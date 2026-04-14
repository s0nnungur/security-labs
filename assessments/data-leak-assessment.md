# Data Risk Assessment – Least Privilege & Data Leak Analysis

## Context

This activity analyzes a data leak incident at an educational technology company. The organization develops an application that processes sensitive data from students, parents, instructors, and academic institutions. The incident involved confidential internal business documents being unintentionally shared with an external partner due to improper access controls.

The objective of this assessment is to evaluate how failures in applying the principle of least privilege contributed to the data leak and to propose control enhancements based on NIST SP 800-53 (AC-6).

---

## Incident Analysis (Issues)

The data leak occurred because access permissions were overly broad and not time-limited. A customer success representative was granted access to a folder containing confidential internal documents, and the folder was not unshared after the meeting. The representative mistakenly shared the entire folder with an external partner, resulting in unintended exposure.

---

## Review of Current Controls (NIST SP 800-53 – AC-6)

NIST SP 800-53 AC-6 emphasizes the principle of least privilege, requiring organizations to grant users only the minimum access necessary to perform their job functions. It also recommends periodic access reviews, privilege monitoring, and restrictions on the use of privileged accounts to reduce the risk of misuse or accidental exposure.

---

## Recommended Control Enhancements

1. **Time-bound and role-based access controls**  
   Access to sensitive folders should be limited to specific roles and automatically expire after business needs are met, such as after meetings or projects conclude.

2. **Restricted sharing and approval workflows**  
   Implement controls that prevent external sharing of sensitive folders unless explicitly approved by management or data owners.

---

## Justification

These enhancements reduce the risk of accidental data exposure by limiting access duration and enforcing stricter sharing controls. Applying least privilege more rigorously ensures that sensitive information is only accessible when necessary and prevents unauthorized or unintended distribution of confidential data.

---

## Reflection

This assessment demonstrates how misconfigured access controls and human error can lead to significant data privacy incidents. It highlights the importance of combining technical controls with clear access governance to protect sensitive organizational data.
