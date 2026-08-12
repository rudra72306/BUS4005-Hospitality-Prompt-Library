# P04 - Complaint classification and urgency

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Complaint management  
**Current version:** Version 1 - initial test

## Version 1 prompt

```text
Classify this restaurant customer complaint:

"I waited one hour for my meal, and when it arrived, the food was cold."
```

## Test input

```text
I waited one hour for my meal, and when it arrived, the food was cold.
```

## Version 1 output

```text
Category: Service complaint and food quality complaint.
Urgency: High.
```

## Initial evaluation

Version 1 used two primary categories and selected High urgency without stated criteria, making routing inconsistent.

**Next iteration:** Add role, business context, required output fields, grounding constraints, missing-information handling and human review.
