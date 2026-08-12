# Prompt 4 - Booking Data Check

## Intended Workflow or Task
Check booking completeness before staff confirm a reservation.

## Problem Being Solved
Incomplete booking records can reach the floor or kitchen without a valid contact number, exact date, party size or important guest requirements. This creates avoidable follow-up and service risk.

## Version 1
**Prompt:** Check this restaurant booking and tell me what is missing.

**Issue:** Required and optional fields were undefined, so the AI could apply its own judgement and return an inconsistent completeness result.

## Final Version - v1.1
### Prompt Text
You are a booking validation assistant for a medium-sized restaurant chain.

Check the booking record using only the information provided.

Required fields:
- Customer name
- Exact booking date
- Booking time
- Number of guests
- Contact information

Check these additional fields if provided:
- Dietary requirements
- Accessibility requirements
- Special occasion or seating request

Return exactly:
1. Validation status: READY FOR AVAILABILITY CHECK or REVIEW REQUIRED
2. Required fields present
3. Required fields missing
4. Additional information provided
5. Information requiring clarification
6. Staff action required

Mark READY FOR AVAILABILITY CHECK only when every required field is present. Do not guess, correct or create information. Do not confirm the booking.

## Example Input
Customer name: Alex
Booking date: 14 August 2026
Booking time: 7:30 pm
Number of guests: 8
Contact information: Not provided
Accessibility requirement: Wheelchair access for one guest

## ChatGPT Test Evidence
### Version 1 Output
The booking includes a customer name, date, time, party size and wheelchair access. A phone number, dietary requirements and seating preference may be needed before confirming it.

**Issues and Limitations - Version 1:**
- The output did not return a standard READY or REVIEW REQUIRED decision.
- Optional dietary and seating details were mixed with the genuinely missing required contact information.
- The prompt did not clearly prevent confirmation or correction of the record.

### Final Version v1.1 Output
1. **Validation status:** REVIEW REQUIRED
2. **Required fields present:** Customer name, exact booking date, booking time, number of guests
3. **Required fields missing:** Contact information
4. **Additional information provided:** Wheelchair access for one guest
5. **Information requiring clarification:** Confirm the type of accessible seating or access support required. Dietary requirements and special requests are not provided.
6. **Staff action required:** Obtain valid contact information, clarify the accessibility requirement and then check live table availability. Do not confirm the booking yet.

**Improvements - Final v1.1:**
- Defined five mandatory fields and separated additional guest information.
- Added a rule-based READY FOR AVAILABILITY CHECK or REVIEW REQUIRED result.
- Kept availability and final confirmation outside the AI decision.

### Comparison
Version 1 correctly noticed the missing contact details but mixed them with optional information and gave no standard status. Final v1.1 applied explicit completeness rules, returned REVIEW REQUIRED and explained the exact follow-up needed. The result is predictable enough for a pre-confirmation workflow.

## Test Result
The improved prompt consistently marked the record REVIEW REQUIRED because one mandatory field was missing.

## Automation Potential
**High for completeness checking.** Can flag incomplete booking records before staff check availability.

## Risks and Limitations
A field can be present but false or mistyped; the AI cannot validate phone numbers, date conflicts, accessibility suitability or restaurant capacity.

## Mitigation and Human Oversight
Use AI only to check completeness. Staff or booking-system validation must confirm accuracy, availability and guest requirements.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | Required and optional fields were undefined, so the AI could apply its own judgement and return an inconsistent completeness result. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Defined mandatory and additional fields, added rule-based validation status, separated clarification needs and prohibited confirmation. | The record was consistently marked REVIEW REQUIRED because contact information was missing, while the accessibility detail was preserved for follow-up. | Validation prompts require explicit business rules and cannot replace accuracy checks against the reservation system. |
