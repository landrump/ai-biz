# Listinglever Agent Orchestration Guide

This guide explains the process flow shown in
[`listinglever-agent-orchestration.svg`](listinglever-agent-orchestration.svg).

Status legend:

- **Green / Ready** - Agent can operate now or the setup item is complete.
- **Yellow / Needs work** - Partially ready, but needs account fields, product
  shells, access, or creative production.
- **Red / Blocked** - Cannot run until the user completes setup or live market
  data exists.
- **Blue / Draft** - Designed, but intentionally waiting for signal before use.

## System overview

The Listinglever system has four layers:

1. **Owner inputs** - Accounts, credentials, payments, approvals, and legal/tax
   setup that only the user can complete.
2. **Strategy and orchestration** - The Official AI Biz Agent and Marketing
   Orchestrator decide the next business objective and assign work.
3. **Production and distribution agents** - Specialist agents create products,
   listings, visuals, content, email flows, and channel assets.
4. **Market loop** - Publish, measure, diagnose, and improve.

## Step-by-step flow

| Step | Status | Agent / owner | Inputs | What happens | Outputs |
| --- | --- | --- | --- | --- | --- |
| Owner inputs | Mixed | User | Domain, email, Etsy, Gumroad, Pinterest, file access, approvals | User completes setup that requires identity, payment, account ownership, or sensitive credentials. | Access, accounts, approvals, product shells, publish permissions |
| 1. Market Intel | Ready | Market Intelligence Agent | Niche, constraints, buyer, budget, research links | Evaluates buyer pain, marketplace evidence, competition, risks, and founder-fit. | Demand signals, risks, positioning hypotheses |
| 2. Offer Builder | Ready | Offer Builder Agent | Buyer pain, demand signals, product model | Converts opportunities into workflow-kit products and bundles. | Product briefs, manuscripts, lead magnets, product ladder |
| 3. Creative Production | Ready | Creative Production Agent | Offer, platform specs, brand style, image tools | Creates AI-first image prompts and visual specs for thumbnails, covers, pins, and landing assets. | Creative briefs, prompt packs, visual variants |
| 4. Marketplace SEO | Needs work | Marketplace SEO Agent | Etsy/Gumroad setup fields, titles, tags, product files | Turns product copy into platform-ready titles, tags, descriptions, FAQs, and listing tests. | Upload-ready listings and search/conversion variants |
| 5. Content Engine | Needs work | Content Engine Agent | Product hooks, audience, channel plan | Produces Pinterest pins, short posts, blog/SEO drafts, and repurposed content. | Organic traffic queue |
| 6. Email Lifecycle | Needs work | Email Lifecycle Agent | Gumroad account, free checklist, buyer products, email access | Builds welcome, delivery, nurture, buyer onboarding, and upsell flows. | Email sequences and automation instructions |
| 7. Publish | Blocked | Launch Operations Agent + user | Product shells, product files, images, account access, approvals | Publishes Etsy/Gumroad/Pinterest assets when account setup and approvals are complete. | Live purchase pages and pins |
| 8. Measure | Blocked | Analytics Growth Agent | Etsy, Gumroad, Pinterest, email, ad metrics | Reads impressions, clicks, saves, carts, sales, downloads, replies, and conversion bottlenecks. | Performance readout and next decision |
| 9. Iterate / Scale | Draft | Marketing Orchestrator + specialist agents | Metrics, customer feedback, bottleneck diagnosis | Improves thumbnails, titles, pricing, offers, pin angles, email flows, outreach, partnerships, or ads. | Next test, scale/pause/pivot decision |

## Current state

### Ready / running

- Business model and positioning.
- Agent stack.
- Product manuscripts.
- Gumroad copy.
- Etsy/Gumroad/Pinterest copy banks.
- Customer support and policy drafts.
- AI-first creative production plan.
- Gumroad profile and production email setup are recorded.

### Needs work

- Gumroad product shells.
- Etsy shop/listing completion.
- AI-generated production visuals.
- Pinterest business account and boards.
- Email automation configuration.
- File handoff/write access if direct upload is desired.

### Blocked

- Publishing until product shells, upload files/images, account setup, and final
  approvals are complete.
- Measurement until purchase pages/pins are live and traffic exists.

### Draft / later

- Paid acquisition.
- Outbound sales.
- Partnerships.
- Founder-edge alternative niche expansion.

These should wait until the first launch assets are credible or there is a
specific validation reason to use them earlier.

## Inputs the user owns

The user owns:

- Account creation and identity verification.
- Payout, tax, business, and payment setup.
- Passwords, API keys, and OAuth authorization.
- Final approval of public claims, prices, and refund policies.
- Any paid spend budget.
- Any decision to run outbound campaigns using personal or business contact
  data.

## Work the agents own

The agents own:

- Research and evidence gathering.
- Product strategy and offer creation.
- Product manuscripts and lead magnets.
- Marketplace copy.
- Visual briefs and AI image prompts.
- Organic content queues.
- Email sequences.
- Support macros and policy drafts.
- Metrics trackers.
- Performance diagnosis and next-test recommendations.

## Operating loop

```text
Objective -> Inputs -> Agent production -> Publish -> Measure -> Diagnose -> Improve
```

If there is no live data, the system keeps advancing launch assets until it
reaches an owner-only blocker.

If there is live data, the system stops guessing and improves the highest-impact
bottleneck:

- No impressions: fix distribution and keywords.
- Impressions but no clicks: fix title, thumbnail, hook, first image.
- Clicks but no carts: fix offer clarity, preview, proof, trust, price.
- Carts but no sales: fix price, urgency, bundle, FAQs, checkout confidence.
- Sales but weak average order value: improve bundle and upsell path.

## Next unlocks shown on the slide

1. Create Gumroad product shells.
2. Finish Etsy shop/listing setup.
3. Create Pinterest Business account.
4. Generate production visuals from the AI-first creative plan.
5. Publish and collect live metrics.

