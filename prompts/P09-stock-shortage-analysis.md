# P09 - Stock shortage analysis

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Restaurant operations  
**Current version:** Version 1 - initial test

## Version 1 prompt

```text
Summarise these restaurant stock shortages:

"The restaurant has five chicken portions, no orange juice and two bags of rice remaining. There are 60 dinner bookings tonight."
```

## Test input

```text
Five chicken portions, no orange juice, two bags of rice, 60 dinner bookings tonight, no supplier or delivery information.
```

## Version 1 output

```text
The restaurant is running low on chicken and rice and has no orange juice. With 60 bookings tonight, staff should urgently order more stock.
```

## Initial evaluation

Version 1 assumed an urgent order was the right action even though demand, package size, supplier and delivery information were missing.

**Next iteration:** Add role, business context, required output fields, grounding constraints, missing-information handling and human review.
