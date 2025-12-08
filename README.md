# beverage-ops-batching-and-costing
Cocktail costing &amp; batch planning (kegs and large format containers) with inventory module integration.
# Bar Operations — Cocktail Batching & Costing

A practical workbook for cocktail recipe costing and batch planning across single-serve and large-format containers. 
Focus: per-serve cost and margin, dilution, transfer loss, container presets, automatic scaling (servings/volume/container), and clean Tableau exports.

## Quick start
1. Download `Fairways_FINAL_USER.xlsx` (or open in Google Sheets).
2. Fill **Ingredient Library** (names, category, vendor, bottle size value + unit, bottle cost).
3. Enter recipes in **Recipe Builder** (one row per ingredient; optional Glassware).
4. In **Cocktail Summary**, type a cocktail name in column A and enter **Price per Serve $** to see margin.
5. Use **Batch Calc** to scale by **Servings / Volume / Container** (handles dilution, transfer loss, headspace).
6. (Optional) Use **Batch Export** or **DataReady** sheets when publishing to Tableau.

## Sheets overview
| Sheet | What it’s for |
|---|---|
| Sheet_Map | Click to navigate. |
| Ingredient Library | Master list; unit-aware bottle sizes (ml/oz → oz) and costs. |
| Recipe Builder | One row per ingredient per cocktail; auto line cost; **Glassware** note column. |
| Cocktail Summary | Totals per serve: **Total oz**, **Cost per Serve $**, **Price per Serve $** → **Margins**. |
| Batch Calc | Human-friendly inputs (dropdowns for cocktail, batch type, container). Shows volumes, servings, cost, water add. |
| Batch Export | KPI block + scaled ingredient list for the active batch (Tableau-ready). |
| QC Log | Simple check log (Check Date, Cocktail, Container, Batch Type, Status, Notes). |
| Reference | All lookups in one place: **Ingredient Categories, Vendors, Container sizes**. |
| DataReady_* | Hidden tidy tables for Tableau (no editing needed). |

## Batch Calc (how to use)
1. Pick **Cocktail**.
2. Choose **Batch Type** (Partial = without added water; Complete = includes dilution water).
3. Choose **Target Method** (Servings / Volume / Container) and enter the target.
4. Set **Dilution %**, **Transfer Loss %**, **Headspace oz** as needed.
5. Read the results: **Net Target Volume**, **Pre-loss Volume**, **Base (before dilution)**, **Servings**, **Total Ingredient Cost**, **Water Addition**.

## Tableau
- Connect to **Batch Export** or the **DataReady_*** sheets.
- Publish 2–3 visuals: Cost vs Price (margin), Batch KPI panel, simple QC timeline.
- Tableau Public link: 

## Reuse & credit (optional)
Licensed under **CC BY 4.0**. Please credit this repo if you reuse or adapt the workbook or docs.
