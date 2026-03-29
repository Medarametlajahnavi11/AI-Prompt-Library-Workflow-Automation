# P01 · Invoice validation check (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 1 of 3 (Validation → Decision → Action)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst responsible for validating vendor invoices.

Review the invoice below and check for correctness.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Invoice Date: 20 March 2026  

Line Items:
- Flour (50kg): $400  
- Sugar (20kg): $180  
- Butter (30kg): $360  

Total Amount: $1000  

Tasks:
1. Verify if the total amount matches the sum of line items  
2. Identify any discrepancies or missing details (e.g., tax, additional charges)  
3. Clearly state whether the invoice is valid or invalid  
4. Provide a brief explanation of your findings  

Keep the response clear, structured, and professional.

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice received from vendor  
- Actor: Finance executive runs validation prompt  
- Timing: Immediately upon invoice receipt  
- Next step:  
  - Valid → Approval workflow (P05)  
  - Invalid → Dispute handling (P08)

Invoice received → [P01 RUNS] → Validation result  
→ Valid → Approval  
→ Invalid → Vendor correction  

---

## ❗ Problem Being Solved

Finance teams spend 3–7 minutes per invoice verifying:
- Totals  
- Missing charges  
- Data inconsistencies  

At scale (200+ invoices/day), this leads to:
- 10–23 hours/day effort  
- Payment delays  
- Increased financial risk  

---

## ⚡ Automation Potential

Level: High

- Repetitiveness: Very high  
- Data availability: High  
- Human judgment needed: Medium  
- Integration possibility: Partial (not machine-readable yet)  
- Estimated time saving: ~75%  

Human-in-the-loop role:  
Finance team reviews flagged discrepancies before action.

---

## ⚠️ Risks and Limitations

- Output still not machine-readable → Mitigation: JSON in v1.2  
- Variation in formatting → Mitigation: Strict output format  
- Missed edge cases → Mitigation: Add validation checklist  
- Over-reliance → Mitigation: Human review  

Overall risk rating: MEDIUM  

---

## 🔄 Version History

### v1.0 → v1.1 Improvements

- Added role (finance analyst)  
- Added structured task steps  
- Improved consistency and reasoning  

### v1.1 Observations

- Structured output  
- Accurate validation  
- Professional tone  
- Still not machine-readable  

Lesson: Need structured output (JSON) for automation.

---

## 📊 Comparison

- v1.0: Basic, inconsistent  
- v1.1: Structured, improved reasoning, still not automatable  

---

## 🔗 Related Prompts

- Next: P05 — Approval recommendation  
- If invalid: P08 — Dispute email  
- Upstream: P02 — Invoice data extraction  
