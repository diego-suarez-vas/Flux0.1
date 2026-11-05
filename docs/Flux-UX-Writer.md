# Flux UX writing guide

Use this guide for every word users read in Flux: titles, labels, buttons, messages, empty states, alerts, tooltips and modals. English is the main language today. The rules come from the PULSE guide and apply to Flux without changes, with new patterns added for Flux.

## 1. Core principles
- **Clarity over complexity.** Make messages easy to understand at a glance.
- **Conciseness for impact.** Remove unnecessary words. Prioritize value over quantity.
- **User-centric language.** Write from the user's point of view. Use "you".
- **Action-oriented verbs.** Guide users toward what to do next.
- **Consistency of tone.** Keep the same tone at every touchpoint.
- **Accessibility.** Write at an 8th grade reading level. Use inclusive, gender-neutral language.

## 2. Voice
- **Expert, but not arrogant.** Confident and knowledgeable without lecturing.
- **Data-driven, but relatable.** Connect insights to user outcomes, such as a healthier herd or better profitability.
- **Professional, but approachable.** Polished and human.
- **Supportive, not condescending.** Encourage, reassure and empower.
- **Pragmatic, not pessimistic.** Offer solutions, not barriers.

## 3. Tone by user
- **Workers (cow-side, operational):** Clarity, brevity and reliability. Short messages, one idea each.
- **Owners, managers and advisors (strategic):** Insight, empowerment and results.

## 4. Language mechanics
- **Voice:** Use active voice.
- **Casing:** Sentence case for messages. Title Case for buttons and page titles. Everything else (labels, helper text, tooltips) uses sentence case.
- **Punctuation:** Use commas, apostrophes and ellipses correctly.
- **Exclamation points:** Only for feature announcements.
- **Contractions:** Use them naturally (can't, don't).
- **Abbreviations:** Use standard dairy terms that users know, such as DIM. Use only the approved abbreviations in the table below, and show the full term in a tooltip. Do not invent abbreviations. Do not show system codes. Write DairyComp 305, not DC305.
- **No jargon:** Keep it simple and direct. Terms that dairy professionals use every day are not jargon.
- **Emphasis:** Bold only for UI element names or critical emphasis.
- **Truncation:** Avoid it unless a tooltip shows the full text.
- **Names:** Follow official product names: Flux, VAS PULSE Platform, DairyComp 305.
- **Numbers and dates:** Use numerals. Show the unit with every number. Format dates, numbers and units by the user's region.

### Approved abbreviations
Use these as written. Show the full term in a tooltip. The design lead adds new ones.

| Abbreviation | Full term |
|---|---|
| DIM | Days in milk |
| SCC | Somatic cell count |
| DMI | Dry matter intake |
| BCS | Body condition score |
| IOFC | Income over feed cost |
| TMR | Total mixed ration |
| ET | Embryo transfer |
| EID | Electronic ID |
| RFID | Radio frequency identification |
| KPI | Key performance indicator |

"AI" can mean artificial insemination or artificial intelligence. Spell out the one you mean.

## 5. Content best practices
- Explain the benefit or impact of a feature. Do not only describe what it does.
- Give examples when possible.
- Do not state the obvious.
- Keep a second-person perspective ("you").
- Use industry and product knowledge to keep content accurate and relevant.

## 6. Patterns

### Buttons
- Title Case. Start with a verb. Use one to three words when possible.
- Say what will happen: Save, Add Event, Assign Task, See Animal Profile.
- Avoid vague labels such as "OK" or "Click Here".

### Insights and alerts
Write in this order:
1. **What changed or needs attention.** State the observation.
2. **Why it matters** to the user's farm.
3. **The next step.** A short instruction or a button.

Separate what you observed from what you predict ("dropped" vs "may need"). Say what the insight is based on when it helps trust. Do not use alarming words unless the user must act now.

> Milk yield dropped 8% in Pen 4 this week. Check feed, water and recent events for this pen.
> These 5 animals may need a breeding check this week, based on their cycle.

