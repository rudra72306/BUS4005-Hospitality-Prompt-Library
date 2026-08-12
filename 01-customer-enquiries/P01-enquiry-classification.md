# Prompt 1 - Customer Enquiry Classification

## Intended Workflow or Task
First-stage customer enquiry triage.

## Problem Being Solved
Restaurant enquiries arrive through phone transcripts, email, social media and website forms. Staff must read each message before deciding who should handle it, which can slow response and create inconsistent routing.

## Version 1
**Prompt:** Classify this restaurant customer enquiry.

**Issue:** No approved categories, urgency definitions, output structure or missing-information rule were provided.

## Final Version - v1.1
### Prompt Text
You are a customer enquiry assistant for a medium-sized restaurant chain.

Analyse the customer enquiry below using only the information provided.

Classify it into exactly one category:
- Booking
- Menu
- Allergy
- Opening Hours
- Delivery
- Other

Assign one urgency level:
- High: an allergy, immediate safety concern or urgent same-day accessibility issue is explicitly stated
- Medium: the enquiry concerns a same-day booking or unresolved service issue
- Low: a routine enquiry with no immediate risk

Return exactly:
1. Category
2. Urgency
3. Reason for classification
4. Details found in the message
5. Missing information required
6. Recommended staff action

Do not invent information or confirm table availability. If information is missing, write "Not provided - staff confirmation required."

## Example Input
Hi, I want to book a table for six people this Saturday at 7 pm.

## ChatGPT Test Evidence
### Version 1 Output
This is a booking enquiry for six people on Saturday at 7 pm.

**Issues and Limitations - Version 1:**
- The enquiry type was recognised, but no approved category label or urgency level was returned.
- Missing details such as the exact date, customer name and contact information were not identified.
- The output did not tell staff what to do next or prevent a false booking confirmation.

### Final Version v1.1 Output
1. **Category:** Booking
2. **Urgency:** Low
3. **Reason for classification:** The customer is requesting a restaurant table. No immediate safety or same-day issue is stated.
4. **Details found in the message:** Six guests; Saturday; 7 pm.
5. **Missing information required:** Customer name, contact information, exact calendar date, dietary requirements and accessibility requirements are not provided - staff confirmation required.
6. **Recommended staff action:** Confirm the missing details and check live table availability before accepting the booking.

**Improvements - Final v1.1:**
- Added controlled categories and clear urgency rules for consistent routing.
- Required the output to separate supplied facts from missing information.
- Prevented the AI from confirming availability and retained the final decision with staff.

### Comparison
Version 1 identified the general topic but did not provide an operational result. Final v1.1 applied a standard Booking category, assigned Low urgency using a stated rule, exposed all missing information and gave staff a safe next action. The improved result is more consistent and easier to route.

## Test Result
The final prompt produced a repeatable six-part classification and did not treat the request as a confirmed booking.

## Automation Potential
**High.** Suitable for first-stage inbox or web-form routing. It can classify and extract information before staff review.

## Risks and Limitations
Ambiguous messages may be misclassified; urgency can be understated if a customer describes an allergy or accessibility need indirectly; the AI cannot see live table availability.

## Mitigation and Human Oversight
Use only the customer message, route Allergy and uncertain cases for prompt staff review, and require restaurant staff to check the live booking system before confirming anything.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | No approved categories, urgency definitions, output structure or missing-information rule were provided. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added a restaurant role, fixed categories, urgency rules, six output fields, a missing-information fallback and a no-confirmation rule. | The same message was classified as Booking and Low urgency, missing fields were made visible and the next staff action was clearly stated. | Classification becomes automation-ready only when business categories, decision rules and the human hand-off are explicit. |
