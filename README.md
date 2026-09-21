# EPR Dashboard

Personal and programme dashboard for the EPR Regional Office — statutory calendar, AI inbox triage, daily to-do with colour ageing, mission and conference follow-up, strategic documents, and cluster-wide shared views.

## View it

Once GitHub Pages is enabled (see below), the live dashboard is at:

**https://atagbaza.github.io/EPR-Dashboard/**

## Enable GitHub Pages (one time)

1. Upload `index.html` to the root of this repository.
2. Go to **Settings → Pages**.
3. Under *Build and deployment*, set **Source** to `Deploy from a branch`, **Branch** to `main` / `root`.
4. Save. The URL above goes live in about a minute.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The dashboard, fully self-contained — works offline, no build step, no dependencies |
| `source/EPR Command Dashboard v3 WHO blue.dc.html` | Editable source the dashboard is compiled from (WHO blue palette) |
| `source/support.js` | Runtime the source file loads when opened locally |
| `DATA-NEEDED.md` | The outstanding inputs and exactly where each one lands in the dashboard |
| `SCHEMA.md` | The exact fields to send for each section — share this with anyone supplying data |
| `data.template.json` | Blank template matching the schema, ready to fill in |

## Collaborating

- **Reviewing and commenting** — open an Issue, or comment on a line of `index.html` in a pull request.
- **Content changes** (calendars, activities, document titles, missions) — these live in the source file's data tables near the top of its `<script>` block: `EVENTS`, `DOCS`, `MAILS`, `HUB_DETAIL`. Edit there, not in `index.html`.
- **Re-compiling** — `index.html` is generated from the source file. Do not hand-edit it; edits there are lost on the next build.

## Status

Structure and functionality are complete. Sample content is realistic placeholder data pending the real calendars and activity log — see `DATA-NEEDED.md`.
