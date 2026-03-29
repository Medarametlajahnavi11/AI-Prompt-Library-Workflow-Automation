# P07 · Dispute email generator (v1.2)

**Section:** Finance Operations — Accounts Payable  
**Workflow step:** Step 5 (Issue Resolution / Vendor Communication)  
**Current version:** v1.2  
**Status:** ✅ Tested and production-ready  
**Last updated:** March 2026  

---

## 📌 Prompt Text (v1.2 — final)

You are a finance analyst responsible for communicating invoice issues to vendors.

Using ONLY the information provided, draft a professional dispute email.
Do not add or assume any information beyond what is given.

Details:
Vendor: FreshFarm Supplies  
Invoice Number: INV-7845  
Issue: Total amount does not match calculated value ($1000 vs $940)

Rules:
1. Follow the exact format below  
2. Keep the email concise (maximum 120 words)  
3. Maintain a professional and polite tone  
4. Do not include any extra text outside the format  

Output format:

Subject: Invoice Discrepancy – [Invoice Number]

Email Body:
Dear [Vendor] Team,

We have identified a discrepancy in Invoice [Invoice Number]. The stated total is $1000, while the calculated total is $940.

Kindly review this issue and provide clarification or a revised invoice.

Thank you for your prompt attention.

Best regards,  
[Your Name]  
[Your Position]  
[Company Name]

---

## 🏢 Intended Workflow or Task

- Trigger: Invoice rejected (P05) or flagged (P06)  
- Actor: Automated system / finance team  
- Timing: Immediately after issue detection  
- Next step: Vendor responds with clarification or correction  

Flow:
P02 → P03 → P04 → P01 → P05 → P06 → [P07 RUNS]

---

## ❗ Problem Being Solved

Manual email drafting:
- Time-consuming  
- Inconsistent tone  
- Risk of missing key details  

v1.2 standardizes communication and ensures consistency.

---

## ⚡ Automation Potential

**Level: Very High**

- Fully standardized output  
- Reusable template  
- Easily integrated into CRM/email systems  
- Minimal human intervention  

---

## ⚠️ Risks and Limitations

- Placeholder fields must be populated correctly  
- Limited flexibility for complex disputes  
- Requires oversight for sensitive cases  

**Overall risk: LOW**

---

## 🔄 Version History

### v1.0
- Basic email generation  
- Unstructured  

### v1.1
- Structured email format  
- Improved tone  

### v1.2 (Final)
- Strict template enforced  
- Length constraint added  
- Fully production-ready  

---

## 📊 Final Output (v1.2)

Subject: Invoice Discrepancy – INV-7845  

Email Body:  
Dear FreshFarm Supplies Team,  

We have identified a discrepancy in Invoice INV-7845. The stated total is $1000, while the calculated total is $940.  

Kindly review this issue and provide clarification or a revised invoice.  

Thank you for your prompt attention.  

Best regards,  
[Your Name]  
[Your Position]  
[Company Name]  

---

## 📊 Improvement Summary

| Criteria | v1.0 | v1.1 | v1.2 |
|----------|------|------|------|
| Structure | Low | High | Very High |
| Consistency | Medium | High | Very High |
| Template control | Low | Medium | High |
| Automation readiness | Low | Medium | Very High |

---

## 🔗 Related Prompts

- Previous: P06 — Fraud detection  
- Next: P08 — Escalation summary  

