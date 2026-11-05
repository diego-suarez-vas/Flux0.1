# Flux: product context for UX design

Purpose: general context so designers and AI tools understand what Flux is and what good design means here. It is not a spec. Flux is in ideation and development, so many details are still open. When a detail is missing, ask. Do not invent it.

Last reviewed: 2026-11-05, from Confluence (sources at the end).

## 1. What Flux is
Flux (formerly Central Platform, "CP") is an insight-driven experience that helps dairy teams save time and find opportunities in their operation. It is not a standalone product with one launch date. It evolves the current VAS portfolio step by step (PULSE, DairyComp 305, FeedComp, mobile). Over time, daily activity moves toward Flux's web and mobile experiences, without forced migration.

North star: become the trusted decision-making platform for dairy.

Core loop: **Data → Insight → Task → Action → Outcome.**
Flux does not copy existing reports into the cloud. It shows what needs attention, explains why it matters, and makes the next step clear.

Guiding question for every design: *Does this help the user understand something important sooner, and make the next step clearer?*

## 2. Who it is for
| Persona | Examples | What they need |
|---|---|---|
| **Owner or manager** | Owner, herd manager, repro manager, herd health manager, parlor manager | A clear view of performance and profit. Know what needs attention. Move from a herd-level trend to the animals, tasks or people behind it. Coordinate work and check that protocols are followed. |
| **Worker** | Herd, calf care, maternity or hospital technician | Simple workflows where the next task is obvious. Fast, accurate event entry next to the animal. Works for different levels of tech skill and different languages. |
| **Advisor** | Veterinarian, nutritionist, consultant, sales representative | Herd data and trends across clients. Full animal history. Evidence to guide recommendations. |

The experience should adapt to the user's role and language.

## 3. Where it is used
- **Large format (web, desk-side).** Overview, analysis, reports, setup, task assignment, compliance. **Current focus: desktop first, responsive.**
- **Small format (mobile, cow-side).** Identify, evaluate and treat animals, and record events. Must be fast, work offline, scan animal tags (RFID, barcode), be readable in barn conditions and easy to use with gloves. Still being defined.
- **Language.** English first. Spanish and Portuguese are documented early targets. More languages later.

## 4. Main workflow areas (not final scope)
- **Cow management and events:** find a cow, see her profile and history, record reproduction, health, calving and movement events.
- **Worklists and tasks:** tasks generated from animal data and schedules, in priority order, assigned by role. Common types: vet checks, hospital, vaccination, dry-off, pen moves, breeding, cull, animals needing attention. Completing a task confirms the event.
- **Protocols:** farm-defined treatment, reproduction, vaccine, dry-off, calving and pen-move protocols that create tasks automatically.
- **Insights and reports:** KPIs, trends, alerts, task compliance, herd inventory, traceability. Each insight should lead to an action (assign it, add it to a worklist, dismiss it, watch it).
- **Data quality:** help users fix data problems without running commands.
- **Setup:** users and roles, integrations, language and workflow configuration.

Early priorities named in strategy: inventory projections, breeding, protocols, data-quality actions, and role-based tasks and worklists.

Not goals: full DairyComp 305 parity, rebuilding every desktop workflow, or a generic AI assistant disconnected from real workflows.

## 5. UX principles
**Keep users in context.** Open a right-side panel instead of a new page. Keep filters, scroll position and selection when the panel closes.

**Show the basics first.** Reveal detail progressively.

**Tie actions to the selected object.** Keep action placement and behavior consistent on every screen (Add, Edit, Create).

**Make it easy to find and narrow.** Universal search. Strong filters: multi-select, saved filters, smart defaults.

**Make signals impossible to miss.** Alerts, deadlines, health and reproduction status look the same everywhere.

**Be easy to scan.** Clear hierarchy, consistent modular layouts, grouped content. Avoid walls of cards and dense unstructured tables.

**Use plain language.** Full names instead of codes and abbreviations. Plain-language errors with a way to recover.

**Build trust.** Show data freshness and system status. Separate observations from predictions and show uncertainty. AI can help later, but the value is the insight, not the technology.

**Landing page.** It should surface signals and entry points into workflows, based on the user's role. It is not meant to be a dashboard of reports.

Existing patterns to reuse: transaction pills (inventory history), linked entities (animal detail), drawer editing.

## 6. Navigation model (click-through levels)
| Level | What it is |
|---|---|
| 1 | Landing page. Content depends on the user (for example KPIs or tasks). |
| 1.5 | Preview drawer on the right. Summary of the selected item. The page stays visible and dimmed. |
| 2 | Full entity view, opened from the drawer's button. Starts with breadcrumbs. |
| 2.5 | Preview drawer opened from inside a level 2 page, for a sub-item. |
| 3 | Full view of the sub-item. |
| 3.5+ | Avoid. Use tabs or collapsible sections inside level 3 instead. |

Drawers have a top section (title and key reference data), a scrollable main content, and an optional fixed footer for the main action. Drawers do not need breadcrumbs. A drawer never replaces the page behind it.

## 7. Offline and field conditions (mobile)
Workers cannot wait for a connection. Scanning or searching an animal, logging events and treatments, viewing and completing tasks, hospital and breeding records, and critical alerts must work offline. New entries are saved locally and sync automatically. Show sync status and unsynced counts. Handle conflicts when two people edit the same cow. Respect language and role offline.

## 8. Still open
Overall information architecture, final flows, the mobile app, exact scope and timing of releases, and how Flux and PULSE surfaces divide the work. These will change. Treat this file as direction, not a decision log.

## 9. Sources (Confluence)
- Flux UX Guiding Principles (click-through model, guardrails, drawer). Updated 2026-10-27.
- GTM Framework 3.0 (used only for the definition of Flux). Updated 2026-10-30.
- Flux User Personas. Updated 2026-09.
- Central Platform UX/UI Opportunities. Updated 2026-06.
- Central Platform UX/UI Customer Experience Direction. 2025-09, older.
- CP: Phase One. 2026-03, older. Its timeline was overtaken by later strategy.
- New UX Ticket Template.

Left out on purpose: pricing, go-to-market and launch plans, costs, team structure and customer names.
