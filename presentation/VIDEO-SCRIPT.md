# 5-7 Minute Consultancy Video Script

## Slide 1 - Set the scene

Good morning. My name is Rudra Patel, and today I am presenting an AI prompt library designed for a medium-sized restaurant chain. I am taking the role of a business consultant. The proposal focuses on a practical question: how can AI reduce repetitive administration without taking important decisions away from restaurant staff?

## Slide 2 - Business problem and objective

Restaurants receive many short customer messages and internal notes. These include opening-hours questions, booking requests, complaints, shift handovers, incident notes and stock updates. The information is often unstructured. Staff may miss a detail, use inconsistent wording or make a quick assumption when service is busy.

The objective of this proposal is to use AI for drafting and organising information. The AI does not confirm bookings, send messages, order stock or decide legal, safety or compensation matters. Those actions stay with authorised staff.

## Slide 3 - The proposed solution

I created 10 prompts across three connected workflows.

The first workflow covers customer enquiries. Prompt 1 classifies the message, Prompt 2 drafts a response about approved opening hours, and Prompt 3 extracts booking details.

The second workflow covers complaints. Prompt 4 classifies a complaint, Prompt 5 drafts a controlled response, and Prompt 6 prepares a confidential management summary for a serious complaint.

The third workflow supports daily operations. It includes shift handover, incident reporting, stock shortage analysis and a weekly management summary.

This structure is useful because the prompts support real workflow steps instead of operating as 10 unrelated writing tasks.

## Slide 4 - Prompt design strategies

I used several prompt design strategies. Each improved prompt gives the AI a clear role, action and business context. It also defines how the result must be evaluated.

For factual tasks, I used the instruction, use only the information provided. I added fixed headings, category lists, urgency definitions and word limits. When information is missing, the AI must say that staff confirmation is required instead of guessing.

I also added explicit exclusions. For example, the AI cannot promise compensation, confirm availability, decide what caused an illness or incident, or assign blame. These controls make the output more suitable for human review.

## Slide 5 - Booking example and iteration

Prompt 3 shows the improvement process clearly. Version 1 simply asked the AI to summarise a booking message. It captured the party size and time, but it did not clearly identify the missing contact details, dietary requirements or exact date. It also did not state that the table was unconfirmed.

Version 2 uses nine required fields. It flags missing information, records the wheelchair access requirement and ends with a clear notice that restaurant staff must check availability. The lesson is that a readable answer is not always an operationally complete answer.

## Slide 6 - High-risk examples

The serious complaint and incident prompts have stronger controls because the consequences of error are higher.

In the serious complaint test, Version 1 incorrectly described the customer's illness as confirmed food poisoning caused by the restaurant. Version 2 separates confirmed information from the customer's unverified claim. It avoids medical and legal conclusions and sends the matter for immediate management review.

The incident-report prompt follows the same principle. It records the wet floor and first aid but does not invent an injury, cause or responsible person. Missing evidence is clearly listed for manager follow-up.

## Slide 7 - Business value and governance

The expected business value is more consistent documentation, clearer handovers, faster first drafts and better visibility of missing information. I have not claimed a percentage saving or financial return because no workplace pilot data was supplied.

Instead, management should measure the current manual handling time and compare it with a controlled pilot. Useful measures include average drafting time, number of staff edits, missing-field rate, classification accuracy and correct escalation of serious cases.

The main risks are hallucination, privacy exposure, outdated operating information and staff over-reliance. The controls are approved data sources, limited access, audit records, staff training and mandatory human sign-off for external messages and high-risk records.

## Slide 8 - Recommendation

I recommend a four-week controlled pilot. The restaurant should begin with lower-risk prompts such as opening-hours responses and booking extraction. Serious complaints and workplace incidents should remain under immediate management review throughout the pilot.

At the end of four weeks, management should compare the pilot measures with the manual baseline and collect staff feedback. The library should only expand if accuracy, governance and operational value are acceptable.

In summary, this proposal uses AI as a drafting and decision-support tool, not as a replacement for staff responsibility. Thank you.
