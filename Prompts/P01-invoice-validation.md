# P01 · Invoice validation check (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 1 of 3 (Validation → Decision → Action)  
**Current version:** v1.2  
**Status:**  Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst responsible for validating vendor invoices.

Using ONLY the information provided, validate the invoice and identify any issues. 
Do not assume or add information that is not explicitly stated.

Validation rules:
1. Verify if the total amount equals the sum of all line items  
2. Check for missing components such as tax, shipping, or additional charges  
3. Flag any inconsistencies or unexplained differences  

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Invoice Date: 20 March 2026  

Line Items:
- Flour (50kg): $400  
- Sugar (20kg): $180  
- Butter (30kg): $360  

Total Amount: $1000  

Respond in JSON ONLY. Do not include any explanation outside the JSON.

{
  "invoice_number": "INV-7845",
  "is_valid": true/false,
  "calculated_total": number,
  "stated_total": number,
  "discrepancy": number,
  "issues": [
    "issue 1",
    "issue 2"
  ],
  "summary": "One-line explanation"
}

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice received  
- Actor: Automated system / finance team  
- Timing: Real-time validation  
- Next step:
  - Valid → Approval workflow  
  - Invalid → Dispute flow  

---

## ❗ Problem Being Solved

Manual invoice validation is slow and error-prone.  
This prompt automates validation with structured output for system integration.

---

## ⚡ Automation Potential

Level: Very High

- Fully machine-readable output  
- API/ERP integration ready  
- Minimal human intervention required  

---

## ⚠️ Risks and Limitations

- Edge cases (complex tax rules) → Human review required  
- Incorrect input data → Garbage in, garbage out  
- Over-reliance → Add audit checks  

---

## 🔄 Version History

### v1.0
- Basic prompt  
- Unstructured output  

### v1.1
- Added role + structure  
- Improved reasoning  

### v1.2 (Final)
- JSON output enforced  
- Validation rules added  
- Fully automatable  

---

## 📊 Final Output (v1.2)

{
"invoice_number": "INV-7845",
"is_valid": false,
"calculated_total": 940,
"stated_total": 1000,
"discrepancy": 60,
"issues": [
"Total amount does not match the sum of line items",
"Unexplained difference of $60",
"No tax, shipping, or additional charges specified"
],
"summary": "Invoice is invalid due to mismatch between calculated total ($940) and stated total ($1000) with no explanation."
}

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Structure | Low | High | Very High |
| Consistency | Medium | High | Very High |
| Automation readiness | Low | Medium | Very High |
| Machine-readable | ❌ | ❌ | ✅ |

---

## 🔗 Related Prompts

- Next: P05 — Approval recommendation  
- If invalid: P08 — Dispute email  
