# Prompt 6 - Complaint Response

## Intended Workflow or Task
Draft a customer response based on an approved restaurant action.

## Problem Being Solved
Staff spend time writing similar acknowledgements and may accidentally promise a refund, discount or outcome that has not been approved by a manager.

## Version 1
**Prompt:** Reply to this restaurant complaint.

**Issue:** The prompt contained no approved-action boundary and did not prevent compensation promises or admissions of responsibility.

## Final Version - v1.1
### Prompt Text
You are a customer care assistant for a medium-sized restaurant chain.

Draft a professional response using only the customer complaint and approved action provided.

The response must:
1. Acknowledge the customer's experience
2. Apologise for the inconvenience
3. Summarise the issue without assigning blame
4. Explain the approved next step
5. Ask for the booking or order number if it is not provided
6. End with a respectful closing

Keep the response under 150 words.

Do not promise a refund, discount, replacement, free item or compensation unless it is explicitly included in the approved action. Do not admit legal responsibility or promise a specific investigation outcome.

Add this heading: "Draft - staff review required"

## Example Input
Customer complaint: I waited one hour for my meal, and it arrived cold.
Approved action: The restaurant manager will review the matter after receiving the customer's booking or order number.

## ChatGPT Test Evidence
### Version 1 Output
We are very sorry about the long wait and cold meal. We will give you a full refund and a free meal on your next visit.

**Issues and Limitations - Version 1:**
- The response made refund and free-meal promises that were not approved.
- It did not request the booking or order number needed for review.
- There was no staff-review label or boundary between drafting and management authority.

### Final Version v1.1 Output
**Draft - staff review required**

Hello,

We are sorry that you waited one hour for your meal and that it arrived cold. We understand this would have been disappointing.

Our restaurant manager can review the matter once we receive your booking or order number. Please reply with that number so the relevant details can be checked. A staff member will then contact you about the next step.

Kind regards,  
Customer Care Team

**Improvements - Final v1.1:**
- Limited the response to the manager-approved next step.
- Requested the missing booking or order number required for review.
- Prohibited unapproved compensation, legal admissions and investigation outcomes.

### Comparison
Version 1 was apologetic but created unauthorised financial and service commitments. Final v1.1 acknowledged the same experience, requested the information required for review and stayed within the approved action. The final output is safer for customer-facing use because staff retain control over the remedy.

## Test Result
The final prompt produced a calm response without promising compensation or deciding the complaint outcome.

## Automation Potential
**High for drafting; human approval required before sending.** The AI can prepare consistent acknowledgements but cannot decide remedies.

## Risks and Limitations
An incomplete approved action can produce an unhelpful reply; the wrong tone may worsen the complaint; customer information may be sensitive; accidental auto-send could make an unapproved commitment.

## Mitigation and Human Oversight
Managers approve the action, staff verify facts and tone, customer data is handled in an approved system, and every response is reviewed before sending.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | The prompt contained no approved-action boundary and did not prevent compensation promises or admissions of responsibility. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added an approved-action input, required response elements, a word limit, compensation and legal restrictions, and a staff-review label. | The final output asked for the required identifier and removed the unauthorised refund and free-meal promises. | AI can draft customer communication, but business commitments and remedies must remain under authorised human control. |
