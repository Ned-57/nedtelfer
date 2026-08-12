# nedtelfer.com

Personal site for Ned Telfer — a CV and portfolio aimed at job applications, plus a couple of small self-contained projects.

Not to be confused with [telfardo.com](https://telfardo.com), which is the freelance business. Different audience, different pitch: this site is written for recruiters and hiring managers, so keep career positioning here and client-facing sales copy there.

## What's in it

| Path | What it is |
| --- | --- |
| `index.html` | The CV: profile, experience, education, contact. The page people are actually sent to. |
| `wordlescape/` | Wordlescape — a daily OSRS-themed Wordle. Self-contained game with its own icon set in `wordlescape/icons/`. |
| `circus-performer/` | A one-page joke site. |

## Stack

Plain, deliberately. There is **no build step, no package manager and no dependencies to install** — every page is a single HTML file with its CSS in one `<style>` block and its JavaScript in one `<script>` block.

The only external requests are Google Fonts, and links out to GitHub and LinkedIn. Nothing else is fetched at runtime.

## Running it locally

Open the file:

```bash
start index.html
```

That works for everything except paths — links between pages assume they're served from a web root. If you're testing navigation, serve the folder instead:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Editing

Because each page is one file, edits are direct: find the section in the HTML and change it. There is no templating, so anything appearing on more than one page — the nav, the footer year — has to be changed in each file that uses it.

Two things worth keeping consistent when editing `index.html`:

- **Dates and tenure.** The intro paragraph states a number of years of experience. If a role's dates change, check that sentence still adds up — it has contradicted the experience list before.
- **Job titles.** The experience entries carry official job titles; the intro describes the discipline. Those are allowed to differ, but neither should drift into something that wasn't the case.

## Deployment

Hosted on **Netlify**, deployed automatically from `main`. There's no `netlify.toml` — the build settings live in the Netlify UI, and since there's no build step it just publishes the repository root. Pushing to `main` is a deploy.

## Domain

`nedtelfer.com`, served over HTTPS by Netlify.
