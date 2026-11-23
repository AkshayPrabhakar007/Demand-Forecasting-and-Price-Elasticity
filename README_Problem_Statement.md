# Data Science Specialist — Take-Home Assignment

## Scenario

You are a data scientist supporting a product line sold across six sales
regions. The commercial team wants to understand what drives demand and how to
price for the upcoming quarter. You have ~4 years of monthly history in
`demand_panel.csv`.

Each row is one region in one month:

| Column | Description |
|---|---|
| `date` | Month (first of month) |
| `region` | Sales region |
| `price_usd_per_ton` | Our average selling price |
| `competitor_price_usd_per_ton` | Competitor average price |
| `promo_flag` | 1 if a promotion ran that month, else 0 |
| `industrial_index` | Industrial-production index (demand driver, base 100) |
| `demand_tons` | Units sold (the quantity of interest) |
| `monthly_capacity_tons` | Plant capacity ceiling for that region/month |

> The data is real-world-messy. Part of the exercise is noticing and handling
> that. Document any assumptions you make.

## What we'd like you to do

1. **Prepare the data.** Clean and harmonize the panel; engineer features you
   think are useful. Briefly explain your choices.
2. **Forecast demand.** Build a model to forecast monthly `demand_tons` by
   region. Validate it honestly (respect time ordering) and compare against a
   simple baseline. Report your error metric and why you chose it.
3. **Estimate price sensitivity.** Quantify the own-price elasticity of demand
   and interpret it for a commercial stakeholder. Account for the panel
   structure (multiple regions over time).
4. **Make a pricing recommendation.** Given a variable cost of **$600/ton** and
   the capacity ceiling, recommend a price per region that improves
   contribution margin. State your reasoning and any caveats.
5. **Communicate.** Write a short summary (≤1 page) of your recommendation for a
   non-technical commercial leader.

We care more about sound reasoning, honest validation, and clear communication
than about squeezing out the last point of accuracy. If a simpler method is the
right call, use it and say why.

## Constraints

- **Language:** Python or R.
- **Time:** aim for ~4–6 focused hours. Don't gold-plate.
- You may use any standard open-source libraries.

## Deliverables

- Your **code**, runnable top to bottom, with a short `README` explaining how to
  run it and what each part does.
- Your **1-page summary** (Markdown or PDF).
- Note any assumptions and anything you'd do with more time.

## How to submit

1. Create a **private Git repository** (GitHub or Azure DevOps).
2. Commit your work in logical steps — we review commit history as well as the
   final state.
3. Share the private repo with the reviewers listed in your email.

## How we evaluate

| Area | What we look for |
|---|---|
| Data handling | Catches messiness (missing values, outliers, inconsistent labels, duplicates); sensible feature engineering |
| Validation rigor | Time-aware split (no leakage); baseline comparison; appropriate metric |
| Modeling judgment | Right-sized method; justifies model choice over fancier alternatives |
| Econometric reasoning | Correct elasticity estimate and interpretation; accounts for panel structure / confounders |
| Optimization & business sense | Coherent pricing recommendation; respects capacity; flags extrapolation risk |
| Communication | Clear, honest, stakeholder-appropriate write-up; clean, readable repo |
