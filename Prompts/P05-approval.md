# P05 · Approval recommendation (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 3 of 3 (Extraction → Validation → Decision)  
**Current version:** v1.2  
**Status:** ✅ Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst responsible for reviewing invoices and recommending approval decisions.

Using ONLY the information provided, determine whether the invoice should be Approved, Rejected, or sent for Review.
Do not assume or add information beyond what is given.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Total Amount: $1000  
Calculated Total: $940  

Decision rules:
1. Approve → If total matches calculated value and no issues are present  
2. Reject → If there is a clear discrepancy or missing critical information  
3. Review → If there is uncertainty or incomplete data  

Tasks:
1. Select EXACTLY ONE decision: Approve / Reject / Review  
2. Provide a short reason based only on the given data  
3. Assign a confidence score between 0 and 1  

Respond in JSON ONLY. Do not include any explanation outside the JSON.

{
  "invoice_number": "",
  "decision": "",
  "confidence": 0.0,
  "reason": ""
}

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice validated (P01 completed)  
- Actor: Automated system / finance team  
- Timing: Before payment approval  
- Next step:
  - Approve → Payment processing  
  - Reject → Vendor dispute (P08)  
  - Review → Manual investigation  

Flow:
P02 → P03 → P04 → P01 → [P05 RUNS] → Decision  

---

## ❗ Problem Being Solved

Approval decisions are:
- Time-consuming  
- Inconsistent  
- Risk-prone  

v1.2 enables automated, consistent, and explainable decisions.

---

## ⚡ Automation Potential

**Level: Very High**

- Fully machine-readable output  
- API/ERP integration ready  
- Scalable across large invoice volumes  
- Minimal human intervention  

---

## ⚠️ Risks and Limitations

- Edge cases may require manual override  
- Confidence score is subjective  
- Over-reliance risk → audit required  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0
- Basic decision  
- No rules  

### v1.1
- Added decision rules  
- Improved consistency  

### v1.2 (Final)
- JSON output  
- Confidence score  
- Fully automatable  

---

## 📊 Final Output (v1.2)

{
"invoice_number": "INV-7845",
"decision": "Reject",
"confidence": 0.98,
"reason": "The total amount ($1000) does not match the calculated total ($940), indicating a discrepancy."
}

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Consistency | Medium | High | Very High |
| Decision control | Low | High | Very High |
| Machine-readable | ❌ | ❌ | ✅ |
| Automation readiness | Low | Medium | Very High |

---

## 🔗 Related Prompts

- Previous: P01 — Invoice validation  
- Next: P08 — Dispute email  

