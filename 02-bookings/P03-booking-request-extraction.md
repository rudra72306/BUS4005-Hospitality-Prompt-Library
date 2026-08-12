# Prompt 3 - Booking Request Extraction

## Intended Workflow or Task
Convert a free-text booking request into structured booking fields.

## Problem Being Solved
Booking requests often arrive as free text. Staff can overlook the exact date, contact information, dietary needs or accessibility requirements when manually transferring the message into a reservation system.

## Version 1
**Prompt:** Summarise this restaurant booking request.

**Issue:** The output structure was not fixed, missing details were not consistently identified and the AI was not prevented from confirming the booking.

## Final Version - v1.1
### Prompt Text
You are a booking assistant for a medium-sized restaurant chain.

Extract and organise the booking information below using only the customer's message.

Use this exact structure:
1. Customer name
2. Requested date
3. Requested time
4. Number of guests
5. Contact information
6. Dietary requirements
7. Accessibility requirements
8. Other requests
9. Missing information
10. Recommended staff action

Do not guess missing details or confirm table availability.

If information is missing, write "Not provided - staff confirmation required."

End with: "Booking is not confirmed until availability is checked by restaurant staff."

## Example Input
My name is Alex. I need a table for eight people this Friday at 7:30 pm. One guest uses a wheelchair.

## ChatGPT Test Evidence
### Version 1 Output
Alex would like a table for eight people this Friday at 7:30 pm. One guest requires wheelchair access.

**Issues and Limitations - Version 1:**
- The main details were captured, but the relative date was not flagged for conversion to an exact date.
- Missing contact information and dietary requirements were not identified.
- The output did not warn that the booking was still unconfirmed.

### Final Version v1.1 Output
1. **Customer name:** Alex
2. **Requested date:** This Friday; exact calendar date not provided - staff confirmation required.
3. **Requested time:** 7:30 pm
4. **Number of guests:** Eight
5. **Contact information:** Not provided - staff confirmation required.
6. **Dietary requirements:** Not provided - staff confirmation required.
7. **Accessibility requirements:** Wheelchair access for one guest
8. **Other requests:** Not provided - staff confirmation required.
9. **Missing information:** Exact date, contact information, dietary requirements and other requests.
10. **Recommended staff action:** Confirm the missing information, check suitable accessible seating and check live availability.

Booking is not confirmed until availability is checked by restaurant staff.

**Improvements - Final v1.1:**
- Added 10 exact booking fields for consistent reservation intake.
- Made relative dates and missing details visible instead of allowing guesses.
- Added accessibility handling and an explicit unconfirmed-booking safeguard.

### Comparison
Version 1 was readable but incomplete for reservation processing. Final v1.1 separated every operational field, retained the wheelchair-access requirement, flagged “this Friday” as an unresolved exact date and requested staff confirmation of missing information. It is therefore safer for transfer into a booking system.

## Test Result
The final prompt created a complete booking checklist and clearly separated known details from information still requiring confirmation.

## Automation Potential
**High.** Can standardise booking intake and pre-fill a reservation record before staff validation.

## Risks and Limitations
Relative dates can be misunderstood; accessibility needs may require more detail; the AI cannot verify contact information, restaurant capacity or suitable table availability.

## Mitigation and Human Oversight
Convert relative dates to confirmed calendar dates, require staff to discuss accessibility and dietary needs respectfully, and check all details in the live reservation system.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | The output structure was not fixed, missing details were not consistently identified and the AI was not prevented from confirming the booking. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added exact booking fields, missing-data rules, accessibility and dietary fields, a staff action and an unconfirmed-booking notice. | The final output showed every supplied detail and clearly identified the exact date, contact and dietary information that still needed confirmation. | Extraction prompts should mirror the destination system and explicitly identify incomplete records before automation continues. |
