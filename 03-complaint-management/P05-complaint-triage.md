# Prompt 5 - Complaint Triage

## Intended Workflow or Task
Classify and prioritise a restaurant customer complaint.

## Problem Being Solved
Complaints arrive in free text and can involve more than one issue. Inconsistent classification makes routing, escalation and response tracking harder for managers and customer-service staff.

## Version 1
**Prompt:** Classify this restaurant customer complaint.

**Issue:** No approved categories, primary-issue rule or urgency definitions were supplied.

## Final Version - v1.1
### Prompt Text
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
- High: injury, allergic reaction, food-safety concern, discrimination, threat or legal action is explicitly reported
- Medium: serious delay, repeated problem or unresolved billing issue
- Low: routine dissatisfaction without an immediate risk

Return:
1. Primary category
2. Secondary issue, if applicable
3. Urgency
4. Factual summary
5. Reason for classification
6. Recommended staff action

Do not blame the customer or employees. Do not invent facts or decide compensation.

## Example Input
I waited one hour for my meal, and when it arrived, the food was cold.

## ChatGPT Test Evidence
### Version 1 Output
This is a service and food-quality complaint. It appears serious and should be handled urgently.

**Issues and Limitations - Version 1:**
- Two categories were returned without one standard primary routing category.
- “Serious” and “urgently” were subjective because no urgency rules were defined.
- No factual summary, reason or controlled staff action was provided.

### Final Version v1.1 Output
1. **Primary category:** Service
2. **Secondary issue:** Food Quality
3. **Urgency:** Medium
4. **Factual summary:** The customer reports waiting one hour for a meal and receiving it cold.
5. **Reason for classification:** The one-hour wait is the main service issue. Cold food is a secondary quality issue. The stated serious delay meets the Medium rule, and no immediate safety concern is reported.
6. **Recommended staff action:** Record the complaint, acknowledge both issues and refer it to the duty manager for review and an approved response.

**Improvements - Final v1.1:**
- Added one controlled primary category plus an optional secondary issue.
- Defined High, Medium and Low urgency using restaurant risk and service rules.
- Required neutral facts, reasoning and a staff action without blame or compensation decisions.

### Comparison
Version 1 recognised both issues but could not support consistent routing because it used two categories and subjective urgency. Final v1.1 selected Service as the primary category, retained Food Quality as secondary and applied the Medium rule for a serious delay. This makes the triage result easier to review and route.

## Test Result
The final prompt applied the controlled category and urgency rules without adding blame or an unsupported remedy.

## Automation Potential
**High.** Suitable for first-pass complaint routing, with manager review for High, uncertain and multi-issue cases.

## Risks and Limitations
Ambiguous language can cause misclassification; the model cannot verify the customer claim; serious safety wording may be indirect; cultural or language differences can affect interpretation.

## Mitigation and Human Oversight
Require human review of High, Safety or Allergy and unclear complaints, retain the original customer message, and allow staff to override the classification.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | No approved categories, primary-issue rule or urgency definitions were supplied. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added approved categories, one-primary-category logic, urgency definitions, factual reasoning, a controlled staff action and no-blame rules. | The same complaint was consistently classified as Service with Food Quality secondary and Medium urgency. | Controlled taxonomies and escalation rules make complaint triage more consistent while preserving human judgement. |
