# Domain Model — Loan Application API

## LoanApplication
| Field | Suggested type | Notes |
|---|---|---|
| id | Long | Generated database identifier |
| applicantReference | String | Synthetic reference; do not store real identity data in this portfolio project |
| loanType | enum | PERSONAL, HOME, AUTO |
| requestedAmount | BigDecimal | Validate positive values and define precision/scale |
| tenureMonths | Integer | Validate a sensible configured range |
| status | enum | SUBMITTED, UNDER_REVIEW, APPROVED, REJECTED |
| createdAt | LocalDateTime or Instant | Set when created |
| updatedAt | LocalDateTime or Instant | Update when modified |

## Example status flow
~~~text
SUBMITTED -> UNDER_REVIEW
UNDER_REVIEW -> APPROVED
UNDER_REVIEW -> REJECTED
~~~

Decide and test whether any additional transitions are permitted. Do not allow arbitrary status changes just because the request contains a valid enum value.

## Validation and reliability
- Reject missing or blank applicant references.
- Reject non-positive amounts and invalid tenure.
- Use BigDecimal for monetary values.
- Return appropriate HTTP status codes and a consistent error response.
- Keep persistence operations that must succeed together within a well-defined transaction boundary.
- Do not log sensitive payloads.
- Use synthetic test data only.
