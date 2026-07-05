# શાર્દૂલ શિશુ વિહાર — દીદી માર્ગદર્શિકા

Teacher's weekly planning guide for Shardul Shishu Vihar, Vadodara. Static site hosted on GitHub Pages.

**Live:** https://shardul-vadodara.github.io/didi-margdarshika/

## What it shows

The week's teacher sheet, browsable by week and age group:

- **સાવજ-કેસરી** (૨.૫-૫.૫ વર્ષ) and **મૃગેન્દ્ર-પુંડરિક** (૫.૫-૮ વર્ષ)
- Per week: title, dates, and teacher sheet downloads (PDF / PNG) — the sheet
  contains પ્રવૃત્તિ, શૈક્ષણિક પ્રવૃત્તિ માર્ગદર્શિકા, વિશેષ ઉત્સવ/દિવસ, ઋતુ સંકેત,
  and a blank ઘટક-notes table
- The front-end also renders richer per-week content (activities, ક્રિયાકલાપ,
  notes) if it ever appears in `data/weeks.json` — currently only downloads
  are published

## How content gets here

Content is authored in the private `active-parents` repo using the unified planner tool (v4). The teacher clicks **શિક્ષક PDF/PNG સેવ કરો** which writes the teacher sheet PDF/PNG to `exports/teachers/`, then commits and pushes. The `publish-teachers.yml` GitHub Action (separate from the parent-portal one) builds the index and pushes it here:

```
data/config.json   school info + groups
data/weeks.json    published weeks index (generated — do not hand-edit)
files/             teacher sheet PDFs / PNGs (generated)
```

GitHub Pages redeploys automatically on every push (~1 minute).

## Constraints

- Static only (GitHub Pages free tier): no server, no login, no database
- This repo is public — never publish student names, phones, or photos
