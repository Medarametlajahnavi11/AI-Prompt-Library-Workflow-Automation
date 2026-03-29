# P04 · Invoice summary (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 1.5 of 3 (Extraction → Classification → Summary → Validation → Decision)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Summarize the following invoice.

Invoice details:
Invoice Number: FF-9021  
Vendor: FreshFarm Supplies  
Date: 22 March 2026  

Items:
- Flour (50kg): $500  
- Eggs (200 units): $300  
- Milk (100L): $250  

Total: $1050  

Provide a short summary.

---

## 🏢 Intended Workflow or Task

- **Trigger:** Invoice processed after extraction and classification  
- **Actor:** Finance team / manager  
- **Timing:** Before validation or approval  
- **Next step:** Supports quick review → P01 validation or P05 approval  

Flow:
P02 → P03 → [P04 RUNS] → Summary → P01  

---

## ❗ Problem Being Solved

Finance managers often need a **quick overview** of invoices without reading full details.

Manual review:
- Time-consuming  
- Repetitive  
- Inefficient at scale  

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: Very high  
- Data availability: High  
- Human judgment: Low  
- Integration: Possible  
- Time saving: ~70%  

---

## ⚠️ Risks and Limitations

- Output too generic  
- Important details may be missed  
- No structure or standard format  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0 — Initial draft

**Output observed:**
- Correctly summarizes invoice  
- Includes vendor, date, items, and total  

**Issues:**
- No structure → varies across runs  
- Not standardized → hard for reporting  
- No constraints → could become too long or too short  

**Lesson learned:**
- Need structured summary format  
- Need role-based prompting  
- Need consistency controls  

---

## 📊 Test Output (v1.0)

Invoice FF-9021 from FreshFarm Supplies, dated 22 March 2026, includes flour, eggs, and milk with a total of $1050.

---

## 🔗 Related Prompts

- Previous: P03 — Vendor classification  
- Next: P01 — Invoice validation  
- Downstream: P05 — Approval  

