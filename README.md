# શાર્દૂલ શિશુ વિહાર — આચાર્ય માર્ગદર્શિકા

Teacher's weekly planning guide for Shardul Shishu Vihar, Vadodara. Static site hosted on GitHub Pages.

**Live:** https://shardul-vadodara.github.io/didi-margdarshika/

## What it shows

One feature — the week's comprehensive teaching plan, browsable by week and age group:

- **સાવજ-કેસરી** (૨.૫-૫.૫ વર્ષ) and **મૃગેન્દ્ર-પુંડરિક** (૫.૫-૮ વર્ષ)
- Per week: title, dates, main activities, ક્રિયાકલાપ (detailed steps, materials, learning goals), teacher notes, festivals, season notes
- Downloads: teacher guide PDF / PNG per week

## How content gets here

Content is authored in the private `active-parents` repo using the unified planner tool (v4). The teacher clicks **પ્રકાશન પેકેજ સેવ કરો** which writes backup JSON + teacher PDF/PNG to `exports/`, then commits and pushes. A GitHub Action converts the data and pushes it here:

```
data/config.json   school info + groups
data/weeks.json    published weeks (generated — do not hand-edit)
files/             teacher PDFs / PNGs (generated)
```

GitHub Pages redeploys automatically on every push (~1 minute).

## Constraints

- Static only (GitHub Pages free tier): no server, no login, no database
- This repo is public — never publish student names, phones, or photos
