# P03 · Vendor classification (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 0.5 of 3 (Extraction → Classification → Validation → Decision)  
**Current version:** v1.2  
**Status:** ✅ Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst responsible for categorizing vendors for financial reporting.

Using ONLY the vendor name provided, classify the vendor into EXACTLY ONE of the categories below.
Do not assume information beyond what is implied by the name.

Categories:
- Raw Materials Supplier  
- Logistics & Delivery  
- Equipment & Maintenance  
- Professional Services  
- Utilities  
- Other  

Vendor Name: FreshFarm Supplies  

Rules:
1. Choose ONLY one category from the list  
2. If unsure, select "Other"  
3. Provide a short reasoning based ONLY on the vendor name  
4. Assign a confidence score between 0 and 1  

Respond in JSON ONLY. Do not include any explanation outside the JSON.

{
  "vendor_name": "",
  "category": "",
  "confidence": 0.0,
  "reason": ""
}

---

## 🏢 Intended Workflow or Task

- Trigger: Vendor identified during invoice processing  
- Actor: Automated system / finance team  
- Timing: Real-time classification  
- Next step: Used in validation (P01) and reporting  

Flow:
P02 → P03 → P01 → P05  

---

## ❗ Problem Being Solved

Unstructured vendor data leads to:
- Poor spend visibility  
- Inconsistent categorization  
- Weak analytics and fraud detection  

v1.2 enables consistent, structured categorization.

---

## ⚡ Automation Potential

**Level: Very High**

- Machine-readable output  
- API-ready  
- Scalable across large invoice volumes  
- Minimal human intervention  

---

## ⚠️ Risks and Limitations

- Ambiguous vendor names → misclassification risk  
- Confidence score subjective  
- Requires periodic audit  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0
- No constraints  
- Inconsistent output  

### v1.1
- Fixed categories  
- Improved consistency  

### v1.2 (Final)
- JSON output  
- Confidence score added  
- Fully automatable  

---

## 📊 Final Output (v1.2)

{
"vendor_name": "FreshFarm Supplies",
"category": "Raw Materials Supplier",
"confidence": 0.9,
"reason": "The name suggests supply of farm-based goods, which are typically used as raw materials."
}

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Consistency | Medium | High | Very High |
| Control | Low | High | Very High |
| Machine-readable | ❌ | ❌ | ✅ |
| Automation readiness | Low | Medium | Very High |

---

## 🔗 Related Prompts

- Previous: P02 — Invoice extraction  
- Next: P01 — Invoice validation  

