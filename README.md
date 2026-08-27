# SkillSet WSP / ATR Demo

[![Static Site Smoke Test](https://github.com/LokerH83/skillset-wsp-demo/actions/workflows/static-site-smoke-test.yml/badge.svg)](https://github.com/LokerH83/skillset-wsp-demo/actions/workflows/static-site-smoke-test.yml)

Live demo: https://lokerh83.github.io/skillset-wsp-demo/

SkillSet WSP / ATR Demo is a static sales and workflow demonstration from [SkillSet SA](https://www.skillsetsa.com/). It shows how training spreadsheets can be inspected and converted into a more controlled process for workforce planning, training delivery, evidence tracking and decision-ready reporting.

## What the demo shows

- Local Excel and CSV workbook inspection
- Training demand, WSP planning and ATR capture
- Provider, course, booking and employee workflow
- Requested-versus-planned-versus-achieved reporting
- Submission-readiness scoring and data-quality checks
- Evidence, owner, due-date and management sign-off controls
- Filtered CSV exports and a print-ready readiness pack
- SkillSet SA configuration through `client-config.js`

## Honest product boundary

This repository is a browser-based static demo and sales asset. It uses clearly synthetic data and browser `localStorage`; it is not a production Microsoft 365 system, an official SETA submission tool or a system of record.

A production implementation would require organisation-approved authentication, role-based access, a controlled data layer, workflow automation, governed reporting, and approved security, privacy, retention and compliance controls.

## Run locally

From the repository folder:

```bash
python -m http.server 8092
```

Then open `http://localhost:8092/`.

## Configure the demo

Edit `client-config.js` to change product wording, colours, reporting cycle and privacy copy. Reusable public presets are in `config-presets/`.

## Core files

- `index.html` - application shell
- `styles.css` and `scanner-alignment.css` - SkillSet-aligned interface
- `app.js` - browser-local workflow and reporting logic
- `client-config.js` - public demo positioning and visual settings
- `data/demo-snapshot.js` - neutral synthetic demo data
- `sample-workbooks/SkillSet_WSP_ATR_Demo_Workbook.csv` - synthetic scanner sample
- `scripts/static-smoke.mjs` - structural smoke test
- `scripts/functional-demo-test.mjs` - functional demo test

## Safety

- Use synthetic or explicitly approved demonstration data only.
- Do not load private employee records into a public deployment.
- Workbook inspection happens locally in the browser.
- No data is sent to SkillSet SA by this static demo.
- Confirm SETA, legal, security and compliance requirements for any real implementation.

## Publishing

GitHub Pages publishes the `main` branch from the repository root.

Repository: https://github.com/LokerH83/skillset-wsp-demo

Expected public URL: https://lokerh83.github.io/skillset-wsp-demo/