### Errors
Say what happened, then how to fix it. Use plain words. Do not blame the user. Do not use "Oops".

> Upload failed. Check your file format and try again.

### Success messages
Keep them short, specific and in the past tense. Add what happens next only if it helps. No exclamation points.

> Event saved. The animal's history is up to date.

### Empty states
1. **First line:** Clear, empathetic and direct. Acknowledge that there is no data.
2. **Second line:** Give context or say what to do next.
3. **Action (when applicable):** Encourage the next logical step.

> No tasks today.
> New tasks appear here when they're assigned to you.

> No events yet.
> Add the first event to start this animal's history.
> [Add Event]

### Modals
- Do not use questions.
- **Title:** Uppercase. An affirmative sentence.
- **Description:** Confirm the action. Explain the consequences if needed.
- **Buttons:** CANCEL and CONFIRM. Buttons inside modals are the one exception to Title Case: write them in uppercase. Buttons everywhere else stay in Title Case.

> DELETE EVENT
> This removes the event from the animal's history. You can't undo this action.
> [CANCEL] [CONFIRM]

### Drawers
- **Title:** The name of the item or view.
- **Top section:** Short reference data, such as animal ID, pen or stage.
- **Footer button (optional):** Save, Confirm, or a button that goes deeper, such as See Animal Profile.

### Offline, sync and data freshness
Show the state in plain words. Do not use technical words like "cache", "queue" or "conflict".

> Updated 5 minutes ago.
> You're offline. Your changes will sync when you reconnect.
> 3 changes are waiting to sync.
> Sync failed. Check your connection and try again.
> Someone else updated this animal. Review the changes before you save.

### Search and filters
- The search placeholder says what users can search: "Search animals, tasks and reports".
- No results is an empty state: "No results for 'Pen 9'. Check the spelling or clear your filters."
- Use plain words for filter names.

## 7. Terms
Use one word for one idea.
- **Animal:** The general term. Use cow, heifer or calf only when the group matters.
- **Pen:** A place where animals are kept.
- **Task:** One piece of work assigned to someone.
- **Worklist:** A list of tasks, such as Vet or Hospital.
- **Event:** Something recorded about an animal, such as a treatment, breeding, calving or move.
- **Protocol:** A farm-defined plan that creates tasks.
- **Insight:** Something Flux found in the data, with a next step.
- **Alert:** A notice that needs attention soon.

## 8. Writing for other languages
English is the main language now. Write so that translation is easy:
- Write complete sentences. Do not join pieces of text together.
- Avoid idioms, slang and humor.
- Do not put text inside images.
- Leave room. Translated text can be 30% longer or more.
- Use one term per concept (see section 7).

## 9. Review checklist
Check for:
- Only approved abbreviations. No system codes.
- Inclusive, gender-neutral language (they/their, role-based nouns).
- Clarity and flow. No missing context, broken variables or cross-reference gaps.
- Correct punctuation and capitalization.
- Alignment with voice, tone and product names.
- Terms from section 7.
- Benefit-driven explanations instead of generic descriptions.
- A clear next step. Errors say how to fix the problem.
- Observations and predictions are clearly different.

## 10. Examples in practice

**Draft:** "Data upload failed. The user should check his file format."
- ❌ Gendered pronoun ("his").
- ❌ Passive tone ("should check").
- ❌ Does not guide the next action.

Suggestions:
- ✅ "Upload failed. Check your file format and try again."
- ✅ "Upload failed. Review the file format before retrying."
- ✅ "File format error. Update the file and upload again."

**Draft:** "Oops! Something went wrong with the sync."
- ❌ Exclamation point.
- ❌ Vague.
- ❌ No next step.

Suggestion:
- ✅ "Sync failed. Check your connection and try again."

**Draft (modal):** "Are you sure you want to delete this event?"
- ❌ Question.
- ❌ Does not explain the consequence.

Suggestion:
- ✅ Title: "DELETE EVENT". Description: "This removes the event from the animal's history. You can't undo this action."
