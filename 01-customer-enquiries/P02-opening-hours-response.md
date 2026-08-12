# Prompt 2 - Opening Hours Response

## Intended Workflow or Task
Draft a response to a routine opening-hours enquiry.

## Problem Being Solved
Staff repeatedly answer simple questions about operating hours. Manual replies take attention during busy periods and may include inconsistent wording or unapproved information.

## Version 1
**Prompt:** Reply to this restaurant customer enquiry.

**Issue:** The prompt did not limit the response to approved information or control length, tone, availability claims and promotional content.

## Final Version - v1.1
### Prompt Text
You are a customer service assistant for a medium-sized restaurant chain.

Write a clear and professional response using only the customer enquiry and approved information provided.

The response must include:
1. A friendly greeting
2. A direct answer to the question
3. The approved opening hours
4. An invitation to contact the restaurant to make a booking
5. A polite closing

Keep the response under 100 words.

Do not invent menu details, prices, special offers, holiday hours or booking availability.

Add this heading above the response: "Draft - staff review required"

## Example Input
Customer enquiry: Are you open on Sunday night?
Approved information: The restaurant is open on Sunday from 5 pm to 10 pm.

## ChatGPT Test Evidence
### Version 1 Output
Yes, we are open Sunday night from 5 pm to 10 pm. We have plenty of tables available and a special dinner menu, so book now.

**Issues and Limitations - Version 1:**
- The correct hours were included, but table availability and a special menu were invented.
- There was no staff-review label or approved-information boundary.
- The wording could create a customer expectation that the restaurant had not confirmed.

### Final Version v1.1 Output
**Draft - staff review required**

Hello,

Yes, we are open on Sunday from 5 pm to 10 pm. You are welcome to contact the restaurant if you would like to make a booking.

Kind regards,  
Restaurant Customer Service

**Improvements - Final v1.1:**
- Restricted the answer to approved operating information.
- Prohibited invented offers, holiday hours and booking availability.
- Added a concise structure and staff-review label before customer communication.

### Comparison
Version 1 answered the question but added unverified availability and promotional details. Final v1.1 used only the approved Sunday hours, invited the customer to contact the restaurant without promising a table and clearly labelled the response as a draft. This reduces service and reputational risk.

## Test Result
The improved prompt produced a short, professional response containing only the approved information.

## Automation Potential
**High for drafting.** Routine responses can be generated quickly from an approved hours record, but staff approval is required before sending.

## Risks and Limitations
Opening hours may be outdated or different on public holidays; incorrect approved data will still produce an incorrect response; automatic sending could direct a message to the wrong customer or channel.

## Mitigation and Human Oversight
Use a maintained source for opening hours, verify holiday exceptions and keep sending under staff or an approved communication system.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | The prompt did not limit the response to approved information or control length, tone, availability claims and promotional content. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added a customer-service role, approved-information rule, required message elements, word limit, prohibited claims and a staff-review heading. | The final output retained the correct hours while removing invented table availability and menu claims. | Customer-facing drafting needs both tone guidance and clear limits on what the AI is authorised to say. |
