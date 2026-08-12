# P08 - Workplace incident report draft

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Restaurant operations  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are a workplace incident documentation assistant for a medium-sized restaurant chain.

Prepare a factual incident report using only the notes provided.

Use this structure:

1. Incident date
2. Incident time
3. Location
4. Person involved
5. Factual description in time order
6. Injury or damage reported
7. Immediate actions taken
8. Witnesses or available evidence
9. Missing information
10. Required follow-up

Use neutral and professional language.

Do not guess the cause, assign blame or make medical or legal conclusions.

If information is unavailable, write:
"Not recorded - manager follow-up required."

Write this heading:
"Draft incident report - manager verification required"

Incident notes:
"At approximately 8 pm, a waiter slipped near the kitchen door. The floor was wet. The duty manager provided first aid. The date, injury details and witness names were not recorded."
```

## 2. Intended workflow or task

Incident notes -> P08 factual draft -> manager verifies evidence -> official incident process. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Incident notes may be incomplete and inconsistently written. A factual draft can speed documentation, but accuracy and legal sensitivity require strict controls.

## 4. Automation potential

Low to medium. AI can organise facts but must never submit the official report. Management must verify evidence, injury details and required reporting actions.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Invented cause, injury or blame | High | Use only recorded facts and an explicit no-inference rule. |
| Missing legally important details | High | Create a dedicated missing-information and follow-up section. |
| Draft mistaken for final record | High | Display a manager-verification heading and require official sign-off. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
At approximately 8 pm, a waiter slipped near the kitchen door. The floor was wet. The duty manager provided first aid. Date, injury details and witness names were not recorded.
```

## Version 1 test

### Version 1 prompt

```text
Write an incident report using these restaurant staff notes:

"At approximately 8 pm, a waiter slipped near the kitchen door. The floor was wet. The duty manager provided first aid."
```

### Version 1 output

```text
At 8 pm, a waiter slipped because the wet floor had not been cleaned. The employee was injured and received first aid. The kitchen team was responsible for leaving the floor unsafe.
```

### Issue identified

Version 1 invented causation, injury and blame, which could create an inaccurate workplace record.

## Version 2 test

### Version 2 output

```text
Draft incident report - manager verification required

1. Incident date: Not recorded - manager follow-up required.
2. Incident time: Approximately 8 pm.
3. Location: Near the kitchen door.
4. Person involved: A waiter; name not recorded - manager follow-up required.
5. Factual description in time order: At approximately 8 pm, a waiter slipped near the kitchen door. The floor was wet.
6. Injury or damage reported: Not recorded - manager follow-up required.
7. Immediate actions taken: The duty manager provided first aid.
8. Witnesses or available evidence: Not recorded - manager follow-up required.
9. Missing information: Date, exact time, employee name, injury details, witness details, evidence and further actions.
10. Required follow-up: The manager should verify the missing information and complete the organisation's incident process.
```

### Improvement observed

Version 2 grounds every statement in the notes, records unknowns and requires manager verification.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 invented causation, injury and blame, which could create an inaccurate workplace record. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 grounds every statement in the notes, records unknowns and requires manager verification. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
