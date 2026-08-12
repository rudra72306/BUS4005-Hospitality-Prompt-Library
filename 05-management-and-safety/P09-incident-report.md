# Prompt 9 - Workplace Incident Report

## Intended Workflow or Task
Prepare a factual first draft from restaurant incident notes.

## Problem Being Solved
Incident notes may be incomplete and mixed with assumptions. Inaccurate wording about cause, injury or blame can create safety, employment, insurance and legal risk.

## Version 1
**Prompt:** Write an incident report from these restaurant staff notes.

**Issue:** The AI could fill information gaps with plausible causes, injuries or blame and the draft was not clearly marked for verification.

## Final Version - v1.1
### Prompt Text
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

Use neutral professional language.

Do not guess the cause, assign blame or make medical, legal or safety-compliance conclusions.

If information is unavailable, write "Not recorded - manager follow-up required."

Add this heading: "Draft incident report - manager verification required"

## Example Input
At approximately 8 pm, a waiter slipped near the kitchen door. The floor was wet. The duty manager provided first aid. The date, injury details and witness names were not recorded.

## ChatGPT Test Evidence
### Version 1 Output
At 8 pm, a waiter slipped because kitchen staff failed to clean a wet floor. The employee was injured and received first aid. The kitchen team was responsible for leaving the area unsafe.

**Issues and Limitations - Version 1:**
- The output invented a cleaning failure, an injury and responsibility for the incident.
- Missing date, employee identity, injury details and witness information were not clearly shown.
- The report could be mistaken for a verified official record.

### Final Version v1.1 Output
**Draft incident report - manager verification required**

1. **Incident date:** Not recorded - manager follow-up required.
2. **Incident time:** Approximately 8 pm.
3. **Location:** Near the kitchen door.
4. **Person involved:** A waiter; name not recorded - manager follow-up required.
5. **Factual description in time order:** At approximately 8 pm, a waiter slipped near the kitchen door. The floor was wet.
6. **Injury or damage reported:** Not recorded - manager follow-up required.
7. **Immediate actions taken:** The duty manager provided first aid.
8. **Witnesses or available evidence:** Not recorded - manager follow-up required.
9. **Missing information:** Date, exact time, employee name, injury details, witness details, evidence and further actions.
10. **Required follow-up:** The manager must verify the missing information and complete the organisation's incident procedure.

**Improvements - Final v1.1:**
- Added a 10-field factual report structure and explicit unknown-data labels.
- Prohibited cause, blame, medical, legal and compliance conclusions.
- Clearly marked the output as a draft requiring manager verification.

### Comparison
Version 1 produced a fluent report but invented three sensitive claims. Final v1.1 recorded only the wet floor, slip and first aid, then made every missing fact visible. This is safer because it supports documentation without replacing evidence collection or the official incident process.

## Test Result
The final prompt separated recorded facts from unknown information and made no unsupported causal or injury statement.

## Automation Potential
**Medium.** Appropriate for structuring an initial draft, never for autonomous incident submission or investigation.

## Risks and Limitations
Incomplete notes can omit legally or operationally important details; sensitive employee information requires protection; staff may over-rely on a polished draft; emergencies require action before documentation.

## Mitigation and Human Oversight
Follow emergency and workplace procedures first, restrict access, verify the draft against witnesses and records, and require manager completion and sign-off.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | The AI could fill information gaps with plausible causes, injuries or blame and the draft was not clearly marked for verification. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added factual grounding, 10 report fields, missing-information labels, prohibited conclusions and a manager-verification heading. | The final report removed invented cause, injury and blame and created a clear follow-up list for management. | For high-risk documentation, AI should organise evidence and expose gaps rather than interpret cause or responsibility. |
