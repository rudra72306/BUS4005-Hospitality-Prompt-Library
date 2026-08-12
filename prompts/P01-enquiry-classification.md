# P01 - Customer enquiry classification

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Customer enquiries  
**Current version:** Version 1 - initial test

## Version 1 prompt

```text
Classify this restaurant customer enquiry:

"Hi, I want to book a table for six people this Saturday at 7 pm."
```

## Test input

```text
Hi, I want to book a table for six people this Saturday at 7 pm.
```

## Version 1 output

```text
This is a booking enquiry for six people on Saturday at 7 pm.
```

## Initial evaluation

Version 1 identified the general topic, but it gave no urgency, missing-data check or staff action and could not support consistent routing.

**Next iteration:** Add role, business context, required output fields, grounding constraints, missing-information handling and human review.
