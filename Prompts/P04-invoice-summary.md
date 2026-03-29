# P04 · Invoice summary (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 1.5 of 3 (Extraction → Classification → Summary → Validation → Decision)  
**Current version:** v1.2  
**Status:** ✅ Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst preparing standardized invoice summaries for management reporting.

Using ONLY the information provided, generate a concise and structured invoice summary.
Do not add or assume any information not explicitly given.

Invoice details:
Invoice Number: FF-9021  
Vendor: FreshFarm Supplies  
Date: 22 March 2026  

Items:
- Flour (50kg): $500  
- Eggs (200 units): $300  
- Milk (100L): $250  

Total: $1050  

Rules:
1. Follow the exact format below  
2. Keep the overall summary to a maximum of 2 sentences  
3. Do not include any extra text outside the format  

Output format:

Invoice Number:  
Vendor:  
Date:  

Items Summary:  
(List all items with quantities in one line)

Total Amount:  

Overall Summary:  
(1–2 sentence professional summary)

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice processed after extraction and classification  
- Actor: Finance team / management  
- Timing: Before validation and approval  
- Next step: Supports decision-making → P01 validation / P05 approval  

Flow:
P02 → P03 → P04 → P01 → P05  

---

## ❗ Problem Being Solved

Managers need a consistent and quick summary of invoices for faster decision-making.

Manual review:
- Time-consuming  
- Inconsistent  
- Not scalable  

v1.2 standardizes summaries for reporting and decision support.

---

## ⚡ Automation Potential

**Level: Very High**

- Standardized output  
- Consistent format  
- Easily integrable into reporting systems  
- Minimal human effort  

---

## ⚠️ Risks and Limitations

- Still not fully machine-readable (not JSON)  
- Limited analytical depth  
- Depends on accuracy of input data  

**Overall risk: LOW**

---

## 🔄 Version History

### v1.0
- Basic summary  
- Unstructured  

### v1.1
- Structured format  
- Improved readability  

### v1.2 (Final)
- Strict format enforced  
- Length constraints added  
- Standardized output  

---

## 📊 Final Output (v1.2)

Invoice Number: FF-9021  
Vendor: FreshFarm Supplies  
Date: 22 March 2026  

Items Summary:  
Flour (50kg), Eggs (200 units), Milk (100L)  

Total Amount: $1050  

Overall Summary:  
The invoice records the purchase of flour, eggs, and milk from FreshFarm Supplies. The total amount billed for these items is $1050.  

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Structure | Low | High | Very High |
| Consistency | Medium | High | Very High |
| Standardization | Low | Medium | High |
| Automation readiness | Low | Medium | High |

---

## 🔗 Related Prompts

- Previous: P03 — Vendor classification  
- Next: P01 — Invoice validation  
- Downstream: P05 — Approval recommendation  

