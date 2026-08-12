# BUS4005 Hospitality Prompt Library

**Assessment:** BUS4005 Assessment 1 - Prompt Library and Consultancy Pitch  
**Student:** Rudra Patel  
**Business field:** Hospitality  
**Organisation type:** Medium-sized restaurant chain  
**Portfolio:** https://github.com/rudra72306/BUS4005-Hospitality-Prompt-Library  
**Tested with:** ChatGPT using fictional restaurant scenarios  
**Last updated:** 13 August 2026

## Business problem

Restaurant staff handle customer enquiries, bookings, complaints, handovers, incidents, stock checks and management reporting through short, unstructured notes. This creates a risk of missing information, inconsistent wording, unsupported assumptions and unclear escalation.

This library uses 10 prompts to turn supplied information into controlled drafts and structured records. AI supports repetitive language and organisation tasks; staff keep responsibility for live-system checks, approvals, safety, legal decisions and customer communication.

## Library summary

| ID | Prompt | Workflow | Automation potential | Risk | Status |
|---|---|---|---|---|---|
| [P01](prompts/P01-enquiry-classification.md) | Customer enquiry classification | Customer enquiries | High | Medium | Tested |
| [P02](prompts/P02-opening-hours-response.md) | Opening-hours enquiry response | Customer enquiries | High | Medium | Tested |
| [P03](prompts/P03-booking-request-extraction.md) | Booking request extraction | Customer enquiries | Medium-High | High | Tested |
| [P04](prompts/P04-complaint-classification.md) | Complaint classification and urgency | Complaint management | High | High | Tested |
| [P05](prompts/P05-complaint-response.md) | Customer complaint response draft | Complaint management | Medium | High | Tested |
| [P06](prompts/P06-serious-complaint-escalation.md) | Serious complaint escalation summary | Complaint management | Low-Medium | High | Tested |
| [P07](prompts/P07-shift-handover.md) | Shift handover | Restaurant operations | Medium | High | Tested |
| [P08](prompts/P08-incident-report.md) | Workplace incident report draft | Restaurant operations | Low-Medium | High | Tested |
| [P09](prompts/P09-stock-shortage-analysis.md) | Stock shortage analysis | Restaurant operations | Medium | High | Tested |
| [P10](prompts/P10-weekly-management-summary.md) | Weekly management summary | Restaurant operations | Medium | High | Tested |

## Prompt chains

1. **Customer enquiries:** P01 classifies the message; P02 drafts a routine opening-hours response; P03 extracts a booking request for staff verification.
2. **Complaint management:** P04 classifies the complaint; P05 drafts a controlled response; P06 prepares an immediate escalation summary for a serious complaint.
3. **Restaurant operations:** P07 prepares a shift handover; P08 structures incident notes; P09 analyses stock shortages; P10 prepares a weekly management summary.

## Prompting strategies used

- Role, action, context and evaluation criteria
- "Use only the information provided" grounding constraint
- Fixed headings, categories, urgency definitions and word limits
- Missing-information fallbacks instead of guessing
- Explicit exclusions for compensation, legal, medical and causal claims
- Draft labels and mandatory human review
- Prompt chaining between related workflow steps

## Iterative evidence

Each prompt has exactly two versions. Version 1 is a broad instruction. Version 2 adds business context, structure, constraints and governance controls. Each file includes both prompts, both test outputs, the issue found, the improvement and an audit log. The GitHub commit history also records the initial and improved versions.

- [Complete iteration audit log](evaluations/ITERATION-AUDIT-LOG.md)
- [Testing method](evaluations/TEST-METHOD.md)

## Presentation materials

- [Eight-slide consultancy pitch outline](presentation/SLIDE-OUTLINE.md)
- [5-7 minute video script](presentation/VIDEO-SCRIPT.md)
- [Submission checklist](SUBMISSION-CHECKLIST.md)
- [AI acknowledgement draft](AI-ACKNOWLEDGEMENT.md)

## Repository structure

```text
.
├── README.md
├── prompts/
│   ├── P01-enquiry-classification.md
│   ├── P02-opening-hours-response.md
│   ├── P03-booking-request-extraction.md
│   ├── P04-complaint-classification.md
│   ├── P05-complaint-response.md
│   ├── P06-serious-complaint-escalation.md
│   ├── P07-shift-handover.md
│   ├── P08-incident-report.md
│   ├── P09-stock-shortage-analysis.md
│   └── P10-weekly-management-summary.md
├── evaluations/
│   ├── ITERATION-AUDIT-LOG.md
│   └── TEST-METHOD.md
├── presentation/
│   ├── SLIDE-OUTLINE.md
│   └── VIDEO-SCRIPT.md
├── AI-ACKNOWLEDGEMENT.md
└── SUBMISSION-CHECKLIST.md
```

## Responsible-use position

No prompt in this library authorises the AI to confirm a booking, send a customer message, order stock, determine incident or illness causation, offer compensation, assign blame or make legal or medical conclusions. Those actions remain with authorised staff.
