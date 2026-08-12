# P03 - Booking request extraction

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Customer enquiries  
**Current version:** Version 1 - initial test

## Version 1 prompt

```text
Summarise this restaurant booking request:

"My name is Alex. I need a table for eight people this Friday at 7:30 pm. One guest uses a wheelchair."
```

## Test input

```text
My name is Alex. I need a table for eight people this Friday at 7:30 pm. One guest uses a wheelchair.
```

## Version 1 output

```text
Alex would like a table for eight people this Friday at 7:30 pm. One guest requires wheelchair access.
```

## Initial evaluation

Version 1 captured the main details but did not expose missing contact, dietary or exact-date information and did not warn that the booking was unconfirmed.

**Next iteration:** Add role, business context, required output fields, grounding constraints, missing-information handling and human review.
