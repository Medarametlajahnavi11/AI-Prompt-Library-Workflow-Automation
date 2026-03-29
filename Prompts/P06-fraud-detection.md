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

