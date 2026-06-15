# Campus admin — clickable prototype

A pixel-faithful, clickable web prototype of the **Campus admin** flow (Program Transfer Guide requirements), built from the Collaboratives Figma "Campus Admin" and "Version 2" sections and the CCS Component Library (CVC skin). Pure static HTML/CSS/JS — no build step.

## The happy path

```
dashboard.html            Administrator Dashboard
  └ collaboratives.html    Regional Collaboratives (list)
      └ program-detail.html    Program + PTG Requirements table
          ├ add-requirement.html        Add Requirement (Version 2)
          │     ├ Add Course / Add Subject  → slide-in trays
          │     └ AND / OR course list
          └ add-requirement-group.html  Add Requirement Group (AND/OR blocks)
```

## What's in scope
- **Campus Admin section** — the navigation: Dashboard → Regional Collaboratives → Program detail with the **PTG Requirements** table (grouped, Grand Total Credits row, Preview/Edit per row).
- **Version 2 section** — the redesigned requirement authoring:
  - **Add Requirement** with a live **Requirements list** (Course / Component / Subject items, colored by type, with edit/delete) and an **AND/OR** connector.
  - **Add Course / Add Subject** as 480px **slide-in trays**.
  - **Add Requirement Group** — multiple requirement blocks joined by **OR/AND** connectors, with display-title options.

## Updating
Edit the files and `git push` — GitHub Pages redeploys in a minute or two. Asset links carry a `?v=N` cache-buster; bump it when CSS/JS changes so updates show without a hard refresh.
