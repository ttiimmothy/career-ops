# Custom Instructions -- career-ops

<!-- ============================================================
     THIS FILE IS YOURS. It will NEVER be auto-updated.

     Put your own house rules, custom workflows, and automations
     here -- anything you want the agent to ALWAYS do (or never do).

     This is for PROCEDURAL rules ("HOW I want things done").
     For WHO you are (archetypes, narrative, comp, negotiation),
     use modes/_profile.md instead. Keeping the two separate keeps
     each one readable.

     The agent reads this file alongside the system instructions;
     your rules here take precedence over the defaults, as long as
     they don't break the Data Contract (your files are never
     touched, and we never auto-submit an application for you).

     Because this is a user-layer file, anything you write here
     survives `node update-system.mjs`. Put customizations HERE,
     not in CLAUDE.md / modes/_shared.md / other system files --
     those get overwritten on update.
     ============================================================ -->

## House Rules

<!-- Rules the agent should always follow. Examples:
     - Always write evaluation summaries in British English.
     - Never include a photo in my CV (US / ATS-first market).
     - Cap each batch run at 20 listings unless I say otherwise.
     - If a report scores below 6, skip the cover letter. -->

### Auto-pipeline always-run rule (set 2026-09-13 by user)

- Run auto-pipeline Step 3 (PDF), Step 4 (draft application answers), and Step 5 (apply mode) **every time**, regardless of the evaluation score — never skip them on a low score or a discarded row. The PDF renders even when the score is below `auto_pdf_score_threshold`; the draft answers are generated even when the role is a hard-DQ mismatch.
- In Step 5, always add the generated application answers into the report (Section H) — never leave them out, even when they flag gaps or advise against applying.

<!-- This overrides the default auto_pdf_score_threshold gate and the "skip on hard-DQ" behavior. -->

### Resume generation rules (set 2026-09-13 by user)

- **Fit `cv.max_pages` (default 1) by adjusting typography, never by cutting content.** To shrink, lower `style.font_size` and `style.line_height` in `config/profile.yml` — the template's content-text sizes now derive from `--font-size` and `--line-height`, so those two tokens drive the whole page. Do **not** trim bullets, drop roles, or drop projects to hit the page budget.
- **Keep every Work Experience bullet from `cv.md`** — do not trim, merge, or omit any job bullet.
- **Keep every Project bullet from `cv.md`** — do not trim, merge, or omit any project bullet, and render them as a bullet list (same `<ul><li>` form as Work Experience), never flattened into a `description`/`tech` line. The tech stack for each project lives inline in its cv.md bullets — keep that text verbatim inside the bullets; do not split it into a separate `tech` field. The bullet list must render **visibly** as bullets (indented + list markers), matching how job bullets look — a bare `<ul>` with no indentation/markers does not count.
- **Education shows the full date span from `cv.md`, not a single year.** Put the range (e.g. `Feb 2021 - Jun 2021`) in the `year` field so it renders as a period in the same style as experience's period — never collapse it to just the end year.
- **Contact row order (fixed):** LinkedIn → GitHub → Portfolio → Email → Phone. Do not reorder.
- **Work Experience location:** render the location at the end of the **job role/title line** (2nd line), right-aligned via `justify-content: space-between` — the same justify layout as the company/period line — with **no comma**. Only write a location when `cv.md` explicitly states it for that role; if `cv.md` has no location for a role or `(no location)` is added for the experience, omit the location entirely (never assume a city from the company or the profile).

<!-- These rules are standing: they apply to every resume generation from now on. -->

## Custom Workflows

<!-- Multi-step routines you run often, given a short name. Examples:
     - "weekly review": scan my saved portals, evaluate the new roles,
       then give me a one-paragraph summary of the top 3.
     - "prep <company>": pull the JD, generate STAR stories from
       article-digest.md, and draft 5 likely interview questions. -->

(none yet -- add yours above)

## Output Preferences

<!-- How you like results formatted. Examples:
     - Reports: lead with the score and the one-line verdict.
     - Show the per-step token breakdown after a batch run.
     - Save PDFs date-first: YYYY-MM-DD-company.pdf -->

(none yet -- add yours above)

## Off-Limits

<!-- Things the agent must never do for you. Examples:
     - Never auto-fill or submit an application without showing me first.
     - Never edit a system file to customize my setup -- put it here. -->

(none yet -- add yours above)
