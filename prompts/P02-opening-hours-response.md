# P02 - Opening-hours enquiry response

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Customer enquiries  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are a customer service assistant for a medium-sized restaurant chain.

Write a clear and professional response to the customer using only the approved information provided.

Your response must include:

1. A friendly greeting
2. A direct answer to the question
3. The correct Sunday opening hours
4. An invitation to make a booking
5. A polite closing

Keep the response under 100 words.

Do not invent menu details, prices, special offers or booking availability.

Customer enquiry:
"Are you open on Sunday night?"

Approved information:
The restaurant is open on Sunday from 5 pm to 10 pm.
```

## 2. Intended workflow or task

Opening-hours question -> P02 draft -> staff review -> response sent. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Staff repeatedly answer simple opening-hours questions. A controlled draft reduces repetitive writing and helps keep wording consistent across channels.

## 4. Automation potential

High for drafting. Approved opening hours can be inserted automatically, but staff or a maintained knowledge base must verify the hours before sending.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Outdated opening hours | High | Pull hours from an approved source and review holiday exceptions. |
| Invented offers or availability | Medium | Explicitly prohibit unapproved menu, price, offer and availability claims. |
| Message sent to the wrong channel or customer | Medium | Keep final sending under staff or approved system control. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
Customer enquiry: "Are you open on Sunday night?"
Approved information: The restaurant is open on Sunday from 5 pm to 10 pm.
```

## Version 1 test

### Version 1 prompt

```text
Reply to this restaurant customer enquiry:

"Are you open on Sunday night?"

The restaurant is open on Sunday from 5 pm to 10 pm.
```

### Version 1 output

```text
Yes, we are open on Sunday night from 5 pm to 10 pm. Would you like to make a booking?
```

### Issue identified

Version 1 answered correctly, but it did not define tone, length, approved data or information that must not be invented.

## Version 2 test

### Version 2 output

```text
Hello,

Yes, we are open on Sunday from 5 pm to 10 pm. You are welcome to contact us to make a booking.

Kind regards,
Restaurant Customer Service
```

### Improvement observed

Version 2 produces a consistent, concise response and limits the model to approved operating hours.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 answered correctly, but it did not define tone, length, approved data or information that must not be invented. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 produces a consistent, concise response and limits the model to approved operating hours. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
