# Campus admin — clickable prototype

A pixel-faithful, clickable web prototype of the Campus admin (Program Transfer Guide) flow, built from the Collaboratives Figma and the CCS Component Library (CVC skin). Pure static HTML/CSS/JS — no build step.

## The happy path

```
dashboard.html              Administrator Dashboard
  ├ collaboratives.html      Regional Collaboratives (list)
  │   ├ create-collab-1/2     Create Collaborative wizard
  │   └ collab-detail.html    Collaborative hub (Program / Admin tabs)
  │       ├ edit-collaborative.html        Edit settings + partners
  │       ├ add-program-1/2/3.html         Add Program wizard
  │       │   └ program-detail.html        Program + PTG requirements
  │       │       └ add-requirement.html   Requirement + courses
  │       ├ invite-admin.html              Invite campus administrators
  │       └ import-equivalencies-upload    ┐ Course equivalency CSV import
  │           └ import-equivalencies-review ┘  (upload → review/errors → submit)
  └ csv-imports.html          CSV import history (New Import → upload)
```

## What's distinct to the Campus admin flow
- **Course equivalency CSV import** — upload a CSV, review a data preview with row-level error highlighting, then submit the valid rows.
- **CSV imports history** with status badges and per-row download.
- **Edit Collaborative** tabbed editor.
- **PTG (Program Transfer Guide) requirements** with per-institution course scoping and a Grand Total Credits row.

## Updating
Edit the files and `git push` — GitHub Pages redeploys in a minute or two. Asset links carry a `?v=N` cache-buster; bump it when CSS/JS changes so updates show without a hard refresh.
