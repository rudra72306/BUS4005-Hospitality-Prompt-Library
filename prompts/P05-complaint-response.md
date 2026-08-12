# P05 - Customer complaint response draft

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Complaint management  
**Current version:** Version 1 - initial test

## Version 1 prompt

```text
Reply to this restaurant complaint:

"I waited one hour for my meal, and it arrived cold."
```

## Test input

```text
Complaint: "I waited one hour for my meal, and it arrived cold."
Approved action: The manager will investigate after receiving the booking or order number.
```

## Version 1 output

```text
We are very sorry. We will give you a full refund and a free meal on your next visit.
```

## Initial evaluation

Version 1 made unapproved compensation promises and did not gather the information needed for investigation.

**Next iteration:** Add role, business context, required output fields, grounding constraints, missing-information handling and human review.
