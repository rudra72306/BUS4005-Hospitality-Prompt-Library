# Iteration Audit Log

**Student:** Rudra Patel  
**Test date:** 13 August 2026  
**Test data:** Fictional restaurant scenarios only

| Prompt | Version 1 | Version 2 change | Observed effect | Lesson learned |
|---|---|---|---|---|
| P01 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 adds a fixed taxonomy, a defined output structure, a grounding rule and a clear hand-off to staff. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P02 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 produces a consistent, concise response and limits the model to approved operating hours. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P03 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 uses a fixed extraction schema, missing-data rule and confirmation safeguard. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P04 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 defines one primary category, urgency rules, neutral wording and a clear next action. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P05 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 limits the response to an approved action, requests the relevant identifier, marks the message as a draft and retains staff approval. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P06 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 separates confirmed facts from claims, flags missing evidence, avoids medical and legal conclusions, and requires immediate management review. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P07 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 converts the notes into an actionable handover while clearly flagging assignments that still require supervisor confirmation. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P08 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 grounds every statement in the notes, records unknowns and requires manager verification. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P09 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 separates facts from unknowns, evaluates each item, requires physical verification and preserves manager approval. | Specific constraints produce more reliable drafts; human authority must remain explicit. |
| P10 | Broad instruction with limited controls | Added role, structure, grounding, missing-data handling and human review | Version 2 separates facts from recommendations and clearly marks every unsupported conclusion or missing comparison. | Specific constraints produce more reliable drafts; human authority must remain explicit. |

## Overall finding

Across all 10 tests, Version 1 usually produced a readable answer but gave insufficient control over completeness, assumptions, formatting and staff hand-off. Version 2 consistently made missing information visible and reduced unsupported claims. This is a qualitative test only; no real-world efficiency, accuracy or return-on-investment figures are claimed.
