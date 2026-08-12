# BUS4005 Hospitality Prompt Library

**Subject:** AI for Business  
**Business field:** Hospitality - medium-sized restaurant chain  
**Model tested on:** ChatGPT  
**Portfolio purpose:** Demonstrate 10 tested and iterated prompts that support restaurant workflow automation while retaining human oversight.

## Business Context
A medium-sized restaurant chain receives customer enquiries, booking requests, complaints, shift notes, stock information and incident records in different formats. Staff spend time manually extracting information, checking completeness, classifying issues, drafting responses and preparing reports. This prompt library standardises those repetitive tasks while keeping bookings, safety, compensation, purchasing and management decisions under human control.

## Prompt Library
| ID | Prompt | Workflow | Automation Potential | Risk |
|---|---|---|---|---|
| P01 | [Customer Enquiry Classification](01-customer-enquiries/P01-enquiry-classification.md) | Customer Enquiries | High | Medium |
| P02 | [Opening Hours Response](01-customer-enquiries/P02-opening-hours-response.md) | Customer Enquiries | High | Medium |
| P03 | [Booking Request Extraction](02-bookings/P03-booking-request-extraction.md) | Bookings | High | Medium |
| P04 | [Booking Data Check](02-bookings/P04-booking-data-check.md) | Bookings | High | Medium |
| P05 | [Complaint Triage](03-complaint-management/P05-complaint-triage.md) | Complaint Management | High | Medium |
| P06 | [Complaint Response](03-complaint-management/P06-complaint-response.md) | Complaint Management | High | Medium |
| P07 | [Shift Handover](04-shift-operations/P07-shift-handover.md) | Shift Operations | High | Medium |
| P08 | [Stock Shortage Analysis](04-shift-operations/P08-stock-shortage-analysis.md) | Shift Operations | Medium | High |
| P09 | [Workplace Incident Report](05-management-and-safety/P09-incident-report.md) | Management and Safety | Medium | High |
| P10 | [Weekly Management Summary](05-management-and-safety/P10-weekly-management-summary.md) | Management and Safety | Medium | Medium |

## Workflow Structure
1. [Customer Enquiries](01-customer-enquiries/README.md) - classify enquiries and draft approved opening-hours responses.
2. [Bookings](02-bookings/README.md) - extract booking details and check record completeness.
3. [Complaint Management](03-complaint-management/README.md) - triage complaints and draft controlled responses.
4. [Shift Operations](04-shift-operations/README.md) - prepare handovers and analyse stock shortages.
5. [Management and Safety](05-management-and-safety/README.md) - structure incident reports and weekly management summaries.

## Prompting Strategies Used
- Role prompting to define the AI's restaurant function.
- Grounding constraints such as "use only the information provided".
- Fixed output structures for consistent operational records.
- Controlled categories and decision rules for classification and validation.
- Missing-information instructions to reduce hallucination.
- Explicit restrictions on availability confirmation, compensation, blame, legal conclusions and autonomous ordering.
- Human-review requirements for customer messages, bookings, stock actions, safety incidents and management decisions.

## Iteration and Test Evidence
Every prompt file contains Version 1, the improved final v1.1 prompt, one example input, both ChatGPT outputs, identified issues, comparison, automation potential, risks, limitations, mitigation and a detailed audit log. All examples use fictional restaurant information.

## Responsible Automation Boundary
The AI may classify, extract, check completeness, organise notes and draft messages. It does not confirm bookings, send customer communications, approve refunds, order stock, determine incident cause, assign blame or replace manager review.
