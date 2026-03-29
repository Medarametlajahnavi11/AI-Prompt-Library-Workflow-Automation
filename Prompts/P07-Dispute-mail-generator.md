# P07 · Dispute email generator (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 5 (Issue Resolution / Vendor Communication)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst responsible for communicating invoice issues to vendors.

Draft a professional email to the vendor regarding the issue identified in the invoice.

Details:
Vendor: FreshFarm Supplies  
Invoice Number: INV-7845  
Issue: Total amount does not match calculated value ($1000 vs $940)

Write the email using the following structure:

Subject:  
(Clear subject line mentioning invoice issue)

Email Body:
- Greeting  
- Brief description of the issue  
- Specific details of the discrepancy  
- Request for clarification or corrected invoice  
- Polite closing statement  

Closing:
- Your Name  
- Your Position  
- Company Name  

Ensure the tone is professional, polite, and concise.
Do not include unnecessary details.

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice rejected (P05) or flagged (P06)  
- Actor: Finance team / automated system  
- Timing: Immediately after issue detection  
- Next step: Vendor responds with correction  

Flow:
P02 → P03 → P04 → P01 → P05 → P06 → [P07 RUNS]

---

## ❗ Problem Being Solved

Manual communication:
- Time-consuming  
- Inconsistent tone  
- Missing details  

v1.1 standardizes communication and improves clarity.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: Very high  
- Data availability: High  
- Human judgment: Low  
- Time saving: ~80%  

---

## ⚠️ Risks and Limitations

- Still not template-constrained fully  
- Placeholders need validation  
- Not system-integrated  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0 → v1.1 Improvements

- Added role (finance analyst)  
- Introduced structured email format  
- Improved tone consistency  

---

### v1.1 Observations

**Output quality:**
- Professional tone  
- Clear structure  
- Includes all required details  

**Remaining Issues:**
- No strict template enforcement  
- Slight variation possible  
- Not reusable across systems directly  

---

### Lesson Learned

Structured format improves clarity, but **strict templates are needed for full automation**.

---

## 📊 Test Output (v1.1)

Professional email with clear issue explanation and polite request for correction.

---

## 🔗 Related Prompts

- Previous: P06 — Fraud detection  
- Next: P08 — Escalation summary  

