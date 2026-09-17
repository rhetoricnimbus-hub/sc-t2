# Shining Cloud — Proposals Desk

Presentation site for the voice-driven proposal tool.

## Pages

| File | What it is |
|---|---|
| `index.html` | Public overview — the concept, the process, the stack, the release tracker |
| `how-it-works.html` | Internal briefing — the eight steps, what is proven and what is not |
| `roadmap.html` | Interactive route map of the automation programme |

Three self-contained HTML files. No build step, no dependencies, no node_modules.
Fonts come from Google Fonts; the logos and the render clip are embedded in the files.

## Run locally

Open `index.html` in a browser. That is all.

## Deploy to Vercel

    git init
    git add .
    git commit -m "Shining Cloud proposals site"
    git branch -M main
    git remote add origin https://github.com/<you>/<repo>.git
    git push -u origin main

Then at vercel.com: **Add New → Project → Import** the repo.
Framework preset **Other**, build command **empty**, output directory **./**. Deploy.

Or straight from this folder, without GitHub:

    npx vercel --prod

## Before it goes public

- `how-it-works.html` is written for an internal audience — it states plainly
  what has not been verified yet. Rename it to something unguessable, or leave
  it out of the deploy, if the site is shown to clients.
  If you rename it, update the links in `index.html` and `roadmap.html`.
- `index.html` links to the live app at `shining-cloud-v2.onrender.com`.
  That app should stay behind its Google sign-in and address allowlist.

## Editing

Everything lives in one `<style>` block and one `<script>` block per file.

- Colours and type: the `:root`, `[data-theme="light"]` and `[data-theme="dark"]`
  blocks at the top of each file.
- Roadmap stops: the `S` array in `roadmap.html`.
- Release tracker: the `.vrow` markup in `index.html`.
- Pipeline steps: the `S` array in `index.html`.
