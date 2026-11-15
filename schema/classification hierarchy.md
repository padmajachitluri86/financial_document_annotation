# Financial Document Classification Hierarchy

## Introduction

This document defines the hierarchical classification system for financial documents.

Every document must be classified using three levels:
1. Primary Document Type
2. Document Subtype
3. Document Quality and Condition Tags

# Level 1: Primary Document Categories

The project contains eight primary document categories.

| No. | Primary Category | Required Documents |
|---|---|---:|
| 1 | Bank Statements | 30 |
| 2 | Commercial Invoices | 30 |
| 3 | Income Tax Returns | 25 |
| 4 | Loan Agreements | 25 |
| 5 | Insurance Policies | 20 |
| 6 | Regulatory Filings | 20 |
| 7 | Payment Receipts | 25 |
| 8 | Financial Statements | 25 |

Total documents: 200.

Each document must receive exactly one primary category.

# Level 2: Document Subtypes

## 1. Bank Statements
- Savings Account Statement
- Current Account Statement
- Credit Card Statement
- Fixed Deposit Statement
- Demat Account Statement

## 2. Commercial Invoices
- Tax Invoice
- Proforma Invoice
- Debit Note
- Credit Note
- Self-Invoice (Reverse Charge)

## 3. Income Tax Returns
- ITR-1 (Sahaj)
- ITR-2
- ITR-3
- ITR-4 (Sugam)
- ITR-5 (Firms)
- ITR-6 (Companies)
- ITR-7 (Trusts)

## 4. Loan Agreements
- Personal Loan
- Home Loan / Mortgage
- Vehicle Loan
- Business Loan
- Overdraft Facility
- Line of Credit

## 5. Insurance Policies
- Term Life
- Health / Mediclaim
- Motor (Comprehensive/TP)
- Property / Fire
- Professional Indemnity
- Marine Cargo

## 6. Regulatory Filings
- Annual Return (MCA)
- GST Return (GSTR-1/3B/9)
- TDS Return (26Q/27Q)
- SEBI Filing
- RBI Reporting

## 7. Payment Receipts
- Cash Receipt
- Online Payment Confirmation
- Cheque Receipt
- Demand Draft Receipt
- UPI Payment Confirmation

## 8. Financial Statements
- Balance Sheet
- Profit & Loss Statement
- Cash Flow Statement
- Notes to Accounts
- Director Report Extract

# Level 3: Document Quality and Condition Tags

Every document must receive appropriate quality tags. Multiple tags may apply.

| Quality Tag | Definition |
|---|---|
| CLEAN_DIGITAL | Natively digital document with clear text and formatting |
| OCR_HIGH_QUALITY | Scanned document with OCR confidence above 95% |
| OCR_DEGRADED | Scanned document with OCR confidence between 80% and 95%, with some character errors |
| OCR_NOISY | Scanned document with OCR confidence below 80%, with significant errors |
| MULTI_LANGUAGE | Document contains text in two or more languages |
| MULTI_CURRENCY | Document contains amounts in two or more currencies |
| HANDWRITTEN_ELEMENTS | Contains handwritten notes, signatures, or annotations |
| REDACTED | Contains intentionally obscured or redacted information |
| TEMPLATE_MISMATCH | Document format does not match standard templates |
| INCOMPLETE | Document is truncated, missing pages, or partially illegible |

# Classification Rules

1. Every document must have exactly one primary category.
2. Select the most suitable subtype under that category.
3. Assign all applicable quality tags.
4. Do not guess the document type if information is unclear.
5. Record unclear cases for review.
6. Maintain consistent classification across all 200 documents.

# Conclusion

This classification hierarchy ensures that financial documents are organized consistently by category, subtype, and document quality.
