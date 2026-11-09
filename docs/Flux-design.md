# Flux design criteria

How to decide a composition, not what to build it with. Components, variables, styles and icons live in the two Figma libraries and are always read from Figma (see CLAUDE.md). This file never lists them.

Related files, already loaded by CLAUDE.md: Flux-Product-Context.md (what and for whom), Flux-UX-Writer.md (words), CLAUDE.md (how to work).

Marks used here:
- **[CONFIRM]**: draft proposal or missing detail. Ask before relying on it.
- Anything without a mark comes from the product context or the UX writing guide.

## 1. Choose the pattern

| Situation | Use | Why |
|---|---|---|
| Quick look at an item from a list, table or landing signal | Right-side preview drawer (level 1.5) | Keeps the user in context. Filters, scroll and selection survive when the drawer closes. |
| Full detail of an entity | Full page with breadcrumbs (level 2), opened from the drawer's button | The drawer stays a summary. The page holds the depth. |
| Sub-item of an entity | Drawer from inside the page (2.5), then full view (3) | Same logic, one level down. |
| More content than fits at level 3 | Tabs or collapsible sections inside level 3 | Never go to level 3.5. |
| Edit or add something small | Drawer editing | Existing pattern to reuse. |
| Destructive or irreversible action | Modal | See the modal pattern in the UX writing guide. |

Rules:
- A drawer never replaces the page behind it. The page stays visible and dimmed.
- Drawer anatomy: top section (title and key reference data), scrollable content, optional fixed footer with the one main action. No breadcrumbs in drawers.
- The top section always carries the item's identifiers (for example, animal ID and pen), so the user knows which item they are looking at. Switching tabs or opening a panel must never leave them guessing. Follow Example Screens for how the top section behaves on scroll.
- Task and worklist drawers make it clear whether the user is reviewing the task or completing it. The footer action and labels say which. Follow Example Screens. If none shows it, ask the designer.
- Drawers with forms (for example, Add Event) confirm success visibly, using the success message pattern in the UX writing guide. Undo and draft saving for critical forms: **[CONFIRM]** whether Flux includes them.
- Action placement (Add, Edit, Create) is the same on every screen and tied to the selected object.
- Table or cards: depends on the use case. If the brief or ticket provides an existing page in the flow, follow it. If not, ask the designer. Either way, avoid both extremes: no walls of cards, no dense unstructured tables.
- Landing page: signals and entry points by role. Not a dashboard of reports.

## 2. Signals and tokens

- Alerts, deadlines, health and reproduction status look the same everywhere. Reuse the same component and token for the same meaning. Never restyle a status locally.
- Bind every value to a variable or style. Prefer semantic tokens over primitive ones. Read the token tiers and naming directly from Foundations.
- Meaning of each status color: read it from Foundations and from how Example Screens use it. If it isn't defined in either, ask. Don't assign meaning from memory.
- Every insight ends in an action: assign it, add it to a worklist, dismiss it, or watch it.
- Separate observations from predictions visually, not only in text. Follow how Example Screens do it. If no example shows it, ask the designer.

## 3. Layout

- Build in this order: frame and grid, layout, components, text.
- Grid, margins, spacing scale, drawer width, table density: take them from the closest Example Screen. Don't set values by hand.
- Clear hierarchy, consistent modular layouts, grouped content. Show the basics first and reveal detail progressively.
- Universal search and strong filters (multi-select, saved filters, smart defaults) belong on any list or table screen.
- On data-heavy lists (events, tasks, change logs), filters are visible and easy to notice. Never bury them.

## 4. Screen states

Every screen that loads data must define these states. Structure comes from Example Screens. Copy comes from the UX writing guide.

| State | Visual approach |
|---|---|
| Loading | Spinner by default. It can change by flow, so confirm with the designer which loading pattern the flow uses. |
| Empty | Short message, one line of context, one action when it applies. |
| No results | Same as empty. Offer to clear filters. |
| Error | What happened and how to recover, near the place it failed. |
| Stale or updated data | Show data freshness where the user reads the data. |
| Partial data (some of the content loaded, some didn't) | **[CONFIRM]** whether this state is needed. |

Offline states apply to mobile and are out of scope for now.

## 5. Reference screens

Before building, find the closest example in Example Screens and copy its structure.

Current focus: preview screens (level 1.5 and 2.5).

| Screen type | Example frame |
|---|---|
| List or table with a selected row and the drawer open (page dimmed) | **[CONFIRM]** link |
| Entity preview drawer (for example, animal) | **[CONFIRM]** link |
| Insight or alert preview drawer with its actions | **[CONFIRM]** link |
| Task or worklist item preview drawer | **[CONFIRM]** link |
| Drawer editing or add form (for example, Add Event) | **[CONFIRM]** link |
| Drawer opened from inside a full page (level 2.5) | **[CONFIRM]** link |
| Drawer states (loading, empty, error) | **[CONFIRM]** link |
| Destructive action modal | **[CONFIRM]** link |
| Entity detail, full page (level 2) | **[CONFIRM]** link, later |
| Landing page | **[CONFIRM]** link, later |
| Setup or settings | **[CONFIRM]** link, later |

If no example fits, ask. Don't improvise a new pattern.

## 6. Avoid

- Walls of cards. Dense tables with no structure.
- Actions in different places on different screens.
- A new page where a drawer would keep the user in context.
- Level 3.5 and deeper.
- Codes and unapproved abbreviations in the UI.
- Color as the only carrier of status. **[CONFIRM]** whether an icon or label is required.
- Local styles, hex codes, loose pixel values.
- Features, data or flows the request didn't ask for.

## 7. Accessibility

Reference target: WCAG 2.2 AA. It is a goal, not a guarantee. Existing library components, tokens and example screens don't always meet it, and they can't be changed here.

What to do when you find a failure in something that already exists (contrast, target size, focus state, status shown by color alone, and so on):
1. Don't fix it and don't work around it. Keep building with the library as is.
2. Tell the designer in one short message: what fails, where, and which WCAG criterion it breaks.
3. Ask one question: change it or ignore it and continue?
4. If the answer is to change it, treat it as an express request to touch the library (CLAUDE.md rule 2). If the answer is to ignore it, continue and don't raise the same finding again in this task.
5. List every finding and the decision in the final report.

What you control, and should always get right:
- Status doesn't depend on color alone in anything you compose.
- Plain language and a clear recovery path in every error.
- Labels and text follow the UX writing guide.

## 8. Check before reporting

- Does this help the user understand something important sooner, and make the next step clearer?
- Is it the right pattern for the situation (section 1)?
- Does it match an Example Screen?
- Is every value bound to a variable or style?
- Do status signals match the rest of the product?
- Are all states in section 4 covered?
- Does the text pass the UX writing checklist?
- Were accessibility failures in existing pieces flagged to the designer, with their decision recorded?
- Did anything get built that the request didn't ask for?

## 9. Open

Overall information architecture, final flows, mobile, exact release scope and how Flux and PULSE surfaces divide the work. Treat these as questions, not decisions.

Update this file when you correct a design decision. That correction is the rule that belongs here.
