# Dashboard data schema

Send data in this shape and it drops straight into the dashboard. One sheet/tab per section, or one JSON file — either works.

Everything is plain text unless marked. Dates as `YYYY-MM-DD`. Leave a field blank rather than guessing.

---

## 1. Calendar

| Column | Required | Values / example |
| --- | --- | --- |
| `date` | yes | 2026-09-09 |
| `time` | yes | `09:30`, or `—` for all-day |
| `title` | yes | EPR programme management meeting |
| `meta` | no | Teams · programme leads |
| `cadence` | yes | Weekly / Monthly / One-off / Mission / Programme |
| `kind` | yes | `statutory` · `upcoming` · `conference` · `mission` |
| `hub` | no | Nairobi / Dakar / Brazzaville / RD office — blank = personal |
| `open_to_all` | no | yes / no — shows it on the cluster shared calendar |

## 2. Strategic documents

| Column | Required | Values / example |
| --- | --- | --- |
| `title` | yes | Q3 Emergency Response Performance Report |
| `type` | yes | Concept note / Report / Brief / Assessment |
| `origin` | yes | `Drafted by PAMS` or `Requested by RD` |
| `due` | yes | 2026-09-12 |
| `status` | yes | Not started / Drafting / In review / Cleared |
| `link` | no | Full SharePoint URL |
| `path` | no | SharePoint › EPR › Reports › Q3 |

## 3. Missions

| Column | Required | Values / example |
| --- | --- | --- |
| `place` | yes | Islamabad, Pakistan |
| `start` / `end` | yes | 2026-09-21 / 2026-09-24 |
| `purpose` | yes | Country office readiness assessment |
| `tr_approved` | yes | yes / no |
| `report_submitted` | yes | yes / no |
| `claim_submitted` | yes | yes / no |

A mission counts as closed only when all three are `yes`.

## 4. Conferences

| Column | Required | Values / example |
| --- | --- | --- |
| `title` | yes | Global Health Security Forum, Doha |
| `start` / `end` | yes | 2026-11-18 / 2026-11-18 |
| `role` | yes | Keynote speaker / Panellist / Attendee / Chair |
| `confirmed` | yes | yes / no |
| `abstract_sent` | yes | yes / no |
| `slides_ready` | yes | yes / no |
| `brief_read` | yes | yes / no |

## 5. Memos

| Column | Required | Values / example |
| --- | --- | --- |
| `origin` | yes | `CO` · `HQ` · `Internal` |
| `title` | yes | Pakistan CO — request for surge deployment support |
| `meta` | no | For clearance · 2 attachments |
| `date` | yes | 2026-09-08 |
| `link` | no | SharePoint or mail URL |

## 6. Inbox triage rules

Not a table — a short list from RED:

- **Categories** she wants mail sorted into (current set: Invitation to conference, Document to review, Decision to make, Needs response, For information).
- **Urgency rules** — e.g. "anything from the RD front office is urgent", "requests with a date inside 48 hours are urgent".
- **Reminder lead time** — 1 day before / 2 hours before / on the day.

## 7. Hubs

| Column | Required | Values / example |
| --- | --- | --- |
| `hub` | yes | Nairobi / Dakar / Brazzaville / RD office |
| `lead_text` | yes | Emergency operations · 22 staff |
| `activity_title` | yes | Horn of Africa cholera response — operational review |
| `activity_meta` | no | With WCO Kenya |
| `due` | yes | 2026-09-18 |
| `status` | yes | Not started / Drafting / In review / Cleared |

## 8. Directory

| Column | Required | Values / example |
| --- | --- | --- |
| `name` | yes | Dr Chamla |
| `role` | yes | Director, EPR |
| `hub` | no | Brazzaville |
| `mutual_access` | yes | yes / no |

---

## Easiest way to send it

1. One Excel workbook, one tab per section above, headers exactly as written — **or**
2. `data.json` in this repo, filled in following the same field names.

Send either to the repo (Add file → Upload files) or by mail. No formatting or tidying needed — raw exports are fine.
