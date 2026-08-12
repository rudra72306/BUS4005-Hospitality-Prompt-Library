# P06 - Serious complaint escalation summary

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Complaint management  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are an operations assistant for a medium-sized restaurant chain.

Prepare a confidential escalation summary for management using only the information provided.

Use these headings:

1. Complaint summary
2. Date and method received
3. Confirmed information
4. Unconfirmed customer claims
5. Possible safety concern
6. Actions already taken
7. Missing information
8. Recommended next steps
9. Person responsible for review

Use neutral and factual language. Keep the summary under 200 words.

Do not decide what caused the illness. Do not provide medical advice, assign blame or determine legal responsibility.

If information is missing, write:
"Not provided - follow-up required."

Write this heading:
"Confidential draft - immediate management review required"

Customer complaint:
"The customer says they became sick after eating chicken at the restaurant on Monday evening."

Staff notes:
"The complaint was received by phone on Tuesday morning. No medical documents, receipt or order details were provided."

Action taken:
"The duty manager recorded the complaint."
```

## 2. Intended workflow or task

Serious complaint received -> P06 summary -> immediate management review -> investigation process. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Serious complaints carry food-safety, legal and reputational risk. Management needs a rapid factual summary that preserves uncertainty and identifies the next controlled steps.

## 4. Automation potential

Low to medium. AI may structure the initial summary, but a manager must immediately verify facts and follow approved food-safety and incident procedures.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| False causation or legal conclusion | High | Separate confirmed facts from allegations and prohibit causal, medical and legal findings. |
| Delay in escalation | High | Use an immediate-review heading and a defined responsible role. |
| Exposure of sensitive information | High | Limit access, use secure systems and include only information required for review. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
Customer says they became sick after eating chicken on Monday evening. Complaint received by phone Tuesday morning. No medical documents, receipt or order details were supplied. Duty manager recorded the complaint.
```

## Version 1 test

### Version 1 prompt

```text
Summarise this serious complaint for the restaurant manager:

"A customer says they became sick after eating chicken at the restaurant on Monday evening. The complaint was received by phone on Tuesday morning."
```

### Version 1 output

```text
The customer suffered food poisoning caused by chicken served at the restaurant on Monday. Management should accept responsibility and compensate the customer.
```

### Issue identified

Version 1 turned an allegation into a confirmed cause, assigned responsibility and recommended compensation without evidence or authority.

## Version 2 test

### Version 2 output

```text
Confidential draft - immediate management review required

1. Complaint summary: The customer reports becoming sick after eating chicken at the restaurant on Monday evening.
2. Date and method received: Tuesday morning by phone. Exact dates and times were not provided - follow-up required.
3. Confirmed information: The complaint was received and recorded by the duty manager.
4. Unconfirmed customer claims: The customer links the illness to chicken eaten at the restaurant. Causation has not been established.
5. Possible safety concern: A potential food-safety concern requires prompt review.
6. Actions already taken: The duty manager recorded the complaint.
7. Missing information: Receipt, order details, exact dates and times, contact details and supporting documents were not provided.
8. Recommended next steps: Refer immediately to the restaurant manager, obtain missing details and follow the organisation's approved food-safety complaint procedure.
9. Person responsible for review: Restaurant manager.
```

### Improvement observed

Version 2 separates confirmed facts from claims, flags missing evidence, avoids medical and legal conclusions, and requires immediate management review.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 turned an allegation into a confirmed cause, assigned responsibility and recommended compensation without evidence or authority. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 separates confirmed facts from claims, flags missing evidence, avoids medical and legal conclusions, and requires immediate management review. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
