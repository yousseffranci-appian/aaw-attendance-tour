# Attendance at Work: guided tour

A self-contained, click-through tour of **Attendance at Work (AAW)**, sickness absence case management built on Appian. It follows one absence through four people:
- Sarah, the line manager;
- Marcus in Occupational Health;
- Rebecca in HR;
- Priya and the Trust's leaders.

It also shows Daniel's own view in My Attendance, and ends with his return to work.

- **Open it:** `index.html`, or the GitHub Pages site. Use ← → to move, or click the pulsing dot. Append `#s12` to the URL to open step 12.
- **Screens:** captured from the live AAW application.
- **Data:** every person and record is fictional; Pennine Vale is a fictional trust. Emails are simulated. Every AI output in the app is labelled, and a person approves anything that leaves the system.

## Embed it

Add `?embed=1` to hide the page title and footnote, so only the chapters, the screen and the controls show:

```html
<iframe src="https://yousseffranci-appian.github.io/aaw-attendance-tour/?embed=1"
        title="Attendance at Work on Appian: guided tour"
        style="width:100%; aspect-ratio:16/11; border:0; border-radius:12px"
        loading="lazy" allowfullscreen></iframe>
```

- **To start at a step:** add `#s<number>`, for example `?embed=1#s24` opens the HR chapter.
- **Narrow pages:** below 760 px wide, the tip moves under the screen. Give the iframe more height there, for example `aspect-ratio: 3/4`.

## Rebuilding

The source and capture scripts live in the AAW project (`Plans/assets/clickthrough/`), not here:
1. `capture-ct.js` resets the demo and walks the story in Chrome, taking a screenshot and recording the click target for each step.
2. `build.sh` writes this folder.
3. Afterwards, reset the demo data.
