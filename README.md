# Website Performance Status Dashboard

Class project for ADPR 550 (A.I. in Strategic Communication), University of Tennessee, Knoxville.

A single-page dashboard that shows whether website results meet the goals leadership has set. Choose a metric and a time period (7, 30 or 90 days) and it reports **On track**, **At risk** or **Off track**, with the actual value, the goal, the tolerance band and a daily trend line.

## How it works

- The page opens with made-up sample data and sample goals.
- To use your own, load a GA4 daily export (CSV) and a goals file (CSV) under "Load data and goals". Files are read in the browser only. Nothing is uploaded or saved.
- Goals cannot be changed from the dashboard. Goal owners change them in the goals file.
- If the data is incomplete or a goal is not filled in correctly, the dashboard gives no status and says what to fix.
- Each section (Status, All approved metrics, Goals) has an **Export as PowerPoint** button that saves that section as a slide in the same design. The slide carries the "data as of" date and any warnings shown on the page.

## Files

- `index.html` – the whole application. The PowerPoint export loads the open-source PptxGenJS library (version 3.12.0) from the jsDelivr CDN when a button is first used. Slides are built in the browser.
- `sample-ga4-daily-export.csv` – example of the data file format
- `sample-goals.csv` – example of the goals file format

## Limits

- The refresh is manual, so results are only as current as the last export.
- Average goals use a simple average of the daily values.
- The dashboard checks that entries are complete. It cannot tell whether a target or an exported number is the right one. People set the goals and decide what a status means.

Do not commit real analytics data or real targets to this repository. It is public.

Built with AI assistance (Claude Code).
