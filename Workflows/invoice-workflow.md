# 📂 01 — Invoice Processing Workflow

**Business function:** Finance — Accounts Payable  
**Trigger:** Invoice received from vendor (email / system upload)  
**Prompts in this section:** P02, P03, P04, P01, P05, P06, P07, P08  

---

## Section Purpose

This workflow automates the end-to-end invoice processing lifecycle — from data extraction to final escalation.

In finance teams, invoice handling is a high-volume, repetitive task involving manual validation, decision-making, fraud checks, and vendor communication. This prompt chain reduces processing time from 10–15 minutes per invoice to under 2 minutes, while improving accuracy, consistency, and auditability.

---

## Chain Diagram

```
Invoice received
        │
        ▼
   P02 · Invoice extraction        (Extract structured data)
        │
        ▼
   P03 · Vendor classification     (Categorize vendor)
        │
        ▼
   P04 · Invoice summary           (Manager-friendly summary)
        │
        ▼
   P01 · Invoice validation        (Check correctness)
        │
        ▼
   P05 · Approval decision         (Approve / Reject / Review)
        │
        ▼
   P06 · Fraud detection           (Risk analysis)
        │
        ▼
   P07 · Dispute email             (If issue found)
        │
        ▼
   P08 · Escalation summary        (Management reporting)
```

---

## Human-in-the-Loop Points

| Step | Human action required |
|------|-----------------------|
| P02 output | Optional review for extraction accuracy |
| P01 output | Finance analyst verifies validation result |
| P05 decision | Final approval authority reviews decision |
| P06 risk output | High-risk cases reviewed by audit team |
| P07 email | Sent after finance approval |
| P08 summary | Used by management for final escalation decisions |

---

## Prompts

| File | Prompt | Status |
|------|--------|--------|
| P02_invoice_extraction_v1_2.md | Invoice data extraction | ✅ Tested — v1.2 |
| P03_vendor_classification_v1_2.md | Vendor classification | ✅ Tested — v1.2 |
| P04_invoice_summary_v1_2.md | Invoice summary | ✅ Tested — v1.2 |
| P01_invoice_validation_v1_2.md | Invoice validation | ✅ Tested — v1.2 |
| P05_approval_v1_2.md | Approval recommendation | ✅ Tested — v1.2 |
| P06_fraud_detection_v1_2.md | Fraud detection | ✅ Tested — v1.2 |
| P07_dispute_email_v1_2.md | Dispute email generator | ✅ Tested — v1.2 |
| P08_escalation_v1_2.md | Escalation summary | ✅ Tested — v1.2 |

---

## Business Impact

- Processing time reduced by ~80–90%  
- Error rate significantly reduced (rule-based validation)  
- Improved fraud detection and audit readiness  
- Better visibility for management through structured outputs  
- Faster vendor communication and issue resolution  
