# Excel Business Tools Portfolio

A portfolio of practical Excel tools designed to support business decisions, organize operational work, and test different scenarios.

Unlike my Power BI projects, which focus on interactive reporting and data exploration, this portfolio focuses on spreadsheet tools that users can work with directly: entering information, changing assumptions, checking results, and evaluating alternatives.

## Portfolio Overview

| Project | Business Question | Planned Excel Features | Status |
|---|---|---|---|
| Pricing and Break-Even Calculator | How do price, costs, and sales volume affect profitability? | Formulas, input validation, conditional formatting, What-If Analysis | Planned |
| Invoice and Payment Tracker | Which invoices remain unpaid, and which require follow-up? | Excel Tables, date formulas, SUMIFS, validation, aging analysis | Planned |
| Resource-Allocation Planner | How can limited working hours and budget be allocated across tasks? | Formula-based modeling, constraints, Solver, scenario comparison | Planned |

Project statuses will be updated as work progresses. Features listed above describe the intended scope, not completed functionality.

## 01 — Pricing and Break-Even Calculator

### Business Problem

A small business needs to understand how its selling price, costs, and expected sales volume affect profit.

### Planned Solution

An Excel calculator that allows users to change assumptions and immediately see the resulting financial estimates.

### User Inputs

- Selling price per unit
- Variable cost per unit
- Monthly fixed costs
- Expected monthly sales volume

### Planned Outputs

- Estimated revenue
- Total variable costs
- Total costs
- Contribution margin per unit
- Estimated profit or loss
- Break-even sales volume
- Comparison of conservative, base, and optimistic scenarios

### Validation Plan

- Check that required inputs are provided.
- Flag negative costs or sales volumes.
- Flag cases where selling price does not exceed variable cost.
- Compare formula results against manually calculated test cases.
- Distinguish theoretical break-even volume from whole-unit sales requirements.

### Model Assumptions

The initial version will model one product over one reporting period. It will assume constant selling price, constant variable cost per unit, and fixed costs within the modeled range.

## 02 — Invoice and Payment Tracker

### Business Problem

A business needs a consistent way to monitor unpaid invoices and identify payments requiring follow-up.

### Planned Solution

An Excel tracker that calculates outstanding balances, classifies invoice status, and summarizes overdue amounts.

### Planned Data Fields

- Invoice ID
- Customer
- Invoice date
- Due date
- Invoice amount
- Amount paid

### Planned Outputs

- Outstanding balance
- Payment status
- Days overdue
- Aging category
- Total outstanding amount
- Total overdue amount

### Validation Plan

Test the workbook with:

- Fully paid invoices
- Unpaid invoices that are not yet due
- Overdue invoices
- Partially paid invoices
- Invoices due on the reporting date
- Duplicate invoice IDs
- Missing required values
- Due dates earlier than invoice dates
- Payments greater than invoice amounts

A configurable reporting date will make test results reproducible.

### Scope

The initial version will track cumulative payments for each invoice. A separate payment-transaction table may be added later if individual payment histories are needed.

## 03 — Resource-Allocation Planner

### Business Problem

A small team needs to allocate limited working hours across required tasks while respecting availability and budget constraints.

### Planned Solution

An Excel model that compares allocations and uses Solver to search for a solution under explicitly defined constraints.

### Planned Inputs

- Tasks and required working hours
- Team-member availability
- Hourly costs
- Task eligibility, where relevant
- Budget limit

### Planned Outputs

- Allocated hours by task and team member
- Total planned cost
- Remaining capacity
- Unmet task requirements
- Constraint checks

### Initial Optimization Objective

Minimize total staffing cost while meeting required task hours and respecting team-member availability and eligibility.

### Validation Plan

- Confirm that allocated hours do not exceed availability.
- Confirm that required task hours are covered.
- Check that ineligible assignments are excluded.
- Reconcile total hours and costs.
- Test both feasible and infeasible scenarios.
- Document whether hours can be fractional.

### Limitations

The result will depend on the assumptions and constraints included in the model. It will not automatically account for factors such as fatigue, changing priorities, or differences in work quality.

## Data and Assumptions

These projects will use synthetic data and illustrative business assumptions.

They will not contain real customer, employee, or
