# P03 - Booking request extraction

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Customer enquiries  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
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
8. Missing information
9. Recommended action for staff

Do not guess missing details or confirm table availability.

If information is missing, write:
"Not provided - staff confirmation required."

End the response with:
"Booking is not confirmed until availability is checked by restaurant staff."

Customer message:
"My name is Alex. I need a table for eight people this Friday at 7:30 pm. One guest uses a wheelchair."
```

## 2. Intended workflow or task

Booking request -> P03 extraction -> staff checks availability and missing details -> booking confirmed or clarified. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Booking messages often arrive as free text. Missing dates, contact details or accessibility information can cause delays and poor preparation. Structured extraction gives staff a clear checklist.

## 4. Automation potential

Medium to high. AI can extract and organise stated details; staff must verify the date, accessible seating, dietary needs and live availability.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Accessibility need overlooked | High | Make accessibility a mandatory field and require staff confirmation. |
| Relative date misunderstood | High | Flag phrases such as "this Friday" until converted to an exact date by staff. |
| False confirmation | High | End every output with an explicit unconfirmed-booking notice. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
My name is Alex. I need a table for eight people this Friday at 7:30 pm. One guest uses a wheelchair.
```

## Version 1 test

### Version 1 prompt

```text
Summarise this restaurant booking request:

"My name is Alex. I need a table for eight people this Friday at 7:30 pm. One guest uses a wheelchair."
```

### Version 1 output

```text
Alex would like a table for eight people this Friday at 7:30 pm. One guest requires wheelchair access.
```

### Issue identified

Version 1 captured the main details but did not expose missing contact, dietary or exact-date information and did not warn that the booking was unconfirmed.

## Version 2 test

### Version 2 output

```text
1. Customer name: Alex
2. Requested date: This Friday; exact date not provided - staff confirmation required.
3. Requested time: 7:30 pm
4. Number of guests: Eight
5. Contact information: Not provided - staff confirmation required.
6. Dietary requirements: Not provided - staff confirmation required.
7. Accessibility requirements: Wheelchair access for one guest
8. Missing information: Exact date, contact information and dietary requirements.
9. Recommended action for staff: Confirm the exact date, contact details, dietary needs, suitable accessible seating and table availability.

Booking is not confirmed until availability is checked by restaurant staff.
```

### Improvement observed

Version 2 uses a fixed extraction schema, missing-data rule and confirmation safeguard.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 captured the main details but did not expose missing contact, dietary or exact-date information and did not warn that the booking was unconfirmed. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 uses a fixed extraction schema, missing-data rule and confirmation safeguard. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
