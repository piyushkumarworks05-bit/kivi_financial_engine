# Kivi Android integration order

Source of truth: `Kivi_Integrated_Financial_Intelligence_v1.zip`, `Kivi_Screen_Contracts_v1.zip`, `Kivi_Personality_and_Roast_Engine.zip`, and the product specification.

## Non-negotiable rules
- Keep the financial engine authoritative; never calculate Safe 2 Spend separately in the UI.
- A manually entered available balance is a snapshot: do not subtract older SMS again.
- Separate real financial data from `demo:` synthetic AA data.
- Never treat unverified recurring charges as confirmed obligations.
- No roast when the user is distressed or a sensitive financial situation is involved.
- Never ship provider secrets in the APK.
- No fake account connection or invented transaction data labeled real.

## Build milestones
1. Android onboarding: salary, payday, available balance, optional SMS permission.
2. Native SMS intake with explicit permission, parsed transaction review, duplicate detection.
3. Ledger updates and authoritative dashboard refresh.
4. Home Safe 2 Spend and explain-why breakdown.
5. Transaction activity, correction, spending analysis and merchant intelligence.
6. Targets, goals, EMIs/BNPL, habits and ghost purchases.
7. Kivi chat, roast receipts, notifications, privacy controls.
8. Synthetic AA demo isolation and optional live AA server integration.
9. End-to-end Android tests, release signing and verified installable APK.

## Acceptance flow
Onboard with salary/day/balance -> import eligible SMS -> review ambiguous messages -> update ledger -> see Safe 2 Spend -> correct one transaction -> verify Home, Activity, Insights and Kivi explanations all update consistently.

Visual direction: warm paper, deep ink, selective pink/lime/gold/violet accents; editorial Indian pop culture, not gaming UI.
