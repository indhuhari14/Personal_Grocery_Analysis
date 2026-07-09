# Grocery Budget vs Actual Spend Analysis

A personal finance mini-project comparing a planned grocery shopping list against actual spend for a single store run, to identify *why* the final bill exceeded the budget — and by how much.

## Background

Before a grocery trip, I prepared a shopping list with estimated prices for each item, totaling **₹4,179**. The actual bill at checkout came to **₹5,667** — an overspend of **₹1,488 (35.6% over budget)**.

Rather than treat this as a one-off surprise, I broke the bill down item-by-item to understand what actually drove the overspend: rising prices on planned items, or items bought that weren't on the list at all.

## Objective

- Quantify the total variance between planned and actual grocery spend
- Separate the overspend into two distinct causes: **price hikes on planned items** vs. **unplanned purchases**
- Identify which product categories contributed most to the overspend
- Turn a everyday personal expense into a structured, repeatable analysis template

## Tools Used

- **Excel** — data structuring, formulas (`SUMIF`, variance %, conditional formatting)
- **Power BI** *(planned next step)* — category and variance visuals for an interactive dashboard

## Data

Each grocery item was logged with:

| Field | Description |
|---|---|
| Item | Product name |
| Category | Spices & Masala, Grains & Pulses, Oil, Cleaning & Household, Personal Care, Others |
| Status | Planned (was on the original list) or Unplanned (bought in-store, not listed) |
| Est. Qty / Actual Qty | Quantity planned vs. quantity bought |
| Est. Price / Actual Price | Planned cost vs. actual cost paid |

43 items were logged in total: 28 planned items and 15 unplanned purchases.

## Approach

1. **Structured the raw list** into a clean table with a consistent category taxonomy and a Planned/Unplanned status flag for every item.
2. **Calculated variance** (₹ and %) per item using formulas rather than static numbers, so the sheet updates automatically if source data changes.
3. **Aggregated by category** using `SUMIF`, to see which category of goods (spices, grains, household items, etc.) drove the largest gap between estimate and actual.
4. **Split the total overspend into two components**:
   - Price variance on items that were planned for (i.e., the item was budgeted, but cost more than expected)
   - Spend on items that had zero budget allocated (i.e., not on the list at all)
5. **Visualized** the split with a bar chart (estimated vs. actual by category) and a pie chart (planned vs. unplanned share of total spend).

## Key Insight

The overspend was **not primarily driven by rising prices**. A meaningful share of the ₹1,488 gap came from items that were never budgeted for in the first place — unplanned, in-store purchases contributed more to the overspend than price increases on the planned list did.

This reframes the problem: the actionable fix isn't "prices are going up" (largely outside personal control), but **impulse/unplanned buying at the store**, which is a behavior that can actually be managed with a stricter list-adherence habit next time.

## Files

- `Grocery_Budget_Analysis.xlsx` — Dashboard, Category Summary, and item-level Data sheets, fully formula-driven

