# P06 · Fraud / anomaly detection (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 4 of workflow (Risk Check)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst responsible for detecting potential fraud or anomalies in invoices.

Review the invoice below and determine if it shows signs of suspicious activity.

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
1. Determine if the invoice is Suspicious or Not Suspicious  
2. Assign a risk level: Low / Medium / High  
3. Provide a short explanation based on the rules  

Ensure your decision is based only on the given data.
Keep the explanation concise and professional.

---

## 🏢 Intended Workflow or Task

- Trigger: After validation and approval step  
- Actor: Finance / risk system  
- Timing: Before payment release  
- Next step:
  - Low risk → proceed  
  - Medium/High → audit / review  

---

## ❗ Problem Being Solved

Fraud detection is inconsistent and reactive.

v1.1 introduces:
- Rule-based detection  
- Risk classification  
- Better decision support  

---

## ⚡ Automation Potential

**Level: High**

- Repetitive checks  
- Clear rules  
- Scalable  

---

## ⚠️ Risks and Limitations

- Not machine-readable  
- Risk level subjective  
- Needs audit layer  

---

## 🔄 Version History

### v1.0 → v1.1 Improvements
- Added role  
- Added fraud rules  
- Added risk level  

---

### v1.1 Observations

- Correctly flagged as suspicious  
- Risk level: High  
- Explanation aligned with rules  

**Remaining Issues:**
- Not JSON  
- Not automatable  

---

## 📊 Test Output

Suspicious: Yes  
Risk Level: High  

Explanation: Total mismatch causing anomaly.

---

## 🔗 Related Prompts

- Previous: P05 — Approval  
- Next: P10 — Audit reporting  

