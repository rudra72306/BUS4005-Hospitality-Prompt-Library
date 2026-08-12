# Prompt 10 - Weekly Management Summary

## Intended Workflow or Task
Convert verified weekly restaurant records into a management review.

## Problem Being Solved
A short list of weekly figures can be turned into unsupported trends or performance claims. Managers need a consistent summary that clearly separates recorded facts, limitations and recommendations.

## Version 1
**Prompt:** Write a weekly restaurant report using this information.

**Issue:** The prompt did not prevent unsupported comparisons, causes, performance judgements or invented trends.

## Final Version - v1.1
### Prompt Text
You are an operations analyst for a medium-sized restaurant chain.

Prepare a professional weekly management summary using only the records provided.

Use these sections:
1. Executive summary
2. Bookings and customer demand
3. Customer complaints
4. Staffing issues
5. Workplace safety
6. Stock and supply issues
7. Issues requiring management review
8. Three recommended priorities for next week
9. Missing information and limitations

Separate recorded facts from recommendations.

Do not invent causes, trends, percentages, comparisons or performance results. Do not include customer or employee names.

If there is not enough information to draw a conclusion, write "Insufficient information - management review required."

## Example Input
Reporting period: 3-9 August 2026
Records: 120 bookings; 8 customer complaints; 2 staff absences; 1 workplace incident; 3 stock shortages.
No customer satisfaction data was collected. No comparison data from the previous week was provided.

## ChatGPT Test Evidence
### Version 1 Output
The restaurant had a busy week with 120 bookings. Complaints were high, staffing performance declined because of two absences and stock shortages increased. Overall performance was below the previous week.

**Issues and Limitations - Version 1:**
- The output called the week busy and complaints high without capacity or comparison data.
- It claimed staffing performance declined and shortages increased without evidence.
- It compared performance with a previous week even though no previous-week data was supplied.

### Final Version v1.1 Output
1. **Executive summary:** Recorded facts for 3-9 August 2026: 120 bookings, 8 complaints, 2 staff absences, 1 workplace incident and 3 stock shortages. Broader performance conclusion: Insufficient information - management review required.
2. **Bookings and customer demand:** 120 bookings recorded. Daily pattern, capacity and comparison data were not provided.
3. **Customer complaints:** 8 complaints recorded. Categories, outcomes and comparison data were not provided.
4. **Staffing issues:** 2 absences recorded. Causes and service effects were not provided.
5. **Workplace safety:** 1 incident recorded. Severity and follow-up status were not provided.
6. **Stock and supply issues:** 3 shortages recorded. Items, causes and service effects were not provided.
7. **Issues requiring management review:** Complaint details, incident follow-up, staffing coverage and stock controls.
8. **Three recommended priorities:** Confirm incident follow-up; analyse complaint categories and outcomes; review staffing coverage and stock controls before peak periods.
9. **Missing information and limitations:** No customer satisfaction or previous-week data. Causes, trends and performance changes cannot be determined.

**Improvements - Final v1.1:**
- Added nine management sections and separated facts from recommendations.
- Prohibited unsupported causes, trends, percentages and comparisons.
- Required explicit limitations when the supplied records cannot support a conclusion.

### Comparison
Version 1 turned five raw counts into unsupported performance claims. Final v1.1 reported the same figures without judgement, listed the missing information and proposed three clearly labelled management priorities. The improved version is more credible because it does not claim evidence that was never provided.

## Test Result
The final prompt produced a structured factual summary and clearly stated that trends and performance changes could not be determined.

## Automation Potential
**Medium.** Can draft a management summary from verified records, but managers must validate source data, interpret performance and approve actions.

## Risks and Limitations
Incomplete or inaccurate source records will create a misleading summary; aggregation can hide serious individual cases; recommendations may not fit local conditions; confidential information could be exposed if raw records are copied unnecessarily.

## Mitigation and Human Oversight
Use verified aggregate data, review serious incidents separately, restrict sensitive inputs, have management validate the summary and compare results only when reliable baseline data exists.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | The prompt did not prevent unsupported comparisons, causes, performance judgements or invented trends. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added nine report sections, fact-versus-recommendation separation, limitations handling and rules against unsupported trends and comparisons. | The final output retained every supplied count but removed the invented performance decline and previous-week comparison. | Management reporting prompts must make evidence limits visible so fluent language is not mistaken for valid analysis. |
