# P08 · Escalation summary (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 6 (Escalation / Management Reporting)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst preparing an escalation summary for management review.

Summarize the invoice issue below in a clear and structured format.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Issue: Total mismatch ($1000 vs $940)  

Provide the summary in the following format:

Invoice Number:  
Vendor:  

Issue Summary:  
(Brief description of the problem)

Risk Level:  
(Low / Medium / High)

Business Impact:  
(Explain potential impact such as financial risk, delay, or compliance issue)

Recommended Action:  
(What should be done next)

Keep the summary concise, professional, and decision-focused.

---

## 🏢 Intended Workflow or Task

- Trigger: High-risk invoice detected (P05/P06)  
- Actor: Finance / management  
- Timing: Before escalation decision  
- Next step: Management review and action  

Flow:
P02 → P03 → P04 → P01 → P05 → P06 → P07 → [P08 RUNS]

---

## ❗ Problem Being Solved

Managers need clear, structured escalation summaries to:
- Quickly understand issues  
- Assess risk  
- Take action  

v1.1 improves clarity and decision-readiness.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: High  
- Data availability: High  
- Human judgment: Medium  
- Time saving: ~75%  

---

## ⚠️ Risks and Limitations

- Not machine-readable  
- Risk level subjective  
- Variation possible  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0 → v1.1 Improvements

- Added role (finance analyst)  
- Structured format  
- Added risk + impact + action  

---

### v1.1 Observations

- Clear structured output  
- Strong business context  
- Actionable recommendation  

**Remaining Issues:**
- Not JSON  
- Not fully standardized  

---

## 📊 Test Output (v1.1)

Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  

Issue Summary:  
Mismatch between stated and calculated totals ($1000 vs $940).  

Risk Level:  
High  

Business Impact:  
Potential financial discrepancy and overpayment risk.  

Recommended Action:  
Hold payment and request correction.  

---

## 🔗 Related Prompts

- Previous: P07 — Dispute email  
- Upstream: P06 — Fraud detection  

