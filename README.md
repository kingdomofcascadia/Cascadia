# Kingdom of Cascadia — Community Platform Prototype

An interactive React/Vite frontend demonstrating Cascadian Realms, a social feed, demo marketplace, citizenship membership flow, and proposed CDD wallet.

## Run

```bash
npm install
npm run dev
```

Open the local URL shown by Vite. For a production bundle, run `npm run build`.

## Current limitations

- This is a **frontend prototype**. All data is temporary in browser memory and resets on refresh.
- No real authentication, subscriptions, SMS, ID verification, marketplace payment processing, or banking is connected.
- CDD is **not issued**, redeemable, backed by reserves, or tradeable. The wallet displays zero and disables money actions.
- Realm chat is a local interface demonstration, not a multi-user real-time service.

## Production implementation plan

1. Add PostgreSQL + Supabase Auth, Row Level Security, email verification, account recovery and session management.
2. Implement Realm, channel, message, role, invitation and moderation tables with enforced server-side permissions and realtime subscriptions.
3. Implement Stripe Billing subscriptions, Stripe Identity (subject to account and regional eligibility), an SMS verification service, verified webhooks, cancellation handling and least-privilege ID data handling.
4. Implement marketplace seller onboarding with Stripe Connect, Checkout, order records, webhook-driven payment confirmation, refunds, disputes and payout reporting.
5. Select a compliant CAD stablecoin issuer / banking partner and obtain Canadian legal review of applicable payment, securities, AML, custody and reserve requirements before live CDD issuance or trading. Use audited contracts, custody and redemption controls, independent reserve reporting, transaction reconciliation, and an authorized on/off-ramp.
6. Deploy in staging with automated tests, monitoring, backups, fraud controls and security review before any production launch.

Do not put Stripe secret keys or private wallet keys into browser code. Do not represent membership as government citizenship or immigration status.
