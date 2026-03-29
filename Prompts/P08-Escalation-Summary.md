# P08 · Escalation summary (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 6 (Escalation / Management Reporting)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Summarize the issue with the invoice for escalation.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Issue: Total mismatch ($1000 vs $940)  

Provide a short summary for management.

---

## 🏢 Intended Workflow or Task

- **Trigger:** High-risk or rejected invoice (P05/P06)  
- **Actor:** Finance team / automated system  
- **Timing:** Before escalation to management  
- **Next step:** Manager review and decision  

Flow:
P02 → P03 → P04 → P01 → P05 → P06 → P07 → [P08 RUNS]

---

## ❗ Problem Being Solved

Managers need quick, clear summaries of issues without reviewing full invoice details.

Manual escalation:
- Time-consuming  
- Inconsistent  
- Lacks clarity  

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: High  
- Data availability: High  
- Human judgment: Low  
- Time saving: ~70%  

---

## ⚠️ Risks and Limitations

- No structured format  
- Missing risk context  
- Not standardized  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0 — Initial draft

**Output observed:**
- Clearly identifies discrepancy  
- Concise summary  

**Issues:**
- No structure  
- No risk level  
- Not standardized  

**Lesson learned:**
- Need structured escalation format  
- Need risk and impact context  
- Need consistency  

---

## 📊 Test Output (v1.0)

Invoice INV-7845 shows a mismatch between stated and calculated totals ($1000 vs $940), indicating a discrepancy requiring escalation.

---

## 🔗 Related Prompts

- Previous: P07 — Dispute email  
- Upstream: P06 — Fraud detection  

