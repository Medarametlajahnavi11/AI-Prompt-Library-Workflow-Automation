# P05 · Approval recommendation (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 3 of 3 (Extraction → Validation → Decision)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst responsible for reviewing invoices and recommending approval decisions.

Based on the invoice details below, decide whether the invoice should be Approved, Rejected, or sent for Review.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Total Amount: $1000  
Calculated Total: $940  

Decision rules:
1. Approve → If total matches calculated value and no issues are present  
2. Reject → If there is a clear discrepancy or missing critical information  
3. Review → If there is uncertainty or partial information  

Tasks:
1. Choose one decision: Approve / Reject / Review  
2. Provide a short explanation for your decision  

Ensure the decision strictly follows the rules above.
Keep the explanation concise and professional.

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice validated (P01 completed)  
- Actor: Finance team / automated system  
- Timing: Before payment approval  
- Next step:
  - Approve → Payment processing  
  - Reject → Vendor dispute (P08)  
  - Review → Manual investigation  

Flow:
P02 → P03 → P04 → P01 → [P05 RUNS] → Decision  

---

## ❗ Problem Being Solved

Manual approval decisions:
- Are inconsistent  
- Delay processing  
- Increase financial risk  

v1.1 introduces standardized decision rules.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: High  
- Data availability: High  
- Human judgment: Medium  
- Integration: Partial  
- Time saving: ~75%  

---

## ⚠️ Risks and Limitations

- Not machine-readable  
- Edge cases may still require human review  
- Decision rules may need expansion  

**Overall risk: MEDIUM**

---

## 🔄 Version History

### v1.0 → v1.1 Improvements

- Added role (finance analyst)  
- Introduced decision rules  
- Improved consistency  

---

### v1.1 Observations

- Correct decision: Reject  
- Decision aligned with rules  
- Clear explanation  

**Remaining Issues:**
- Not JSON  
- Not automatable  

---

### Lesson Learned

Decision rules significantly improve reliability, but **structured output is required for full automation**.

---

## 📊 Comparison

| Criteria | v1.0 | v1.1 |
|----------|------|------|
| Consistency | Medium | High |
| Control | Low | High |
| Automation readiness | Low | Medium |

---

## 📊 Test Output

Decision: Reject  

Explanation: Total mismatch between stated and calculated values.

---

## 🔗 Related Prompts

- Previous: P01 — Invoice validation  
- Next: P08 — Dispute email  

