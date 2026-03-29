# P08 · Escalation summary (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 6 (Escalation / Management Reporting)  
**Current version:** v1.2  
**Status:** ✅ Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst preparing executive-level escalation summaries for management.

Using ONLY the information provided, generate a concise and structured escalation summary.
Do not add or assume any information beyond what is given.

Invoice details:
Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  
Issue: Total mismatch ($1000 vs $940)  

Rules:
1. Follow the exact format below  
2. Keep each section concise (maximum 1–2 lines)  
3. Maintain a professional and decision-focused tone  
4. Do not include any extra text outside the format  

Output format:

Invoice Number:  
Vendor:  

Issue Summary:  
(1–2 line summary)

Risk Level:  
(Low / Medium / High)

Business Impact:  
(1–2 line impact)

Recommended Action:  
(1 line action)

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

Managers need concise, structured summaries to quickly assess risks and take action.

v1.2 ensures:
- Standardized reporting  
- Faster decision-making  
- Clear accountability  

---

## ⚡ Automation Potential

**Level: Very High**

- Fully standardized output  
- Dashboard/report ready  
- Scalable across high volumes  
- Minimal human effort  

---

## ⚠️ Risks and Limitations

- Not JSON (human-readable focus)  
- Risk level subjective  
- Requires governance checks  

**Overall risk: LOW**

---

## 🔄 Version History

### v1.0
- Basic summary  
- Unstructured  

### v1.1
- Structured format  
- Added risk and action  

### v1.2 (Final)
- Strict template  
- Executive-ready  
- Fully standardized  

---

## 📊 Final Output (v1.2)

Invoice Number: INV-7845  
Vendor: FreshFarm Supplies  

Issue Summary:  
Mismatch between stated total ($1000) and calculated total ($940), resulting in a $60 discrepancy.  

Risk Level:  
High  

Business Impact:  
Risk of incorrect payment due to discrepancy in invoice total.  

Recommended Action:  
Hold payment and request clarification or corrected invoice from the vendor.  

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Structure | Low | High | Very High |
| Decision-readiness | Low | High | Very High |
| Standardization | Low | Medium | High |
| Automation readiness | Low | Medium | Very High |

---

## 🔗 Related Prompts

- Previous: P07 — Dispute email  
- Upstream: P06 — Fraud detection  

