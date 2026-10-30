# nedtelfer.com

Personal site for my CV and portfolio aimed at job applications.
## What's in it

| Path | What it is |
| --- | --- |
| `index.html` | The CV: profile, experience, education, contact. The page people are actually sent to. |
| `wordlescape/` | Wordlescape — a daily OSRS-themed Wordle. Self-contained game with its own icon set in `wordlescape/icons/`. |

## Stack

Plain, deliberately. There is **no build step, no package manager and no dependencies to install** - every page is a single HTML file with its CSS in one `<style>` block and its JavaScript in one `<script>` block.

The only external requests are Google Fonts, and links out to GitHub and LinkedIn. Nothing else is fetched at runtime.

## Running it locally

Open the file:

```bash
start index.html
```

That works for everything except paths. Links between pages assume they're served from a web root. If you're testing navigation, serve the folder instead:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Editing

All pages are in one file, edits are direct: find the section in the HTML and change it.

Keeping consistent when editing `index.html`:

- **Dates and tenure.** The intro paragraph states a number of years of experience. If a role's dates change, check that sentence still adds up — it has contradicted the experience list before.
- **Job titles.** The experience entries carry official job titles; the intro describes the discipline.
## Deployment

Hosted on **Netlify**, deployed automatically from `main` upon push.

## Domain

`nedtelfer.com`, served over HTTPS by Netlify.
