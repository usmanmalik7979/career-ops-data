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

- Write all output in British English (UK spelling, £, DD Month YYYY dates).
- Generate PDFs on A4 paper.
- **Sponsor licence check (mandatory for every evaluation, triage and apply):**
  1. If the JD says the employer cannot/will not sponsor, or requires the right to work in the UK without sponsorship → recommend SKIP and stop.
  2. Otherwise look the employer up in `data/uk-sponsor-register.csv` (official GOV.UK "Register of licensed sponsors: workers"), e.g. `grep -i "<name>" data/uk-sponsor-register.csv`. Try the brand name, then the legal entity name (often "<Name> Ltd / Limited / UK Ltd") from the careers page or footer.
  3. Count it as a sponsor only if a row shows route **Skilled Worker**. A **B rating** is a soft warning, not a blocker.
  4. Record the result in the report header as `**Sponsor licence:** confirmed (<register name>, <rating>) | not found | ambiguous (<candidates>)`. Never guess a match: if several entities could be it, mark ambiguous and ask.
  5. "Not found" → treat as a blocker and tell the user (it may be listed under an unrelated legal name).
- If `data/uk-sponsor-register.csv` is missing or older than 30 days, refresh it: fetch https://www.gov.uk/government/publications/register-of-licensed-sponsors-workers, take the linked CSV on assets.publishing.service.gov.uk, and save it to `data/uk-sponsor-register.csv`. The user also uses https://huntukvisasponsors.com/register-of-licensed-sponsors for manual checks; it blocks automated requests, so use the GOV.UK file instead.

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
