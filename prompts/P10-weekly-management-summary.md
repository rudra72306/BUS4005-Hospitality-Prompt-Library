# P10 - Weekly management summary

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Restaurant operations  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
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

If there is not enough information to draw a conclusion, write:
"Insufficient information - management review required."

Reporting period:
3-9 August 2026

Records:

- 120 bookings
- 8 customer complaints
- 2 staff absences
- 1 workplace incident
- 3 stock shortages
- No customer satisfaction data was collected
- No comparison data from the previous week was provided
```

## 2. Intended workflow or task

Weekly records -> P10 management summary -> manager review -> priorities for next week. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

Management summaries can become misleading when sparse operational data is turned into unsupported trends. A controlled template creates a consistent factual review and identifies data gaps.

## 4. Automation potential

Medium. AI can structure verified records and draft priorities, but managers must validate source data, interpret performance and approve actions.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Invented trends or causes | High | Prohibit comparisons and explanations unless data is supplied. |
| Sensitive names included | Medium | Use aggregate data and exclude customer and employee names. |
| Recommendations presented as facts | High | Separate recorded facts, conclusions and recommendations into distinct sections. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
Reporting period 3-9 August 2026: 120 bookings, 8 complaints, 2 absences, 1 incident and 3 stock shortages. No satisfaction or previous-week data.
```

## Version 1 test

### Version 1 prompt

```text
Write a weekly restaurant report using this information:

"During the week, the restaurant had 120 bookings, eight customer complaints, two staff absences, one workplace incident and three stock shortages."
```

### Version 1 output

```text
The restaurant had a busy week with 120 bookings. Customer complaints were high, staffing performance declined because of two absences, and stock shortages increased. Overall performance was below the previous week.
```

### Issue identified

Version 1 described the week as busy, called complaints high, claimed staffing declined and compared performance with a previous week that was not supplied.

## Version 2 test

### Version 2 output

```text
1. Executive summary
Recorded facts: From 3-9 August 2026, the restaurant recorded 120 bookings, 8 customer complaints, 2 staff absences, 1 workplace incident and 3 stock shortages.
Conclusion: Insufficient information - management review required.

2. Bookings and customer demand
Recorded fact: 120 bookings. No daily pattern, capacity or comparison data was provided.

3. Customer complaints
Recorded fact: 8 complaints. Complaint categories, outcomes and prior-period comparisons were not provided.

4. Staffing issues
Recorded fact: 2 staff absences. Causes and service effects were not provided.

5. Workplace safety
Recorded fact: 1 workplace incident. Severity, cause and follow-up status were not provided.

6. Stock and supply issues
Recorded fact: 3 stock shortages. Items, causes and service effects were not provided.

7. Issues requiring management review
Complaint details, incident follow-up, staffing coverage and stock-shortage causes require review.

8. Three recommended priorities for next week
1. Review the incident and confirm all required follow-up is complete.
2. Analyse complaint categories and actions taken.
3. Check staffing coverage and stock controls before peak service periods.

9. Missing information and limitations
No customer satisfaction data or previous-week comparison was provided. Causes, trends and performance changes cannot be determined.
```

### Improvement observed

Version 2 separates facts from recommendations and clearly marks every unsupported conclusion or missing comparison.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 described the week as busy, called complaints high, claimed staffing declined and compared performance with a previous week that was not supplied. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 separates facts from recommendations and clearly marks every unsupported conclusion or missing comparison. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
