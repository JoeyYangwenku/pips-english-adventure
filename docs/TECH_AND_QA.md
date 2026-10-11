# Technical Overview · Pip V5.4.2

## Prototype

- `index.html` contains the HTML/CSS/JavaScript for the six-task educational prototype.
- The GitHub Pages variant loads the hero artwork from eight same-origin text data chunks in `assets/hero-data/`. That preserves the original opening image while respecting per-upload request limits.
- **The GitHub-hosted HTML is not a standalone offline file.** For offline demonstration use the separately produced original single-file HTML in the full submission package.
- Other smaller artwork and the UI styles remain embedded in the HTML.
- Browser speech synthesis generates audio on demand; voice quality varies by OS/browser.
- No backend, account registration, microphone recording, or automated speech scoring.
- Lesson Map and Learning Evidence derive from answers, retries and activity completion. Attempts and first-try correctness are not equivalent to language mastery.

## Demonstrated user path

1. Story introduction and Crystal Bridge opening.
2. Six-task learning overview.
3. Current lesson + changing Lesson Map / Learning Evidence.
4. Wrong answer prompt and correct retry.
5. Completion state and Chinese parent activity report.

## Browser/QA boundary

Previous CSS layout tests used Chromium at 1440, 1024, 810, and 390 pixels. New GitHub Pages hosting needs its own browser acceptance test (hero-part requests, asset initialization, all six interactions).

## Roadmap

- Reliable human-recorded narration and instructions
- Consistent finalized Pip art and expression sets
- True sound blending / phonics progression
- Home testing, consent-aware analytics, and validated teaching outcomes