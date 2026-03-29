<<<<<<< HEAD:Prompts/P06-fraud-detection.md
# P06 · Fraud / anomaly detection (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 4 of workflow (Risk Check)  
**Current version:** v1.2  
**Status:** ✅ Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst responsible for detecting potential fraud or anomalies in invoices.

Using ONLY the information provided, assess whether the invoice shows signs of suspicious activity.
Do not assume or add any information beyond what is given.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Total Amount: $1000  
Calculated Total: $940  

Fraud detection rules:
1. Flag as suspicious if there is a mismatch between total and calculated values  
2. Flag if there are unexplained differences in amounts  
3. Flag if critical information is missing or inconsistent  

Tasks:
1. Determine if the invoice is suspicious (true/false)  
2. Assign a risk level: Low / Medium / High  
3. Assign a risk score between 0 and 1  
4. Provide a short reason based only on the given data  

Respond in JSON ONLY. Do not include any explanation outside the JSON.

{
  "invoice_number": "",
  "is_suspicious": true/false,
  "risk_level": "",
  "risk_score": 0.0,
  "reason": ""
}

---

## 🏢 Intended Workflow or Task

- Trigger: After validation and approval stage  
- Actor: Automated risk system / finance team  
- Timing: Before final payment  
- Next step:
  - Low risk → proceed  
  - Medium/High → audit / investigation  

Flow:
P02 → P03 → P04 → P01 → P05 → [P06 RUNS]  

---

## ❗ Problem Being Solved

Fraud and anomalies are often:
- Detected late  
- Inconsistently identified  
- Highly manual  

v1.2 enables proactive, structured fraud detection.

---

## ⚡ Automation Potential

**Level: Very High**

- Machine-readable output  
- Scalable  
- Integrates with audit systems  
- Minimal human effort  

---

## ⚠️ Risks and Limitations

- Risk score is heuristic  
- Complex fraud patterns may require advanced models  
- Requires audit governance  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0
- Basic suspicion check  

### v1.1
- Added rules + risk level  

### v1.2 (Final)
- JSON output  
- Risk scoring  
- Fully automatable  

---

## 📊 Final Output (v1.2)

{
"invoice_number": "INV-7845",
"is_suspicious": true,
"risk_level": "High",
"risk_score": 0.95,
"reason": "The total amount ($1000) does not match the calculated total ($940), creating an unexplained discrepancy."
}

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Logic control | Low | High | Very High |
| Risk insight | None | Medium | High |
| Machine-readable | ❌ | ❌ | ✅ |
| Automation readiness | Low | Medium | Very High |

---

## 🔗 Related Prompts

- Previous: P05 — Approval  
- Next: P07 — Dispute email  

=======
# P06 · Fraud / anomaly detection (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 4 of 3+ (Risk Check after Decision)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Check if the following invoice looks suspicious or not.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Total Amount: $1000  
Calculated Total: $940  

Provide:
- Whether it is suspicious or not  
- Reason for your answer

---

## 🏢 Intended Workflow or Task

- **Trigger:** After invoice validation or decision stage  
- **Actor:** Finance team / automated risk system  
- **Timing:** Before final approval or audit  
- **Next step:**  
  - Not suspicious → Continue process  
  - Suspicious → Flag for investigation  

Flow:
P02 → P03 → P04 → P01 → P05 → [P06 RUNS]  

---

## ❗ Problem Being Solved

Fraud detection is:
- Manual  
- Inconsistent  
- Reactive instead of proactive  

Missed anomalies can lead to:
- Financial loss  
- Compliance issues  
- Vendor fraud  

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: High  
- Data availability: High  
- Human judgment: Medium  
- Time saving: ~75%  

---

## ⚠️ Risks and Limitations

- No defined fraud rules  
- Subjective outputs  
- Not structured  
- Cannot integrate into systems  

**Overall risk: MEDIUM–HIGH**

---

## 🔄 Version History

### v1.0 — Initial draft

**Output observed:**
- Correctly identified discrepancy  
- Marked invoice as suspicious  
- Provided logical reasoning  

**Issues:**
- No standardized fraud criteria  
- No risk scoring  
- Not machine-readable  

**Lesson learned:**
- Need fraud detection rules  
- Need risk levels  
- Need structured output (JSON in v1.2)  

---

## 📊 Test Output (v1.0)

Suspicious: Yes  

Reason: Total mismatch creates unexplained discrepancy.

---

## 🔗 Related Prompts

- Previous: P05 — Approval decision  
- Downstream: P10 — Audit / reporting  

>>>>>>> 8775419450718289b8de78390b6f8f4e839ffc6d:Prompts/P06-Fraud-Detection.md
