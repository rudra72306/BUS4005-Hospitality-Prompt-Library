# P01 - Customer enquiry classification

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Customer enquiries  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are a customer enquiry assistant for a medium-sized restaurant chain.

Analyse the customer enquiry below using only the information provided.

Classify it into exactly one category:

- Booking
- Menu
- Allergy
- Opening Hours
- Delivery
- Other

Then provide:

1. Category
2. Urgency: Low, Medium or High
3. Reason for classification
4. Booking details found in the message
5. Missing information required to process the request
6. Recommended next action for restaurant staff

Do not invent any information or confirm table availability. If information is missing, write "Not provided - staff confirmation required."

Customer enquiry:
"Hi, I want to book a table for six people this Saturday at 7 pm."
```

## 2. Intended workflow or task

Customer message -> P01 classification -> P02 response or P03 booking extraction -> staff review. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Unstructured enquiries can be routed inconsistently or processed with missing details. This prompt standardises the first review so staff can identify the request and the information still needed.

## 4. Automation potential

High for first-stage classification. AI can classify and extract stated details, but restaurant staff must check availability and confirm the booking.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Wrong category or urgency | Medium | Use a fixed category list and require staff review for unusual or safety-related messages. |
| Invented booking details | High | Use only the customer message and require a missing-information statement. |
| Booking treated as confirmed | High | The prompt prohibits confirmation; staff must check the booking system. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
Hi, I want to book a table for six people this Saturday at 7 pm.
```

## Version 1 test

### Version 1 prompt

```text
Classify this restaurant customer enquiry:

"Hi, I want to book a table for six people this Saturday at 7 pm."
```

### Version 1 output

```text
This is a booking enquiry for six people on Saturday at 7 pm.
```

### Issue identified

Version 1 identified the general topic, but it gave no urgency, missing-data check or staff action and could not support consistent routing.

## Version 2 test

### Version 2 output

```text
1. Category: Booking
2. Urgency: Low
3. Reason for classification: The customer is requesting a restaurant table. No immediate safety or service risk is stated.
4. Booking details found in the message:
   - Number of guests: Six
   - Requested day: Saturday
   - Requested time: 7 pm
5. Missing information required to process the request:
   - Customer name: Not provided - staff confirmation required.
   - Contact information: Not provided - staff confirmation required.
   - Exact date: Not provided - staff confirmation required.
   - Dietary and accessibility requirements: Not provided - staff confirmation required.
6. Recommended next action for restaurant staff: Confirm the exact date, customer details, requirements and table availability before accepting the booking.
```

### Improvement observed

Version 2 adds a fixed taxonomy, a defined output structure, a grounding rule and a clear hand-off to staff.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 identified the general topic, but it gave no urgency, missing-data check or staff action and could not support consistent routing. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 adds a fixed taxonomy, a defined output structure, a grounding rule and a clear hand-off to staff. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
