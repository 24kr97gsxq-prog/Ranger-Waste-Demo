# RANGER DISPATCH — MASTER TO-DO (priority-ordered)

**Last updated: Tuesday, August 18, 2026 — v3.1.**
Update the date whenever you change something.

**v3.1 additions:** Ranger's real DivertScan reports reviewed (3 LEED projects,
28 tickets, ~104 T YTD through Dalmex — real data stays OUT of the public demo).
The DivertScan bridge is now quantified, not hypothetical: 28 times this year a
Ranger driver crossed the Dalmex scale and the tonnage landed in DivertScan;
in the new system that same driver would be typing it into a phone. The bridge
kills that double entry and prefills the tipping fee. Still API-only, still
LATER. Ranger's range reaches Sherman (60+ mi north) — sharpens the
offline/dead-zone discovery question. **Pitch line: Ranger already runs part
of its business on Robert's software every month (DivertScan reports they hand
their own customers) — Robert is not an unknown vendor.** Demo gained a
DivertScan cross-sell teaser on Reports (fake data; LEED reporting stays
DivertScan's job, full stop). **Jaguar also runs Box Tracker** — a second
prospect for the same product: (a) validates tenant-ready schema, (b)
per-tenant 10DLC brand/campaign = recurring cost PER hauler, (c) hard
confidentiality wall — Ranger's pricing, data, and demo never shown to Jaguar
or vice versa; Jaguar gets its own skin (brand variables already support a
repaint), (d) the EULA don't-log-in rule applies at Jaguar too. Do NOT pitch
Jaguar until Ranger is signed — one live reference beats two prospects.

**Status:** Demo built (5 screens, Ranger-branded, on GitHub). Scope settled:
**dispatch replacement, not full Box Tracker replacement.** Robert is charging;
Ranger's owner knows and will pay for something decent. Amount not agreed.
No discovery call yet. No Supabase project. No 10DLC started.

**Changed since v2:** scope decision (billing engine OUT, CSV handoff stays);
Box Tracker's real pricing verified from their own calculator; EULA read —
migration and conduct constraints identified; competitor landscape mapped;
feature synthesis reviewed and triaged; Ranger confirmed as roll-off open
tops + compactor rentals, no other service lines.

---

## 🎯 SCOPE (settled — resist re-opening)
**Build:** order intake, dispatch board, driver app (EN/ES), container +
compactor tracking, customer request link, event-driven texting, CSV export
to QuickBooks.
**Explicitly OUT:** invoicing engine, double-entry accounting, card
processing, rate-sheet billing. Ranger bills wherever they bill today; we
hand them clean data. (Revisit only if Ranger asks and pays for it as a
separate phase — see PCI note below.)
**Why this shape:** portal/texting/tracking only stay accurate if our system
is where work gets entered. Dispatch replacement makes the rest free
byproducts. Double entry across two systems dies by week three.

## 🥇 THE PITCH (one line, verified)
Box Tracker charges **$0.20 per text** (their calculator). Wholesale via
Twilio is ~$0.013 all-in. At ~1,300 texts/month Ranger would pay Box Tracker
~$260 vs ~$17 at cost. **The texting spread alone can fund the entire
subscription.** Lead with this.

## 💵 BOX TRACKER — VERIFIED ECONOMICS (their cost calculator, Aug 2026)
| Item | Price |
|---|---|
| Setup | $250 base + $150/template (5 templates) = $1,000 max |
| Fleet fee | **$1.95 per dumpster owned / month** (not $0.50 — that figure is wrong and keeps resurfacing; kill it wherever it appears) |
| Text messages | **$0.20 each**, billed in arrears |
| Web API access | **$200 / month** |
| Support, training, extra users | Free |

At a 40–60 can fleet: ~$80–120/mo before texting. Ranger's actual bill may be
grandfathered/negotiated — **ask to see a real invoice.** It also reveals
their fleet count and text volume in one document.

Unverified claims to stop repeating: "QuickBooks sync" (nothing on their site
supports it; they sell their own accounting suite), "automated SMS" (their
automated messages are email; texting is person-to-person), "4.5–5.0 stars"
(Capterra = 5.0 from **two** reviews).

## ⚖️ EULA CONSTRAINTS (Cairn's, effective Jan 2023 — lawyer should confirm)
- **Robert never logs into Ranger's Box Tracker.** No credentials, no
  keyboard, no screenshots. The license bars using the Software to compete
  and bars disclosing its contents. Observe the dispatcher working; take
  notes in your own words.
- **Extract before cancelling, never after.** Cairn may suspend access at any
  time and owes no data preservation on termination. All data comes out while
  the account is live and paid. 7-day notice to cancel; $100 reinstatement.
- Scripting their web UI = breach. API (at $200/mo) is the only sanctioned
  automation route. Only worth it briefly for migration, if at all.
- Ranger should not email Cairn feature ideas (unsolicited ideas become
  Cairn's property).
- Their liability cap is **$50 total**. Mention to Ranger once. Copy the
  concept: Robert's own agreement needs a liability cap too.

## 🏁 COMPETITIVE LANDSCAPE (pricing unverified — leads, not facts)
Docket (~$39–55/mo + add-ons, booking widgets, native driver apps), DRS
($80–280/mo tiers, D2C e-commerce), CurbWaste (enterprise, OCR + geofencing +
overage automation), Roll-Off Amigo ($0–99/mo, **bilingual**), CRO
(multi-line — not our market).
- [ ] Verify competitor pricing against live pages before quoting anyone.
- [ ] **Answer this before pricing: why does Ranger pay Robert instead of
      moving to Docket at $55/mo?** Candidate answers: compactors (absent
      from every competitor's pitch), a system shaped to their exact yard,
      and Robert being local + accountable. The answer must exist in writing.

## 🛑 IMMEDIATE
- [ ] Verify repo separation at the GitHub level (DivertScan's `main`
      auto-deploys to a live site).
- [ ] Get a real Box Tracker invoice from Ranger.
- [ ] Discovery call — walk the demo's "What we guessed" panel with the
      dispatcher. Questions list from v2 still stands (operation size,
      workflow, compactor triggers, dead zones, phones, who invoices, 15 yd
      allowance, cutover overlap).
- [ ] **Decide: system-for-Ranger vs product-for-haulers.** Not urgent, BUT:
- [ ] **Build tenant-ready regardless** — org ID on every table, RLS scoped
      to it, from the first migration. Costs ~nothing now, brutal to
      retrofit. Non-negotiable at Supabase project creation.

## 🟢 PHASE 0 — setup
- [x] GitHub repo (verify separation above).
- [ ] Supabase project — separate from DivertScan, Pro tier ($25/mo; free
      tier pauses after 7 idle days), tenant-ready schema, RLS day one.
- [ ] Start A2P 10DLC now: ~$4–48 brand + ~$15 campaign vetting +
      $1.50–10/mo. 1–3 week approval; the long pole. If Ranger currently
      texts via Box Tracker, a move means a NEW number — old number goes
      dead for customers who saved it. Plan the notice.
- [ ] Robert's service agreement: liability cap, support window, data
      ownership + exit terms, SMS as pass-through or padded flat rate.
      Accountant/lawyer review.

## 💸 RECURRING COSTS (Robert's floor, verified Aug 2026)
Supabase Pro $25 · hosting $0–20 · Twilio number + campaign $3–11 · SMS
volume $15–30 · map tiles $0–25 (OSM free but not production-appropriate;
Google/Mapbox per-load) · domain ~$1. **Hard floor ≈ $50–90/mo.** Price the
6am-when-the-board-is-down responsibility, not the servers. Structure: staged
build fee + flat monthly. Not per-truck (numbers too small at 2–3 trucks).

## 🟡 PHASE 1 — dispatch core
- [ ] Data model: customers, sites, containers, **compactors** (separate
      asset class: unit fixed, receiver box moves, no dwell clock), orders,
      assignments, drivers. All tenant-scoped.
- [ ] Order intake (dispatcher-typed; right-size warning at entry — concrete
      into a 30 yd = overweight can, blocked before it's ordered).
- [ ] Dispatch board; 4 PM same-day cutoff with dispatcher override (their
      promise, operationalized — but a 4:20 call from a good customer must
      be squeezable).
- [ ] Driver app EN/ES: advance status, photo, note, net tons, dry run.
- [ ] **Driver confirms OCR'd or typed weights on screen; photo of scale
      ticket attached as evidence.** OCR proposes, human confirms, fails safe.
- [ ] **Tipping fee capture** (what Ranger PAID at the facility — distinct
      from tons hauled; it's the cost side of gross profit). Box Tracker has
      it; we must too.
- [ ] **Site condition notes that persist per site** ("low power line") and
      warn the next driver. Stolen from Box Tracker Driver; cheap; safety.
- [ ] **Tap-to-call** the customer from the stop.
- [ ] **Geofenced drop logging** — phone GPS + photo at status change. Free
      hardware-wise; kills "where's my can" disputes. This IS the tracking
      feature; GPS pucks on cans stay a priced add-on, later.
- [ ] Container inventory derived from order history; turnover + idle-days
      reporting (the number this market buys on — Box Tracker's whole
      homepage is turnover).

## 🔵 PHASE 2 — customer-facing + money-makers
- [ ] Tokenized customer link (no login). Compactor customers get "it's
      full — come get it."
- [ ] Dispatcher approves/declines every request.
- [ ] Notification engine (stubbed until 10DLC clears; log would-be sends):
      confirmation → en route → complete.
- [ ] **Day-6 free-days text**: "7 days up tomorrow — extend or pick up?"
      Turns silent $20/days into agreed billable ones. Highest-ROI feature.
- [ ] **Morning-of dry-run prevention text**: "coming today — access clear?"
      Two prevented dry runs/month ≈ the subscription.
- [ ] Overage surfaced from captured tonnage → flows into CSV export.
- [ ] **Monthly leakage report**: dry runs prevented, extra days billed, tons
      over allowance, dollars recovered. The app proving its own value =
      Robert's renewal conversation.
- [ ] CSV export to QuickBooks (working in demo; carries rates when Ranger's
      sheet exists).

## 🔴 LATER / MAYBE / DECLINED
- [ ] Web storefront with card capture — only via Stripe/Square hosted flow
      (stays out of PCI scope). Card-on-file overage charging: capture yes,
      **auto-charge no** — queue for human approval. Same rule for any future
      invoice push: driver tap ≠ ledger entry without review.
- [ ] Offline driver mode — decides itself at discovery (dead zones?). Box
      Tracker is web-only too; first to solve offline wins that argument.
- [ ] GPS hardware on cans ($50–200/unit + $5–40/mo each) — optional add-on,
      priced separately, never v1.
- [ ] Compactor fill monitors — same recurring-cost shape; ask if any exist.
- [ ] Route optimization; two-way texting; DivertScan bridge (API only,
      never shared DB).
- ~~Multi-line board (septic/portajohns)~~ — Ranger is roll-off + compactors
  only. Confirmed. CRO's market, not ours.
- ~~Box Tracker companion product~~ — dead: $200/mo API fee + strategy change.
- ~~Live QuickBooks Online sync~~ — CSV chosen; avoids Intuit review gate.

## ⛔ HARD RULES (unchanged)
- Nothing touches DivertScan repo, database, or the Pi. Ever.
- No credentials in code/chat/repo. No real customer phone numbers in test
  data. (Ranger's published business number/address in the demo = fine.)
- Real dispatcher/driver in front of it → DivertScan discipline: backup,
  branch + PR, verify each deploy.

## 📋 DEMO STATUS (unchanged from v2 except brand)
5 screens; real brand colors (#1C1D2A / #F38C4C / #181925 / #F3B48F /
#F9F9FB / #525665; dark text on orange for contrast). Working: full dispatch
flow, compactor hauls, EN/ES, map, cutoff clock, CSV. Placeholder: all
addresses/customers, fill %, Dallas-market dollar figures. "What we guessed"
panel = discovery agenda.
