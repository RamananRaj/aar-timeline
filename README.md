# AAR Programs of Work — Timeline Manager

An interactive Gantt chart and resource management tool for tracking AAR program delivery across Regulatory, Non-Reg, GPS, and BAU streams.

## Features

- **Gantt views** — By Stream, By Squad, By Status
- **Phase tracking** — SD, DEV, SIT, UAT, Go-Live per project with SE/TA FTE counts
- **📊 Resources tab** — Monthly SE/TA demand chart backed by XLS data, drill-down by resource name
- **⚖ Levelling tab** — Capacity vs demand bar chart (blue = within cap, red = over), draggable squad size slider, per-month surplus/shortfall cards
- **☁ Cloud Sync** — GitHub Gist backend; any team member with the share URL can view and edit live data

## Usage

Open `Velocity_Timeline_Manager.html` directly in any modern browser — no server or build step required.

To enable team collaboration:
1. Click **☁ Cloud Sync** in the top bar
2. Create a GitHub Personal Access Token with the `gist` scope
3. Paste the token → the app creates a Gist and generates a shareable URL

## Hosting (GitHub Pages)

This repo is configured to serve via GitHub Pages from the `main` branch root.  
Once Pages is enabled the app is available at:

```
https://<your-username>.github.io/<repo-name>/Velocity_Timeline_Manager.html
```

## Data

Project data is stored in the browser's `localStorage` by default, and optionally synced to a GitHub Gist when cloud sync is enabled. The Gist file is `aar_programs_of_work.json`.

Raw resource figures come from `AAR_Monthly_Resource_Formulas.xlsx` (hardcoded into the app as `XLS_DATA`).
