# P02 - Opening-hours enquiry response

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Customer enquiries  
**Current version:** Version 1 - initial test

## Version 1 prompt

```text
Reply to this restaurant customer enquiry:

"Are you open on Sunday night?"

The restaurant is open on Sunday from 5 pm to 10 pm.
```

## Test input

```text
Customer enquiry: "Are you open on Sunday night?"
Approved information: The restaurant is open on Sunday from 5 pm to 10 pm.
```

## Version 1 output

```text
Yes, we are open on Sunday night from 5 pm to 10 pm. Would you like to make a booking?
```

## Initial evaluation

Version 1 answered correctly, but it did not define tone, length, approved data or information that must not be invented.

**Next iteration:** Add role, business context, required output fields, grounding constraints, missing-information handling and human review.
