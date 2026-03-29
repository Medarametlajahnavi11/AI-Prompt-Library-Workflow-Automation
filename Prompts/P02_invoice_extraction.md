# P02 · Invoice data extraction (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 0 of 3 (Extraction → Validation → Decision)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Extract key details from the following invoice.

Invoice text:
Invoice No: FF-9021
Vendor Name: FreshFarm Supplies
Date: 22 March 2026

Items:
Flour 50kg - $500
Eggs 200 units - $300
Milk 100L - $250

Total: $1050

Provide the extracted information clearly.

---

## 🏢 Intended Workflow or Task

- **Trigger:** Invoice received in raw/unstructured format (text, email, PDF OCR)  
- **Actor:** Automated system or finance executive  
- **Timing:** Immediately upon invoice receipt  
- **Next step:** Output passed to P01 (Invoice Validation)

Flow:
Raw Invoice → [P02 RUNS] → Structured data → P01 Validation  

---

## ❗ Problem Being Solved

Invoices arrive in **unstructured formats**, making it difficult to:
- Extract key fields manually  
- Standardize data for validation  
- Feed into systems  

Manual extraction takes **2–5 minutes per invoice**, creating bottlenecks.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: Very high  
- Data availability: Raw text always available  
- Human judgment needed: Low  
- Integration: Possible after structuring (future versions)  
- Estimated time saving: ~70%  

---

## ⚠️ Risks and Limitations

- Output format inconsistent → Hard to automate  
- Missing fields not clearly flagged  
- Variability in wording across runs  
- Not machine-readable  

**Overall risk rating: MEDIUM**

---

## 🔄 Version History

### v1.0 — Initial draft

**Output observed:**
- Correctly extracted:
  - Invoice number  
  - Vendor name  
  - Date  
  - Items with quantities and prices  
  - Total  

**Issues:**
- Output is formatted for humans, not systems  
- No consistent schema  
- Emojis/formatting may vary  
- Not suitable for direct integration  

**Lesson learned:**
- Need structured format  
- Need role-based prompting  
- Need strict output schema (JSON in v1.2)  

---

## 📊 Test Output (v1.0)

Invoice Number: FF-9021  
Vendor Name: FreshFarm Supplies  
Invoice Date: 22 March 2026  

Items:
- Flour (50 kg) — $500  
- Eggs (200 units) — $300  
- Milk (100 L) — $250  

Total: $1050  

---

## 🔗 Related Prompts

- **Next in chain:** P01 — Invoice validation  
- **Downstream:** P05 — Approval decision  

