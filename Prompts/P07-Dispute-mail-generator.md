# P07 · Dispute email generator (v1.0)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 5 (Issue Resolution / Vendor Communication)  
**Current version:** v1.0  
**Status:** ✅ Tested  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.0 — initial)

Write an email to the vendor regarding an issue with the invoice.

Details:
Vendor: FreshFarm Supplies  
Invoice Number: INV-7845  
Issue: Total amount does not match calculated value ($1000 vs $940)

Write a professional email explaining the issue.

---

## 🏢 Intended Workflow or Task

- **Trigger:** Invoice flagged as invalid (P01) or rejected (P05)  
- **Actor:** Finance team / automated system  
- **Timing:** Immediately after issue detection  
- **Next step:** Await vendor response / correction  

Flow:
P02 → P03 → P04 → P01 → P05 → P06 → [P07 RUNS]

---

## ❗ Problem Being Solved

Manual email drafting:
- Takes time  
- Inconsistent tone  
- Risk of missing key details  

At scale, delays vendor communication and resolution.

---

## ⚡ Automation Potential

**Level: High**

- Repetitiveness: Very high  
- Data availability: High  
- Human judgment: Low  
- Time saving: ~80%  

---

## ⚠️ Risks and Limitations

- Tone may vary  
- Missing placeholders (name/company)  
- Not standardized format  
- Not integrated with systems  

**Overall risk: LOW–MEDIUM**

---

## 🔄 Version History

### v1.0 — Initial draft

**Output observed:**
- Professional tone  
- Clear explanation of discrepancy  
- Includes request for correction  

**Issues:**
- No fixed structure  
- Placeholders not controlled  
- No constraints on tone/length  
- Not standardized for automation  

**Lesson learned:**
- Need structured email format  
- Need tone constraints  
- Need reusable template  

---

## 📊 Test Output (v1.0)

Dear FreshFarm Supplies Team,

We identified a discrepancy in Invoice INV-7845 where total does not match calculated value ($1000 vs $940).

Please review and provide clarification.

Regards,  
[Your Name]

---

## 🔗 Related Prompts

- Previous: P06 — Fraud detection  
- Next: P08 — Escalation summary  

