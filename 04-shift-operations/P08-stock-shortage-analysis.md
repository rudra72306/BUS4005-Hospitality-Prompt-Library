# Prompt 8 - Stock Shortage Analysis

## Intended Workflow or Task
Support pre-service review of low or unavailable restaurant stock.

## Problem Being Solved
Raw stock notes do not show which items may affect service or what information must be checked before ordering. Staff may overreact to total booking numbers without knowing item-level demand.

## Version 1
**Prompt:** Summarise these restaurant stock shortages.

**Issue:** The prompt did not define priority rules, physical verification, required information or limits on ordering recommendations.

## Final Version - v1.1
### Prompt Text
You are an inventory assistant for a medium-sized restaurant chain.

Analyse the stock information using only the information provided.

For each item, return:
1. Item name
2. Recorded current quantity
3. Expected demand
4. Possible effect on service
5. Priority: Critical, High, Medium, Low or Review Required
6. Recommended staff action
7. Information requiring confirmation

Priority rules:
- Critical: recorded quantity is zero
- High: a specific positive quantity is low and a direct service limitation is possible
- Medium: stock is limited but the service effect cannot be confirmed
- Low: no shortage is indicated
- Review Required: quantity or unit is unclear

After all items, list the three most urgent management actions.

Do not invent required quantities, menu demand, prices, supplier availability or delivery times. If information is missing, write "Not provided - physical stock check required."

All quantities must be physically verified and a manager must approve orders.

## Example Input
The restaurant has five chicken portions, no orange juice and two bags of rice remaining. There are 60 dinner bookings tonight. Supplier and delivery information is unavailable.

## ChatGPT Test Evidence
### Version 1 Output
The restaurant is running low on chicken and rice and has no orange juice. With 60 bookings tonight, staff should urgently order more stock from the supplier.

**Issues and Limitations - Version 1:**
- The output assumed that an urgent supplier order was possible without supplier or delivery information.
- It inferred demand for individual items from total bookings.
- No physical verification, manager approval or item-level priority rule was included.

### Final Version v1.1 Output
**Chicken portions**
1. Recorded current quantity: Five portions
2. Expected demand: Not provided - physical stock check required.
3. Possible effect on service: Chicken dishes may become unavailable if demand exceeds five portions.
4. Priority: High
5. Recommended staff action: Verify stock and review expected chicken orders before service.
6. Information requiring confirmation: Menu demand, backup stock and supplier options.

**Orange juice**
1. Recorded current quantity: Zero
2. Expected demand: Not provided - physical stock check required.
3. Possible effect on service: Orange juice cannot be served unless other verified stock is available.
4. Priority: Critical
5. Recommended staff action: Verify zero stock and decide whether to mark the item unavailable or seek approved replenishment.
6. Information requiring confirmation: Backup stock, demand and supplier options.

**Rice**
1. Recorded current quantity: Two bags
2. Expected demand: Not provided - physical stock check required.
3. Possible effect on service: Cannot be confirmed without bag size and expected rice orders.
4. Priority: Medium
5. Recommended staff action: Verify bag size and expected use.
6. Information requiring confirmation: Bag size, prepared stock, demand and supplier options.

**Three urgent management actions:** Verify all quantities; decide how to communicate unavailable or limited items; review expected menu demand and approve any order.

**Improvements - Final v1.1:**
- Added item-level fields and measurable priority rules.
- Separated recorded stock from unknown demand and service impact.
- Required physical verification and manager approval while prohibiting invented supplier information.

### Comparison
Version 1 identified the obvious shortage but jumped directly to an unsupported urgent order. Final v1.1 treated zero orange juice as Critical, limited chicken as High and rice as Medium under stated rules. It also made unknown demand and supplier information explicit and preserved ordering authority with management.

## Test Result
The final prompt produced a controlled item-by-item analysis without inventing demand, supplier availability or order quantities.

## Automation Potential
**Medium.** Useful for organising exception reports and preparing a manager review, but not for autonomous purchasing.

## Risks and Limitations
Recorded quantities may be wrong, unit sizes may be unclear, demand can change during service and supplier data may be unavailable or outdated.

## Mitigation and Human Oversight
Physically count stock, confirm unit sizes and menu demand, use approved supplier systems and require manager approval before orders or menu changes.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general instruction without the final structure, controls or human-review boundary. | The prompt did not define priority rules, physical verification, required information or limits on ordering recommendations. | A readable answer is not automatically reliable or suitable for a business workflow. |
| Final v1.1 | Added item fields, priority definitions, missing-data handling, urgent-action summary, physical verification and manager-approval controls. | The final output applied transparent priorities and replaced the unsupported ordering instruction with verification and management actions. | AI can support inventory decisions only when recorded facts, unknown demand and human purchasing authority are clearly separated. |
