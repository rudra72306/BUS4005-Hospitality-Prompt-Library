# P09 - Stock shortage analysis

**Business field:** Hospitality - medium-sized restaurant chain  
**Workflow:** Restaurant operations  
**Current version:** Version 2  
**Status:** Tested with fictional, non-personal sample data  
**Student:** Rudra Patel

---

## 1. Prompt text - Version 2 (current)

```text
You are an inventory assistant for a medium-sized restaurant chain.

Analyse the stock information below using only the information provided.

For each item, include:

1. Item name
2. Current quantity
3. Expected demand
4. Possible effect on service
5. Priority: Critical, High, Medium or Low
6. Recommended staff action
7. Information requiring confirmation

After listing all items, identify the three most urgent actions for the restaurant manager.

Do not invent required quantities, prices, delivery times or supplier availability.

If information is missing, write:
"Not provided - physical stock check required."

All quantities must be physically verified, and a manager must approve orders.

Stock information:
"The restaurant has five chicken portions, no orange juice and two bags of rice remaining. There are 60 dinner bookings tonight. Supplier and delivery information is unavailable."
```

## 2. Intended workflow or task

Stock data and bookings -> P09 analysis -> physical check -> manager-approved action or order. The AI prepares a draft or structured record; an authorised staff member checks the source information and completes the business action.

## 3. Problem being solved

A raw stock note does not show which item may affect service or what must be checked before ordering. Structured analysis supports faster pre-service decisions without fabricating demand.

## 4. Automation potential

Medium. AI can organise shortages and highlight service risks, but staff must count stock and management must approve changes and orders.

**Human-in-the-loop control:** The AI output is a draft. Staff remain responsible for checking facts, accessing live restaurant systems, making decisions and communicating externally.

## 5. Risks and limitations

| Risk | Level | Mitigation |
|---|---|---|
| Wrong quantity or unit | High | Require physical verification and record pack size where relevant. |
| Unnecessary or impossible order | High | Do not invent supplier availability or delivery time; keep approval with the manager. |
| Demand inferred from total bookings | Medium | State that menu-level demand is unknown until confirmed. |

The prompt cannot access live bookings, stock, personnel, supplier, safety or complaint systems unless an approved integration is provided.

---

## Test input

```text
Five chicken portions, no orange juice, two bags of rice, 60 dinner bookings tonight, no supplier or delivery information.
```

## Version 1 test

### Version 1 prompt

```text
Summarise these restaurant stock shortages:

"The restaurant has five chicken portions, no orange juice and two bags of rice remaining. There are 60 dinner bookings tonight."
```

### Version 1 output

```text
The restaurant is running low on chicken and rice and has no orange juice. With 60 bookings tonight, staff should urgently order more stock.
```

### Issue identified

Version 1 assumed an urgent order was the right action even though demand, package size, supplier and delivery information were missing.

## Version 2 test

### Version 2 output

```text
Chicken
1. Item name: Chicken portions
2. Current quantity: Five portions
3. Expected demand: Not provided - physical stock check required.
4. Possible effect on service: Chicken dishes may become unavailable if demand exceeds five portions.
5. Priority: High
6. Recommended staff action: Physically verify stock and review tonight's menu and bookings before service.
7. Information requiring confirmation: Demand by menu item, other usable stock, supplier and delivery options.

Orange juice
1. Item name: Orange juice
2. Current quantity: None
3. Expected demand: Not provided - physical stock check required.
4. Possible effect on service: Orange juice cannot be served unless stock is available elsewhere.
5. Priority: Critical
6. Recommended staff action: Verify zero stock and decide whether to replenish or mark the item unavailable.
7. Information requiring confirmation: Demand, backup stock, supplier and delivery options.

Rice
1. Item name: Rice
2. Current quantity: Two bags
3. Expected demand: Not provided - physical stock check required.
4. Possible effect on service: Effect cannot be confirmed without bag size, recipe usage and expected orders.
5. Priority: Medium
6. Recommended staff action: Verify bag size and expected usage before service.
7. Information requiring confirmation: Bag size, demand, existing prepared rice, supplier and delivery options.

Three most urgent actions
1. Verify all three quantities physically.
2. Decide how to communicate unavailable orange juice and potentially limited chicken items before service.
3. Review expected menu demand for the 60 bookings and obtain manager approval before any order.
```

### Improvement observed

Version 2 separates facts from unknowns, evaluates each item, requires physical verification and preserves manager approval.

## Audit log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| Version 1 | Used a short, broad instruction. | Version 1 assumed an urgent order was the right action even though demand, package size, supplier and delivery information were missing. | Business prompts need explicit context, fields, constraints and a safe hand-off. |
| Version 2 | Version 2 separates facts from unknowns, evaluates each item, requires physical verification and preserves manager approval. | Output became more complete, consistent and safer for staff review. | AI should structure work, while authorised people retain decisions and system actions. |

## Final evaluation

Version 2 is more suitable because it controls the role, input, output format, missing information and prohibited assumptions. Testing shows a clear qualitative improvement, but no time-saving percentage or financial return is claimed because no workplace pilot data was supplied.
