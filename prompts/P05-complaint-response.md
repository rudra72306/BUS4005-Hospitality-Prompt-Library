# P05 - Customer complaint response draft

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Complaint management  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are a customer care assistant for a medium-sized restaurant chain.

Draft a professional response to the complaint using only the information and approved action provided.

The response must:

1. Acknowledge the customer's experience
2. Apologise for the long wait and cold meal
3. Explain that the matter will be investigated
4. Ask for the booking or order number
5. Provide a clear next step
6. End with a respectful closing

Use a calm and professional tone. Keep the response under 150 words.

Do not promise a refund, discount, replacement or compensation. Do not admit legal responsibility.

Write this heading above the response:
"Draft - staff review required"

Customer complaint:
"I waited one hour for my meal, and it arrived cold."

Approved action:
The restaurant manager will investigate after receiving the customer's booking or order number.
```

## 2. Intended workflow or task

P04 classification -> P05 response draft -> manager review -> response sent. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Rushed complaint replies can be inconsistent or promise outcomes that staff are not authorised to provide. A controlled draft helps staff respond promptly without overcommitting.

## 4. Automation potential

Medium. AI can draft the acknowledgement and information request, but authorised staff must review tone, facts and any remedy before sending.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Unauthorised compensation promise | High | Explicitly prohibit refunds, discounts, replacements and compensation unless approved. |
| Admission of liability | High | Prohibit legal conclusions and require manager review. |
| Insensitive or generic tone | Medium | Require acknowledgement of the stated experience and staff editing before send. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
Complaint: "I waited one hour for my meal, and it arrived cold."
Approved action: The manager will investigate after receiving the booking or order number.
```

## Version 1 test

### Version 1 prompt

```text
Reply to this restaurant complaint:

"I waited one hour for my meal, and it arrived cold."
```

### Version 1 output

```text
We are very sorry. We will give you a full refund and a free meal on your next visit.
```

### Issue identified

Version 1 made unapproved compensation promises and did not gather the information needed for investigation.

## Version 2 test

### Version 2 output

```text
Draft - staff review required

Hello,

Thank you for contacting us. We are sorry that you waited one hour for your meal and that it arrived cold. We understand this would have been disappointing.

Our restaurant manager will investigate the matter. Please reply with your booking or order number so the relevant details can be reviewed. Once we receive that information, a staff member will contact you about the next step.

Kind regards,
Customer Care Team
```

### Improvement observed

Version 2 limits the response to an approved action, requests the relevant identifier, marks the message as a draft and retains staff approval.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 made unapproved compensation promises and did not gather the information needed for investigation. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 limits the response to an approved action, requests the relevant identifier, marks the message as a draft and retains staff approval. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
