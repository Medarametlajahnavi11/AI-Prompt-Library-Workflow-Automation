# P05 · Approval recommendation (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 3 of 3 (Extraction → Validation → Decision)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Based on the following invoice details, decide whether the invoice should be approved or not.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Total Amount: $1000  
Calculated Total: $940  

Provide:
- Decision (Approve / Reject)  
- Reason for your decision

---

## 🏢 Intended Workflow or Task

- **Trigger:** Invoice validated (P01 completed)  
- **Actor:** Finance team / automated system  
- **Timing:** Before payment approval  
- **Next step:**  
  - Approve → Payment processing  
  - Reject → Vendor dispute (P08)  

Flow:
P02 → P03 → P04 → P01 → [P05 RUNS] → Decision  

---

## ❗ Problem Being Solved

Finance teams manually decide invoice approvals, which leads to:
- Delays in processing  
- Inconsistent decision-making  
- Risk of approving incorrect invoices  

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: High  
- Data availability: High  
- Human judgment: Medium  
- Time saving: ~70%  

---

## ⚠️ Risks and Limitations

- No decision rules → inconsistent outputs  
- Not structured → cannot automate  
- May miss edge cases  

**Overall risk: MEDIUM**

---

## 🔄 Version History

### v1.0 — Initial draft

**Output observed:**
- Correct decision: Reject  
- Correct reasoning: mismatch identified  

**Issues:**
- No standard decision criteria  
- No structured output  
- No role context  

**Lesson learned:**
- Need decision rules  
- Need role-based prompting  
- Need structured output (JSON in v1.2)  

---

## 📊 Test Output (v1.0)

Decision: Reject  

Reason: Total mismatch of $60 with no explanation.

---

## 🔗 Related Prompts

- Previous: P01 — Invoice validation  
- Next: P08 — Dispute email  
