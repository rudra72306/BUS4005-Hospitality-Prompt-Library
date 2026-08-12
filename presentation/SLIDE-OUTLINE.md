# Consultancy Pitch - Slide Outline

## Slide 1 - Title and set the scene

- AI-assisted workflow automation for a medium-sized restaurant chain
- BUS4005 Assessment 1
- Rudra Patel, consultant presentation

## Slide 2 - Business problem and objective

- High volume of short, unstructured messages and staff notes
- Risk of missing details, inconsistent responses and unsafe assumptions
- Objective: create controlled AI drafts while keeping staff approval

## Slide 3 - Proposed 10-prompt solution

- Customer enquiries: P01-P03
- Complaint management: P04-P06
- Restaurant operations: P07-P10
- Three linked workflows rather than 10 unrelated prompts

## Slide 4 - Prompt design strategies

- Role, action, context and evaluation criteria
- Grounding: use only supplied information
- Fixed headings, categories, urgency rules and length limits
- Missing-information fallbacks and explicit exclusions
- Human-in-the-loop controls

## Slide 5 - Example: booking request

- P03 extracts eight required booking fields
- Version 1 missed contact, dietary and exact-date gaps
- Version 2 flags unknowns and prohibits false confirmation

## Slide 6 - Examples: serious complaint and incident

- P06 separates a customer's claim from confirmed facts
- P08 prevents invented causation, injury or blame
- Both require immediate human review

## Slide 7 - Business value, measures and governance

- Expected value: consistency, completeness, faster drafting and clearer escalation
- Pilot measures: handling time, revision rate, missing-field rate and escalation accuracy
- Risks: hallucination, privacy, outdated data and over-reliance
- Controls: approved inputs, access restrictions, audit logs and manager sign-off

## Slide 8 - Recommendation and next steps

- Run a four-week controlled pilot with routine, low-risk workflows first
- Keep serious complaints and incidents in mandatory management review
- Compare pilot measures with the manual baseline
- Expand only after accuracy, governance and staff feedback are acceptable
