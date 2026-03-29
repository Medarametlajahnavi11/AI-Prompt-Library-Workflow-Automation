# P01 · Invoice validation check (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 1 of 3 (Validation → Decision → Action)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Check if the following invoice is correct and identify any issues.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Invoice Date: 20 March 2026  

Line Items:
- Flour (50kg): $400  
- Sugar (20kg): $180  
- Butter (30kg): $360  

Total Amount: $1000  

Provide:
- Whether the invoice is valid or not  
- Any issues found  
- A short explanation

---

## 🏢 Intended Workflow or Task

- **Trigger:** Invoice received from vendor (email/PDF/manual entry)  
- **Actor:** Finance executive runs validation prompt  
- **Timing:** Immediately upon invoice receipt  
- **Next step:**  
  - If valid → Sent to approval (P05)  
  - If invalid → Sent for correction (P08 dispute email)

Invoice received → [P01 RUNS] → Validation result  
→ Valid → Approval workflow  
→ Invalid → Vendor correction flow  

---

## ❗ Problem Being Solved

Manual invoice validation takes **3–7 minutes per invoice**, especially when:
- Totals need recalculation  
- Missing charges must be identified  
- Errors require back-and-forth with vendors  

At **200 invoices/day**, this leads to:
- **10–23 hours of manual effort daily**
- Increased risk of **incorrect payments**
- Delays in vendor settlements  

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: Very high  
- Data availability: Structured invoice data available  
- Human judgment needed: Medium  
- Integration possibility: Can integrate into ERP/AP systems  
- Estimated time saving: ~70–80%  

Human-in-the-loop role:  
Finance team reviews flagged discrepancies before taking action.

---

## ⚠️ Risks and Limitations

- Model misses hidden charges → Mitigation: Add validation rules  
- Inconsistent output format → Mitigation: Structured output in next version  
- Over-reliance → Mitigation: Mandatory human review  
- Hallucination risk → Mitigation: Add grounding constraints  

Overall risk rating: MEDIUM  

---

## 🔄 Version History

### v1.0 — Initial draft

- Correctly identified total mismatch ($940 vs $1000)  
- Highlighted missing tax/charges  
- Output not structured  
- No role/context  
- No constraints  

Lesson learned:
- Add role (finance analyst)  
- Add structured output  
- Add explicit validation rules  

---

## 📊 Test Output (v1.0)

- Invoice marked invalid  
- $60 mismatch identified  
- Missing charges flagged  

Conclusion: Works logically but not production-ready.
