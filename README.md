# Global Food Waste Reduction Network — requirements & traceability

A worked example of AI-assisted requirements management, built for a PMI
"GenAI for Project Managers" course. It follows a fictional project — a
platform connecting food donors with recipients to reduce food waste — from
raw stakeholder documents through to a live requirements traceability
dashboard.

**Read [`Development Approach and Lifecycle/WORKFLOW.md`](Development%20Approach%20and%20Lifecycle/WORKFLOW.md)
for the full step-by-step walkthrough**, including the prompts used at each
stage and what came out of them.

## What's in this repo

All files live under `Development Approach and Lifecycle/`:

| File | Description |
|---|---|
| `01. Project Charter.docx` | Project charter — objectives, scope, stakeholders, governance |
| `02. Project Research Areas.docx` | Research activities mapped to the charter's identified risks |
| `03.Project_Requirements_Document.pdf` | Early draft requirements document |
| `04–06. Requirements Team Meeting Transcript *.docx` | Three simulated stakeholder meetings (data security, integration risk, user adoption) |
| `Requirements_Documentation_Global_Food_Waste_Reduction_Network_v2.docx` | All requirements extracted from the source documents, organized by PMBOK category |
| `RTM_Global_Food_Waste_Reduction_Network.xlsx` | The Requirements Traceability Matrix — requirements, test cases, and a traceability verification log |
| `rtm_dashboard.html` | Standalone monitoring dashboard generated from the RTM |
| `WORKFLOW.md` / `workflow-diagram.svg` | How this was all built, step by step |

## Viewing the dashboard

`rtm_dashboard.html` is a single self-contained file (it loads
[Chart.js](https://www.chartjs.org/) from a CDN, nothing else) — open it
directly in a browser, or host it with GitHub Pages:

1. Push this repo to GitHub.
2. In **Settings → Pages**, set the source to your default branch.
3. Visit `https://<your-username>.github.io/<repo-name>/Development%20Approach%20and%20Lifecycle/rtm_dashboard.html`.

It's a static snapshot of the RTM at the time it was generated — regenerate
it whenever the RTM's requirement list or statuses change.

## Tools used

- **ChatGPT** — drafted the initial project documents (charter, research
  memo, meeting transcripts)
- **PMI Infinity** — source of the RTM template's column structure
- **Claude** — requirements extraction and categorization, RTM construction,
  test case authoring, traceability verification, and dashboard generation

## Working with the RTM

The RTM workbook (`RTM_Global_Food_Waste_Reduction_Network.xlsx`) is the
source of truth. It has four tabs:

- **RTM** — one row per requirement, with priority, design spec reference,
  development status, linked test case, and test status
- **Test Cases** — one test scenario per requirement
- **Traceability Verification** — an audit log of ID checks and any
  duplicate/orphaned rows found (and how they were resolved)
- **Legend & Notes** — column definitions and current status summary

If you update the RTM, regenerate the requirements document and the
dashboard from it afterward so all three stay consistent.
