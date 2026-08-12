# P07 - Shift handover

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Restaurant operations  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are a shift supervisor for a medium-sized restaurant chain.

Convert the notes below into a professional handover for the next shift. Use only the information provided.

Use these sections:

1. Staffing
2. Upcoming bookings
3. Customer issues
4. Equipment problems
5. Stock shortages
6. Safety concerns
7. Priority actions for the next shift

For every action, include:

- Priority: High, Medium or Low
- Action required
- Responsible person
- Deadline

Do not invent completed actions, employee names or deadlines.

If the responsible person or deadline is missing, write:
"Not assigned - supervisor confirmation required."

Staff notes:
"Two staff members were absent. Table 12 complained about slow service. The coffee machine is leaking. Only five chicken portions remain. A booking for 20 guests is expected at 7 pm."
```

## 2. Intended workflow or task

Outgoing shift notes -> P07 structured handover -> supervisor verifies assignments -> incoming shift acts. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Informal handovers can omit operational and safety issues. A consistent structure makes the next shift's priorities visible and reduces reliance on memory.

## 4. Automation potential

Medium. AI can structure notes and suggest priority based on stated conditions, but a supervisor must verify facts, assign people and confirm deadlines.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Invented completion, owner or deadline | High | Require explicit missing-assignment wording and supervisor sign-off. |
| Safety issue understated | High | Place safety concerns in a dedicated section and require equipment assessment. |
| Sensitive staff information included | Medium | Use role-level information unless names are operationally necessary and authorised. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
Two staff members absent; Table 12 complained about slow service; coffee machine leaking; five chicken portions remain; booking for 20 guests at 7 pm.
```

## Version 1 test

### Version 1 prompt

```text
Create a shift handover using these restaurant notes:

"Two staff members were absent. Table 12 complained about slow service. The coffee machine is leaking. Only five chicken portions remain. A booking for 20 guests is expected at 7 pm."
```

### Version 1 output

```text
Handover: We were short-staffed, Table 12 complained about slow service, the coffee machine needs fixing, chicken is low and a large booking is arriving at 7 pm. Please deal with these issues.
```

### Issue identified

Version 1 summarised the notes but did not organise them by function or assign priority, ownership and timing.

## Version 2 test

### Version 2 output

```text
1. Staffing
- Two staff members were absent.

2. Upcoming bookings
- A booking for 20 guests is expected at 7 pm.

3. Customer issues
- Table 12 complained about slow service.

4. Equipment problems
- The coffee machine is leaking.

5. Stock shortages
- Five chicken portions remain.

6. Safety concerns
- The leaking coffee machine may require isolation and assessment. The notes do not confirm the source or severity.

7. Priority actions for the next shift
- Priority: High | Action: Make the coffee machine safe and arrange assessment. | Responsible person: Not assigned - supervisor confirmation required. | Deadline: Not assigned - supervisor confirmation required.
- Priority: High | Action: Prepare staffing and service plan for the 20-person booking. | Responsible person: Not assigned - supervisor confirmation required. | Deadline: Before 7 pm.
- Priority: High | Action: Verify chicken stock and menu availability. | Responsible person: Not assigned - supervisor confirmation required. | Deadline: Before the 7 pm booking.
- Priority: Medium | Action: Review and follow up the Table 12 complaint. | Responsible person: Not assigned - supervisor confirmation required. | Deadline: Not assigned - supervisor confirmation required.
```

### Improvement observed

Version 2 converts the notes into an actionable handover while clearly flagging assignments that still require supervisor confirmation.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 summarised the notes but did not organise them by function or assign priority, ownership and timing. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 converts the notes into an actionable handover while clearly flagging assignments that still require supervisor confirmation. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
