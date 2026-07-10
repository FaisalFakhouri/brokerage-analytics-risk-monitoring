# Technical Overview

**Project:** Brokerage Analytics & Risk Monitoring Platform  
**Author:** Faisal Fakhouri

## Technology

- Microsoft Power BI Desktop
- Power BI Project (`.pbip`) format
- DAX
- Semantic model definitions
- PBIR/report definition files
- Git and GitHub

## Architecture

```text
Brokerage Analysis Main.pbip
Brokerage Analysis Main.Report/
Brokerage Analysis Main.SemanticModel/
```

The report and semantic model are represented separately, making the project suitable for source control and iterative development.

## Analytical Domains

The model supports clients, accounts, trades, account performance, daily performance, account risk scores, drawdown summaries, instruments, transactions, monitoring/alert datasets, and KPI measures.

## Measure Layer

A dedicated KPI measure layer supports reusable logic for client and account counts, active-client analysis, trading activity, volume, PnL, win rate, average trade PnL, equity, account PnL, margin usage, risk scoring, drawdown, monitoring metrics, and selected-account context.

## Drill-through Architecture

The Account Investigation page is configured around:

```text
accounts[account_id]
```

Workflow:

```text
Source account row
        ↓
Drill-through on account_id
        ↓
Account Investigation
        ↓
Connected KPIs and visuals recalculate
```

This design reuses the semantic model rather than creating separate pages for individual accounts.

## Relationship Approach

The project preserves valid model relationships and avoids speculative relationship changes. Core account, trading, performance, and risk analysis uses established model paths. Alert structures without a safe active account relationship are not forced into the investigation workflow.

The principle is simple: visual convenience should not override model correctness.

## Validation Approach

Development checks included:

- JSON parsing validation
- Reference checks between report visuals and model fields/measures
- Page order and active-page validation
- Layout bounds checks
- Drill-through field checks
- Git diff/status review before commits
- Manual Power BI Desktop testing of slicers and drill-through behavior

Runtime behavior was manually tested in Power BI Desktop, including account drill-through from account and risk pages.

## Source Control Approach

Git was used to track report-definition changes, preserve stable checkpoints, review modifications, separate meaningful project changes from local Power BI cache/settings artifacts, support rollback, and maintain a visible development history.

## Scope Boundaries

- This is a portfolio demonstration project.
- The documentation does not claim production deployment.
- Alert datasets are not represented as account-connected where the model does not support that relationship.
- The focus is analytical workflow, report engineering, and BI design.

## Author

Designed and built by **Faisal Fakhouri**.
