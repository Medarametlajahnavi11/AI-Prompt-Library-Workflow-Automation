# P02 · Invoice data extraction (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 0 of 3 (Extraction → Validation → Decision)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst responsible for extracting structured data from vendor invoices.

Extract the key details from the invoice below.

Invoice text:
Invoice No: FF-9021
Vendor Name: FreshFarm Supplies
Date: 22 March 2026

Items:
Flour 50kg - $500
Eggs 200 units - $300
Milk 100L - $250

Total: $1050

Provide the output in the following structured format:

Invoice Number:  
Vendor Name:  
Invoice Date:  

Items:
- Item Name | Quantity | Price  

Total Amount:  

Ensure all details are clearly extracted and formatted consistently.

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice received in raw format  
- Actor: Automated system / finance team  
- Timing: Real-time extraction  
- Next step: Pass structured data to P01 (validation)

Flow:
Raw Invoice → [P02 RUNS] → Structured Output → P01 Validation  

---

## ❗ Problem Being Solved

Invoices come in **unstructured formats**, making:
- Manual extraction time-consuming (2–5 minutes/invoice)  
- Standardization difficult  
- Downstream automation (validation, approval) inefficient  

v1.1 improves consistency for easier downstream use.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: Very high  
- Data availability: High  
- Human judgment needed: Low  
- Integration: Partial (still not machine-readable)  
- Estimated time saving: ~75%  

---

## ⚠️ Risks and Limitations

- Not machine-readable → Cannot directly integrate with systems  
- Minor format inconsistencies possible  
- Missing fields not explicitly flagged  

**Overall risk rating: MEDIUM**

---

## 🔄 Version History

### v1.0 → v1.1 Improvements

- Added role (finance analyst)  
- Enforced structured output format  
- Improved consistency and readability  

---

### v1.1 — Observed Output

**Output quality:**
- Clean structured format  
- Correct extraction of all fields  
- Consistent item formatting  

**Remaining Issues:**
- Not JSON / machine-readable  
- Slight formatting variation possible  
- Not API-ready  

---

### Lesson Learned

- Structured templates improve consistency significantly  
- However, **machine-readable format (JSON) is required for full automation**  

---

## 📊 A/B Comparison

| Criteria | v1.0 | v1.1 |
|----------|------|------|
| Structure | Low | High |
| Consistency | Medium | High |
| Readability | Medium | High |
| Automation readiness | Low | Medium |

---

## 📊 Test Output (v1.1)

Invoice Number: FF-9021  
Vendor Name: FreshFarm Supplies  
Invoice Date: 22 March 2026  

Items:
Flour | 50 kg | $500  
Eggs | 200 units | $300  
Milk | 100 L | $250  

Total Amount: $1050  

---

## 🔗 Related Prompts

- **Next in chain:** P01 — Invoice validation  
- **Downstream:** P05 — Approval recommendation  

