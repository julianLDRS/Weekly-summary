# Weekly Summary: how to update

Julian's daily work log. Julian tells Claude what they worked on, and Claude adds it here. Vercel redeploys the site from `main` on every push.

## Files
- `index.html`: the page. Don't change it for a normal update.
- `data.json`: all content.
  - `days["YYYY-MM-DD"]` = `{date, summary, projects: [{name, sections: [{title, items: []}]}]}`
  - `weeks["YYYY-MM-DD"]` (key = the Sunday that starts the week) = `{subject, body}`: the email text shown in the Weekly summary box. Without it the page builds a summary from that week's days.

## Daily update
1. Use the date Julian means ("today" = the current date, "yesterday" = the day before).
2. Add or edit that day in `data.json`, then refresh the current week's `weeks` email so it includes the new work.
3. Check the JSON is valid, then commit and push to `main`.

## How Julian wants entries written
- Short: a line or two per thing, not every detail. Julian said not to type everything.
- Each project is its own entry with its own name. These are separate projects, never sub-items of each other: Stagwell AI, NewIntel, NEW, InfluencerMarketing.Ai.
- Some work is done without Claude, so there's no record of it. Write it the way Julian describes it, with no invented detail, and don't ask for proof.
- Work done with Claude can be checked in the repos, e.g. `git log` in `julianLDRS/stagwell-ai` for the Stagwell AI site, and `julianLDRS/imai-mql` for InfluencerMarketing.Ai MQL onboarding.
- Write the weekly email in plain English, signed "Julian".
- Answer Julian in English.
