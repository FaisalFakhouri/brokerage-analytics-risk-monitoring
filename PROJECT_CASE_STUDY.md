# Project Case Study

## Brokerage Analytics & Risk Monitoring Platform

**Built by Faisal Fakhouri**

## The Problem

A brokerage-style operation can have information spread across client records, accounts, trades, daily performance, risk scoring, drawdown summaries, and monitoring alerts. Looking at these areas separately makes operational investigation slower and less consistent.

The goal of this project was to design an analytical platform that brings those perspectives together and supports both portfolio-level monitoring and account-level investigation.

## Objectives

- Provide a concise executive view of brokerage activity.
- Analyze client and account composition.
- Evaluate trading performance by time, instrument, and direction.
- Surface account risk, drawdown, and margin pressure.
- Review monitoring and compliance alert patterns.
- Allow analysts to move from a flagged account to a focused investigation page.

## The Six-Page Solution

### Executive Overview

The opening page summarizes client activity, trade activity, trading volume, trading PnL, high-risk accounts, regional distribution, instrument activity, risk-band distribution, and PnL trend.

### Client & Account Analysis

This page covers client segmentation, account type and status, net client flow, regional equity, margin usage, and a Management Attention List. The attention list also serves as an entry point into account-level drill-through analysis.

### Trading Performance

This page examines total trades, trading volume, net trading PnL, win rate, average trade PnL, PnL over time, instrument PnL, instrument volume, win rate by instrument, trade-direction performance, and detailed instrument results.

### Risk Monitoring

This page combines high-risk and critical-risk account counts, average risk score, worst drawdown, total equity, margin usage, risk-band distribution, equity versus risk score, margin pressure, drawdown by account type, regional/segment exposure, and a Risk Review Queue.

### Alerts & Compliance

This page examines monitoring alert counts, severity, rule categories, payment methods, client concentration, rapid-withdrawal timing, and detailed unusual-amount investigation records.

### Account Investigation

The Account Investigation page is the central workflow feature. A user can drill through from an account-level source table to a dedicated page filtered to the selected account.

The page provides selected-account context, equity, account PnL, margin usage, risk score, drawdown, total trades, PnL trend, instrument PnL, volume by instrument, PnL by trade direction, equity versus margin usage, and detailed account review information.

## Important Design Decisions

### Separate analytical pages

Executive monitoring, trading analysis, risk review, alert investigation, and account investigation require different levels of detail. Separating them creates clearer analytical focus.

### Drill-through instead of duplicated detail

The account investigation workflow avoids repeating detailed account visuals across several pages. Source pages identify an account; the investigation page handles focused analysis.

### Relationship safety

The project avoids introducing unsupported relationships simply to make every dataset filter every page. Alert structures are not forced into account drill-through behavior where the model does not justify that relationship.

### Visible context

The investigation page displays selected-account context so users can see whether they are viewing one account or a broader context.

## Development Process

1. Build the analytical model and initial report pages.
2. Create and refine KPI measures.
3. Improve page structure, slicers, titles, and formatting.
4. Add account-level drill-through.
5. Validate drill-through from account and risk review tables.
6. Improve the investigation page with explicit account context.
7. Replace a weak single-account risk-band visual with directional PnL analysis.
8. Maintain Git checkpoints for rollback and change review.
9. Prepare the repository for portfolio presentation.

## Skills Demonstrated

- Translating business questions into analytical pages
- Multi-page Power BI report design
- DAX KPI development
- Filter context and relationship reasoning
- Drill-through workflow design
- Monitoring and investigation queues
- PBIP source control with Git and GitHub
- Iterative usability and presentation improvement

## Future Improvements

- Add a formal data dictionary.
- Add automated PBIP validation in CI.
- Expand alert-to-account analysis if a defensible relationship becomes available.
- Add richer period-comparison measures.
- Add scenario-specific risk thresholds.
- Publish a sanitized hosted demonstration if an appropriate environment is available.

## Conclusion

The project's central strength is the connection between high-level monitoring and account-level investigation.

**Author: Faisal Fakhouri**
