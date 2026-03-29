# P02 · Invoice data extraction (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 0 of 3 (Extraction → Validation → Decision)  
**Current version:** v1.2  
**Status:** ✅ Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst responsible for extracting structured data from vendor invoices.

Using ONLY the information provided, extract all key details from the invoice.
Do not assume or infer any missing information.

Invoice text:
Invoice No: FF-9021
Vendor Name: FreshFarm Supplies
Date: 22 March 2026

Items:
Flour 50kg - $500
Eggs 200 units - $300
Milk 100L - $250

Total: $1050

Extraction rules:
1. Extract invoice number, vendor name, and invoice date exactly as given  
2. Extract each line item with:
   - item_name
   - quantity (include units)
   - price  
3. If any field is missing, return "null"  
4. Do not modify or calculate values  

Respond in JSON ONLY. Do not include any explanation outside the JSON.

{
  "invoice_number": "",
  "vendor_name": "",
  "invoice_date": "",
  "items": [
    {
      "item_name": "",
      "quantity": "",
      "price": ""
    }
  ],
  "total_amount": ""
}

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice received in raw/unstructured format  
- Actor: Automated system / finance team  
- Timing: Real-time processing  
- Next step: Output passed to P01 (validation)

Flow:
Raw Invoice → [P02 RUNS] → JSON Output → P01 Validation  

---

## ❗ Problem Being Solved

Invoices are often received in unstructured formats, making:
- Data extraction time-consuming (2–5 min/invoice)  
- Standardization difficult  
- Automation across systems inefficient  

v1.2 enables direct system integration using structured JSON output.

---

## ⚡ Automation Potential

**Level: Very High**

- Fully machine-readable output  
- API/ERP integration ready  
- Minimal human intervention required  
- Estimated time saving: ~90%  

---

## ⚠️ Risks and Limitations

- Incorrect OCR/input text → incorrect extraction  
- Missing fields → returned as null (needs handling)  
- Over-reliance → audit checks required  

**Overall risk rating: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0
- Basic extraction  
- Unstructured output  

### v1.1
- Added role + structured template  
- Improved consistency  

### v1.2 (Final)
- JSON output enforced  
- Strict extraction rules added  
- Fully automatable and API-ready  

---

## 📊 Final Output (v1.2)

{
"invoice_number": "FF-9021",
"vendor_name": "FreshFarm Supplies",
"invoice_date": "22 March 2026",
"items": [
{
"item_name": "Flour",
"quantity": "50kg",
"price": "$500"
},
{
"item_name": "Eggs",
"quantity": "200 units",
"price": "$300"
},
{
"item_name": "Milk",
"quantity": "100L",
"price": "$250"
}
],
"total_amount": "$1050"
}

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Structure | Low | High | Very High |
| Consistency | Medium | High | Very High |
| Machine-readable | ❌ | ❌ | ✅ |
| Automation readiness | Low | Medium | Very High |

---

## 🔗 Related Prompts

- **Next in chain:** P01 — Invoice validation  
- **Downstream:** P05 — Approval recommendation  

