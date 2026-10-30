---
tags: [project, sentri, ai]
updated: 2026-10-30
---
# Sentri Automation (Claude + Notion + Quo)

The system that makes me the highest-throughput coordinator.

## Daily Job Loop (scheduled tasks)
- **7:00am:** cross-references the Notion Service Pipeline + Quo (missed calls, texts, the B2B line, existing tasks) → **top-10 priorities as separate Quo tasks**, staggered 45 min from 8:30, mirrored to Google Calendar
- **5:00pm:** texts me (435-212-1100) a check-in, logs a "Daily Status" Quo task that the next morning's run reads. A continuous loop
- Always uses the "Bryan's Number" inbox. If Quo needs a reconnect, push-notify and stop
- Known issues: the 7am trigger **double-fires** some mornings (10/28, 10/29, 10/30), and Quo/Notion sometimes disconnect

## Handbook & Rollout
- Steven wants the whole team on it. Plan narrowed to **coordinators/fulfillment first**
- Pitch: a two-week pilot with one other coordinator, then before/after numbers
- Key point: it catches the *cross-system* misses (materials landing after the contractor start, a sub's quote above the sold price, a permit nobody pulled)
- Risk: it depends on clean Notion data

## Other Builds
- **Sub-finder tool**: pull licensed-contractor rosters by state (CA, MI, OH, NY, AZ), filter by trade/county/active → call lists
- **Sentri Job Margin Tracker**: React + Vite localhost app, per-job phase margins (seeded with the Dowling kitchen)
- **Commission tracker**: 5% on Job Complete. Monthly earnings alternate between lower and higher months
- Materials list generator (Claude Code), Notion job tracker → Discord webhooks
- Retell AI voice agent for automated calls (in setup)
- Wants Claude to eventually handle all contractor/homeowner comms through Quo

Related: [[Sentri/Sentri Homes]] · [[Knowledge/Tools & AI Stack]]
