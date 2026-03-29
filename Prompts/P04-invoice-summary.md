# P04 · Invoice summary (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 1.5 of 3 (Extraction → Classification → Summary → Validation → Decision)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst preparing a concise invoice summary for management review.

Summarize the invoice below in a clear and structured format.

Invoice details:
Invoice Number: FF-9021  
Vendor: FreshFarm Supplies  
Date: 22 March 2026  

Items:
- Flour (50kg): $500  
- Eggs (200 units): $300  
- Milk (100L): $250  

Total: $1050  

Provide the summary in the following format:

Invoice Number:  
Vendor:  
Date:  

Items Summary:  
(Briefly list key items and quantities)

Total Amount:  

Overall Summary:  
(1–2 sentences summarizing the invoice)

Keep the response professional, concise, and easy to read.

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice processed after extraction and classification  
- Actor: Finance team / managers  
- Timing: Before validation or approval  
- Next step: Quick understanding → P01 validation / P05 approval  

Flow:
P02 → P03 → [P04 RUNS] → Summary → P01  

---

## ❗ Problem Being Solved

Managers need a quick, readable overview of invoices.

Manual reading:
- Time-consuming  
- Inefficient at scale  
- Not standardized  

v1.1 improves readability and consistency.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: Very high  
- Data availability: High  
- Human judgment: Low  
- Integration: Partial  
- Time saving: ~75%  

---

## ⚠️ Risks and Limitations

- Still not machine-readable  
- Slight variation possible  
- No strict length control  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0 → v1.1 Improvements

- Added role (finance analyst)  
- Introduced structured format  
- Improved clarity and readability  

---

### v1.1 Observations

**Output quality:**
- Clean structured format  
- Clear item summary  
- Professional tone  

**Remaining Issues:**
- Not JSON  
- Not automatable for systems  

---

### Lesson Learned

Structured prompts significantly improve readability, but **standardization (JSON) is needed for automation**.

---

## 📊 Test Output (v1.1)

Invoice Number: FF-9021  
Vendor: FreshFarm Supplies  
Date: 22 March 2026  

Items Summary:  
Flour (50kg), Eggs (200 units), Milk (100L)  

Total Amount: $1050  

Overall Summary:  
Purchase of essential food supplies totaling $1050.

---

## 🔗 Related Prompts

- Previous: P03 — Vendor classification  
- Next: P01 — Invoice validation  

