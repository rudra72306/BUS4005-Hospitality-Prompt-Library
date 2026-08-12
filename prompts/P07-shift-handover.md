# P07 - Shift handover

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Restaurant operations  
**Current version:** Version 1 - initial test

## Version 1 prompt

```text
Create a shift handover using these restaurant notes:

"Two staff members were absent. Table 12 complained about slow service. The coffee machine is leaking. Only five chicken portions remain. A booking for 20 guests is expected at 7 pm."
```

## Test input

```text
Two staff members absent; Table 12 complained about slow service; coffee machine leaking; five chicken portions remain; booking for 20 guests at 7 pm.
```

## Version 1 output

```text
Handover: We were short-staffed, Table 12 complained about slow service, the coffee machine needs fixing, chicken is low and a large booking is arriving at 7 pm. Please deal with these issues.
```

## Initial evaluation

Version 1 summarised the notes but did not organise them by function or assign priority, ownership and timing.

**Next iteration:** Add role, business context, required output fields, grounding constraints, missing-information handling and human review.
