# Prompt 7 - Shift Handover

## Intended Workflow or Task
Convert outgoing-shift notes into an actionable restaurant handover.

## Problem Being Solved
Unstructured shift notes can hide safety issues, large bookings, unresolved complaints and stock shortages. Incoming staff may miss important work when completed and outstanding items are mixed together.

## Version 1
**Prompt:** Create a shift handover from these restaurant notes.

**Issue:** The output did not separate operational areas, priorities, assigned responsibility or missing information.

## Final Version - v1.1
### Prompt Text
You are a shift supervisor for a medium-sized restaurant chain.

Convert the notes below into a concise professional handover using only the information provided.

Use these headings:
1. Staffing
2. Upcoming bookings
3. Customer issues
4. Equipment problems
5. Stock shortages
6. Safety concerns
7. Completed items
8. Priority actions for the next shift
9. Missing information requiring confirmation

For each active item, include the current status, action already taken and next required action.

Do not invent completed actions, employee names, causes, deadlines or responsibilities. If a responsible person or deadline is not provided, write "Not assigned - supervisor confirmation required."

## Example Input
Two staff members were absent. Table 12 complained about slow service. The coffee machine is leaking. Only five chicken portions remain. A booking for 20 guests is expected at 7 pm.

## ChatGPT Test Evidence
### Version 1 Output
Handover: The shift was short-staffed. Table 12 complained about slow service, the coffee machine needs fixing, chicken is low and a group of 20 will arrive at 7 pm. Please handle these issues.

**Issues and Limitations - Version 1:**
- Five different operational issues were combined in one paragraph.
- The leaking machine was not clearly separated as a possible safety concern.
- There was no distinction between current status, actions taken, next actions and missing assignments.

### Final Version v1.1 Output
1. **Staffing:** Two staff members were absent. Action already taken: Not provided. Next action: Confirm staffing coverage for the next shift.
2. **Upcoming bookings:** Booking for 20 guests at 7 pm. Action already taken: Not provided. Next action: Confirm table, staffing and service preparation.
3. **Customer issues:** Table 12 complained about slow service. Action already taken: Not provided. Next action: Confirm whether follow-up is required.
4. **Equipment problems:** Coffee machine is leaking. Action already taken: Not provided. Next action: Isolate or assess the machine according to restaurant procedure.
5. **Stock shortages:** Five chicken portions remain. Next action: Physically verify stock and review expected menu demand.
6. **Safety concerns:** The leaking coffee machine requires supervisor assessment; the source and severity are not provided.
7. **Completed items:** None recorded.
8. **Priority actions for the next shift:** Assess the leaking machine; prepare for the 20-person booking; verify chicken stock; review the complaint. Responsible people are not assigned - supervisor confirmation required.
9. **Missing information requiring confirmation:** Actions already taken, responsible people, deadlines, complaint follow-up and equipment status.

**Improvements - Final v1.1:**
- Separated nine operational areas so open issues can be scanned quickly.
- Added status, action taken, next action and missing-information requirements.
- Prevented invented owners and deadlines while retaining supervisor control.

### Comparison
Version 1 accurately repeated the notes but left all issues in one paragraph. Final v1.1 separated staffing, bookings, customer, equipment, stock and safety information, then listed the next actions and unknown assignments. The improved result is more actionable for the incoming shift.

## Test Result
The final prompt made every open issue visible and did not invent a person, deadline or completed action.

## Automation Potential
**High.** Can standardise handovers from staff notes before responsibility transfers to the incoming shift.

## Risks and Limitations
Incomplete notes will produce an incomplete handover; AI-assigned priority may not match live conditions; sensitive staff information may be unnecessarily included; a safety issue can be understated.

## Mitigation and Human Oversight
Outgoing and incoming supervisors verify the handover together, staff names are excluded unless necessary, and equipment or safety concerns follow normal restaurant procedures immediately.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | The output did not separate operational areas, priorities, assigned responsibility or missing information. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added nine workflow headings, status/action/next-action fields, missing-information rules and restrictions on invented owners, deadlines and completed work. | The five issues were separated into an actionable handover and the leaking machine was made visible for supervisor assessment. | Workflow-specific structure is more useful than a general summary when responsibility is being transferred between shifts. |
