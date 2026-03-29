# P03 · Vendor classification (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 0.5 of 3 (Extraction → Classification → Validation → Decision)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Classify the following vendor into a category.

Vendor Name: FreshFarm Supplies

Provide the category and a short explanation.

---

## 🏢 Intended Workflow or Task

- **Trigger:** Vendor identified during invoice processing  
- **Actor:** Automated system / finance team  
- **Timing:** After data extraction (P02)  
- **Next step:** Used for reporting, risk checks, and validation (P01)

Flow:
P02 (Extract) → [P03 RUNS] → Vendor Category → P01 Validation  

---

## ❗ Problem Being Solved

Finance teams lack standardized vendor categorization, leading to:
- Poor spend visibility  
- Difficulty in reporting  
- Inefficient fraud detection  

Manual classification takes time and is inconsistent.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: High  
- Data availability: Vendor name always available  
- Human judgment needed: Medium  
- Integration: Possible with structured output (future versions)  
- Estimated time saving: ~70%  

---

## ⚠️ Risks and Limitations

- No predefined categories → inconsistent outputs  
- Ambiguous vendor names may lead to incorrect classification  
- Output not machine-readable  

**Overall risk rating: MEDIUM**

---

## 🔄 Version History

### v1.0 — Initial draft

**Output observed:**
- Correct classification: Food & Agricultural Supplies  
- Logical explanation based on vendor name  

**Issues:**
- No standard category list → variation across runs  
- Not structured → cannot integrate into systems  
- Subjective reasoning  

**Lesson learned:**
- Need predefined category list  
- Need role-based prompting  
- Need structured output (JSON in v1.2)  

---

## 📊 Test Output (v1.0)

Category: Food & Agricultural Supplies  

Explanation: The vendor name suggests supply of agricultural and food products such as flour, eggs, and milk.

---

## 🔗 Related Prompts

- **Previous:** P02 — Invoice extraction  
- **Next:** P01 — Invoice validation  
- **Downstream:** P09 — Spend analysis  

