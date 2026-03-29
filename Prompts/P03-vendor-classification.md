# P03 · Vendor classification (v1.1)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 0.5 of 3 (Extraction → Classification → Validation → Decision)  
**Current version:** v1.1  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.1 — improved)

You are a finance analyst responsible for categorizing vendors for financial reporting.

Classify the vendor below into EXACTLY ONE of the following categories:

- Raw Materials Supplier  
- Logistics & Delivery  
- Equipment & Maintenance  
- Professional Services  
- Utilities  
- Other  

Vendor Name: FreshFarm Supplies  

Tasks:
1. Select the most appropriate category from the list above  
2. Provide a short explanation for your choice  

Ensure the category is chosen ONLY from the given list.
Keep the explanation concise and professional.

---

## 🏢 Intended Workflow or Task

- Trigger: Vendor identified during invoice processing  
- Actor: Automated system / finance team  
- Timing: After P02 extraction  
- Next step: Used for reporting and validation (P01)

Flow:
P02 → [P03 RUNS] → Category → P01  

---

## ❗ Problem Being Solved

Lack of standardized vendor categorization leads to:
- Poor spend visibility  
- Inconsistent reporting  
- Weak fraud detection  

v1.1 improves consistency using a fixed category list.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: High  
- Data availability: High  
- Human judgment: Medium  
- Integration: Partial  
- Time saving: ~75%  

---

## ⚠️ Risks and Limitations

- Still not machine-readable  
- Misclassification for ambiguous vendors  
- No confidence score  

**Overall risk: MEDIUM**

---

## 🔄 Version History

### v1.0 → v1.1 Improvements

- Added role (finance analyst)  
- Introduced fixed category list  
- Improved consistency  

---

### v1.1 Observations

- Correct classification: Raw Materials Supplier  
- Consistent output format  
- Controlled categorization  

**Remaining Issues:**
- Not JSON  
- Cannot directly integrate  

---

## 📊 Comparison

| Criteria | v1.0 | v1.1 |
|----------|------|------|
| Consistency | Medium | High |
| Control | Low | High |
| Automation readiness | Low | Medium |

---

## 📊 Test Output

Category: Raw Materials Supplier  

Explanation: Vendor provides ingredients like flour, eggs, and milk used as raw materials.

---

## 🔗 Related Prompts

- Previous: P02 — Extraction  
- Next: P01 — Validation  

