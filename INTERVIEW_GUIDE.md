# Interview Guide

## Brokerage Analytics & Risk Monitoring Platform

**Built by Faisal Fakhouri**

## 30-Second Explanation

> I built a six-page Power BI brokerage analytics project that combines executive reporting, client and account analysis, trading performance, risk monitoring, compliance alerts, and account-level investigation. The key workflow is drill-through: an analyst can identify an account in a management or risk review queue and open a dedicated investigation page where the KPIs and visuals update to that account's context. I structured the project in PBIP format and used Git for version control and iterative development.

## 90-Second Explanation

> The project started from the idea that brokerage data is analyzed across clients, accounts, trades, PnL, risk, drawdown, and alerts. I wanted to connect those areas into a useful workflow rather than create unrelated dashboard pages.
>
> I organized the solution into six pages. Executive Overview provides the high-level picture. Client & Account Analysis looks at segmentation, equity, margin usage, and accounts needing attention. Trading Performance focuses on PnL, volume, win rate, instruments, and direction. Risk Monitoring looks at risk bands, drawdown, margin pressure, and a review queue. Alerts & Compliance analyzes monitoring patterns and investigation records.
>
> The strongest workflow is Account Investigation. From an account row on the client or risk page, the user can drill through using account ID. The investigation page recalculates its KPIs, trends, instrument results, directional PnL, and account details for the selected account. A visible selected-account card makes the context clear.
>
> Technically, I used Power BI, DAX, semantic-model relationships, filter context, PBIP project files, Git, and GitHub.

## Common Questions

### Why six pages instead of one dashboard?

The analytical tasks are different. Executive monitoring, trading analysis, risk review, alert investigation, and account investigation each require different detail. Separating them avoids overcrowding and creates a clearer workflow.

### What is the most important feature?

The account drill-through workflow. It connects portfolio-level monitoring to detailed investigation.

### What did you learn about filter context?

A measure's result depends on filter context reaching it through fields and model relationships. The investigation page works because the selected account filters connected account, trade, performance, and risk data.

### Why not connect every alert table to accounts?

Relationships should reflect actual grain and keys. Adding a relationship only to make a visual filter can introduce ambiguity or incorrect results. I kept alert analysis separate where the model did not justify an account relationship.

### Why use Git?

PBIP exposes report and semantic-model definitions as project files. Git provides checkpoints, change review, rollback, and visible development history.

### What would you improve next?

Automated PBIP validation, a richer data dictionary, period-comparison measures, and a sanitized hosted demo. Alert detail would only be integrated into account investigation after establishing a defensible relationship.

## Presentation Flow

1. Start on Executive Overview.
2. Show Client & Account Analysis and the Management Attention List.
3. Show Trading Performance.
4. Show Risk Monitoring and the Risk Review Queue.
5. Briefly show Alerts & Compliance.
6. Return to an account-level source table.
7. Right-click an account and drill through.
8. Point to the selected-account card.
9. Explain how connected visuals recalculate.
10. Finish with the GitHub repository and PBIP/Git workflow.

## CV Summary

> Built a six-page Power BI brokerage analytics and risk-monitoring platform covering executive KPIs, client/account segmentation, trading performance, account risk, monitoring alerts, and account-level drill-through investigation. Developed reusable DAX measures, interactive filtering, investigation queues, and a source-controlled PBIP workflow using Git and GitHub.

## Author

**Faisal Fakhouri**
