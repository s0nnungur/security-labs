# Risk Assessment – Likelihood and Severity Scoring

## Context

This activity focuses on performing a risk assessment for a commercial bank by evaluating common threats to financial assets. The objective is to assess how likely each risk is to occur, estimate its potential impact, and calculate an overall risk score to help prioritize security efforts.

The assessment follows the risk evaluation process aligned with the NIST Cybersecurity Framework (CSF), emphasizing proactive identification and prioritization of risks.

---

## Operating Environment Analysis

The bank operates in a coastal area with low physical crime but faces strict financial regulations and handles large volumes of sensitive data. With 100 on-premise employees, 20 remote employees, and thousands of customer accounts, the attack surface includes phishing, credential misuse, misconfigurations, and environmental disruptions such as hurricanes.

Although physical threats are limited, cyber and operational risks remain significant due to frequent data handling and regulatory exposure.

---

## Risk Register

| Asset | Risk | Description | Likelihood (1–3) | Severity (1–3) | Priority (L × S) |
|------|------|-------------|------------------|---------------|-----------------|
| Funds | Business Email Compromise | An employee is tricked into sharing confidential information via phishing. | 3 | 3 | **9** |
| Funds | Compromised User Database | Customer data is poorly encrypted or improperly secured. | 2 | 3 | **6** |
| Funds | Financial Records Leak | Backups or databases are publicly accessible due to misconfiguration. | 2 | 3 | **6** |
| Funds | Theft | Physical assets are exposed due to unlocked or poorly secured facilities. | 1 | 2 | **2** |
| Funds | Supply Chain Disruption | Cash or service delivery delays caused by natural disasters. | 1 | 3 | **3** |

---

## Risk Prioritization

- **High Priority:** Business Email Compromise (Score: 9)  
  Represents the most immediate and likely threat with severe financial and regulatory impact.

- **Medium Priority:** Compromised user database and financial records leak (Score: 6)  
  These risks could result in regulatory violations, loss of customer trust, and financial penalties.

- **Lower Priority:** Supply chain disruption (Score: 3) and theft (Score: 2)  
  While impactful, these risks are less likely given the operating environment and existing controls.

---

## Reflection

This assessment demonstrates how likelihood and impact scoring can be used to objectively prioritize security risks. By focusing resources on high-priority threats such as phishing and data exposure, organizations can reduce the most damaging risks while maintaining resilience against lower-probability events.
