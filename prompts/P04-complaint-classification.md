# P04 - Complaint classification and urgency

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Complaint management  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are a complaint-handling assistant for a medium-sized restaurant chain.

Analyse the complaint below using only the information provided.

Select exactly one primary category:

- Food Quality
- Service
- Billing
- Booking
- Staff Behaviour
- Safety or Allergy
- Other

Assign one urgency level:

- High: injury, allergic reaction, food safety concern, discrimination, threat or legal action
- Medium: serious delay, repeated problem or unresolved billing issue
- Low: routine dissatisfaction without an immediate risk

Provide:

1. Primary category
2. Secondary issue, if applicable
3. Urgency level
4. Factual summary
5. Reason for classification
6. Recommended staff action

Do not blame the customer or restaurant employees. Do not invent any information.

Customer complaint:
"I waited one hour for my meal, and when it arrived, the food was cold."
```

## 2. Intended workflow or task

Complaint received -> P04 classification -> P05 response draft or P06 management escalation. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Complaints can be labelled differently by different staff, causing inconsistent routing and response times. A shared taxonomy supports predictable triage while preserving manager judgment.

## 4. Automation potential

High for initial triage of routine complaints. Staff must review edge cases, safety concerns and any complaint involving legal or compensation decisions.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Serious complaint marked too low | High | Use explicit High-risk triggers and require manager review of safety-related content. |
| Multiple issues forced into one category | Medium | Allow one secondary issue while retaining one primary routing category. |
| Bias or blame in summary | Medium | Require neutral language and prohibit assigning blame. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
I waited one hour for my meal, and when it arrived, the food was cold.
```

## Version 1 test

### Version 1 prompt

```text
Classify this restaurant customer complaint:

"I waited one hour for my meal, and when it arrived, the food was cold."
```

### Version 1 output

```text
Category: Service complaint and food quality complaint.
Urgency: High.
```

### Issue identified

Version 1 used two primary categories and selected High urgency without stated criteria, making routing inconsistent.

## Version 2 test

### Version 2 output

```text
1. Primary category: Service
2. Secondary issue: Food Quality
3. Urgency level: Medium
4. Factual summary: The customer reports waiting one hour for a meal and receiving it cold.
5. Reason for classification: The one-hour wait is the main service issue. Cold food is a secondary quality issue. The stated delay meets the Medium definition, and no immediate safety issue is reported.
6. Recommended staff action: Record the complaint, acknowledge both issues and refer it to the duty manager for review and an approved response.
```

### Improvement observed

Version 2 defines one primary category, urgency rules, neutral wording and a clear next action.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 used two primary categories and selected High urgency without stated criteria, making routing inconsistent. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 defines one primary category, urgency rules, neutral wording and a clear next action. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
