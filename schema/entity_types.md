# Financial Document Annotation – Entity Types

## Introduction

This document defines the 22 mandatory entity types used in the Financial Document Classification and Entity Extraction project.

Annotators must identify these entities in financial documents and label them using the exact entity names listed below.

## 1. MONETARY_AMOUNT
**Definition:** Any numerical value representing money, including currency symbols or codes.

**Examples:** ₹50,000; $1,200; INR 25,000.

**Rules:**
- Capture the currency.
- Handle multiple currencies in one document.

## 2. DATE
**Definition:** Calendar dates in any format.

**Examples:** 15/03/2025; March 15, 2025.

**Rules:**
- Normalize dates to ISO 8601 (YYYY-MM-DD).
- Flag ambiguous dates.

## 3. ACCOUNT_NUMBER
**Definition:** Bank account, loan account, policy, or folio numbers.

**Examples:** 1234567890; LN20250045.

**Rules:**
- Mask personally identifiable information (PII) in outputs.
- Validate formats according to the institution.

## 4. PARTY_NAME
**Definition:** Names of individuals, companies, trusts, or government entities.

**Examples:** Ravi Kumar; ABC Private Limited.

**Rules:**
- Distinguish payer, payee, guarantor, and beneficiary.

## 5. REGULATORY_ID
**Definition:** Regulatory identifiers such as PAN, GSTIN, TIN, EIN, LEI, and ISIN.

**Examples:** PAN; GSTIN; LEI.

**Rules:**
- Validate checksums wherever applicable.

## 6. ADDRESS
**Definition:** Physical addresses including street, city, state, postal code, and country.

**Examples:** Street address; office address.

**Rules:**
- Extract address sub-components.
- Handle incomplete addresses.

## 7. INTEREST_RATE
**Definition:** Annual, monthly, or periodic interest rates.

**Examples:** 8.5% per annum; 1% monthly.

**Rules:**
- Distinguish APR, flat rate, and compounding rate.

## 8. DURATION
**Definition:** Time periods such as loan tenure, policy term, or notice period.

**Examples:** 12 months; 30 days; 5 years.

**Rules:**
- Normalize periods into standard units such as months or days.

## 9. PERCENTAGE
**Definition:** Non-interest percentages such as tax rates, discounts, and ownership percentages.

**Examples:** GST 18%; discount 10%.

**Rules:**
- Distinguish percentages from interest rates using context.

## 10. DOCUMENT_ID
**Definition:** Invoice numbers, filing references, case numbers, and policy IDs.

**Examples:** INV-2025-001; POL-12345.

**Rules:**
- Cross-reference IDs within and across documents.

## 11. CLAUSE_REFERENCE
**Definition:** References to legal sections, schedules, and annexures.

**Examples:** Section 3.2(a)(ii); Annexure A.

**Rules:**
- Preserve the complete hierarchical structure.

## 12. TRANSACTION_TYPE
**Definition:** Types of financial transactions.

**Examples:** Debit; Credit; Transfer; Refund; Reversal.

**Rules:**
- Standardize variations such as DR, Debit, and D as DEBIT.

## 13. INSTITUTION_NAME
**Definition:** Names of banks, insurance companies, regulatory bodies, and exchanges.

**Examples:** HDFC Bank; insurance company names.

**Rules:**
- Distinguish institutions from general parties.
- Use canonical institution names.

## 14. PRODUCT_NAME
**Definition:** Names of financial products.

**Examples:** Fixed Deposit; Term Insurance; Mutual Fund.

**Rules:**
- Map products to standardized product categories.

## 15. STATUS
**Definition:** Document or transaction status.

**Examples:** Active; Lapsed; Pending; Approved.

**Rules:**
- Record the date to which the status applies, where available.

## 16. CONTACT_INFO
**Definition:** Phone numbers, email addresses, fax numbers, and URLs.

**Examples:** Phone number; email address.

**Rules:**
- Follow PII handling requirements.
- Validate the format.

## 17. SIGNATURE_BLOCK
**Definition:** Signatory names, designations, and signing dates.

**Examples:** Authorized signatory; Director; signature date.

**Rules:**
- Link the signatory to the PARTY_NAME entity.
- Capture authority level.

## 18. TABLE_DATA
**Definition:** Structured tabular information in financial documents.

**Examples:** Loan repayment schedules; insurance coverage tables.

**Rules:**
- Preserve row and column relationships.
- Handle merged cells.

## 19. COMPUTATION
**Definition:** Calculated fields and their formulas.

**Examples:** Total = Subtotal + Tax.
Balance = Opening Balance + Credits - Debits.

**Rules:**
- Capture the calculation logic, not just the result.

## 20. FOOTNOTE_REF
**Definition:** References to footnotes, endnotes, or explanatory notes.

**Examples:** Footnote 1; Note (a).

**Rules:**
- Link footnote content to the text that references it.

## 21. CURRENCY_CODE
**Definition:** ISO 4217 currency codes or currency symbols.

**Examples:** INR; USD; EUR.

**Rules:**
- Normalize symbols to ISO currency codes.
- Handle ambiguous symbols such as $, which may represent USD, SGD, or AUD.

## 22. FISCAL_PERIOD
**Definition:** Financial year, quarter, or assessment year references.

**Examples:** FY 2024–25; Q1 2025; AY 2025–26.

**Rules:**
- Distinguish calendar years from financial years.

## Important Annotation Rules

1. Use the exact entity names defined in this document.
2. Do not guess missing or unclear information.
3. Preserve the original text.
4. Normalize values according to the project rules.
5. Protect personal and financial information.
6. Record ambiguous cases for review.

## Conclusion

These 22 entity types form the foundation of the financial document annotation schema. They help annotators consistently identify important financial information across different document categories.
