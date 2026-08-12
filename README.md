# Kerala Recomp Plan

Single-file nutrition dashboard. No build step, no dependencies, no tracking.
Everything lives in `index.html`.

## Sections

| Tab           | What it does                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------ |
| Overview      | Daily targets, weekly averages, the five cooking rules, water schedule, seed and fruit guidance, recipe list |
| 7-Day Plan    | Five meal slots per day with per-meal macros. Opens on today automatically                                   |
| Protein Foods | Every protein source ranked by grams of protein per 100 kcal, with bars and ratings                          |
| Food Search   | 143 foods, searchable and sortable, plus a portion calculator                                                |
| Swaps         | Interchangeable protein anchors, carb blocks and veg sides                                                   |
| Shopping      | Weekly purchase list with ticks saved in your browser                                                        |
| Daily Log     | Weight, waist, calories, protein, water. CSV export                                                          |

## Run locally

Open `index.html` in any browser. That's it.

Or serve it:

```sh
python3 -m http.server 8080
```

## Deploy to GitHub Pages

1. Create a new repo and push these files to `main`.
2. In the repo, go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. Push. The workflow in `.github/workflows/pages.yml` publishes the site.

Your URL will be `https://<username>.github.io/<repo>/`.

> The repo must be public for Pages on a free account, or you need GitHub Pro for
> private Pages. This file contains your weight and body measurements, so if that
> matters to you, keep the repo private or drop the personal line in the header.

## Data storage

Shopping ticks, log entries and the theme choice are kept in `localStorage` in your
browser only. Nothing is sent anywhere. Clearing site data wipes them, so use
**Export CSV** on the log tab if you want a backup.

## Notes on the numbers

Macros come from standard food composition tables and are averages. The two biggest
sources of error in real use are portion size and cooking oil, not the table values.
Weigh things for the first week or two until you can eyeball them.

Built for planning, not diagnosis. Take any actual health decisions to a doctor or a
registered dietitian.
