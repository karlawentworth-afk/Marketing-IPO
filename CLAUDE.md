# clevermx site, working notes for Claude Code

This repo is the public marketing site for clevermx (thatsclevermx.com). It is a hand-written static site. No framework, no build step, HTML and CSS only, fonts loaded from Google Fonts. It deploys to Netlify by pushing to the main branch.

Read this whole file before changing anything.

## What this site is, and what it is not

It is a general marketing-operations consultancy site, with IPO readiness as the currently featured specialism. It is written to the specialism, never to a specific client.

Hard rule on confidentiality. Nothing about any specific client ever goes in this repo. No client names, no sector detail that could identify one, no IPO dates or timing, no named individuals, no deal specifics. If you are ever unsure whether something is too specific, leave it out. This matters more than any feature or any deadline.

This repo is the public site only. Do not build a private workspace, app, dashboard, login, database, form handler, or any AI feature in here. The only interaction on the site is a mailto link. If a task seems to need a backend or an app, stop and flag it rather than building it.

## Files

- index.html, the homepage. One page, five levels, dark hero, the whole story top to bottom.
- workstream-numbers.html, Workstream A, the numbers
- workstream-operations.html, Workstream B, the operations spine
- workstream-narrative.html, Workstream C, the narrative
- workstream-alignment.html, Workstream D, sales and marketing alignment
- workstream-team.html, Workstream E, team and capability
- 404.html, the not-found page

The five workstream pages share one design system and the same section spine: hero, what good looks like, the conditions, the artefacts, the evidence, the tasks, a five-page pager, a closing with the contact block, then the footer. If you build or edit a workstream page, keep that spine.

## Build status

The site is complete and already wired. All six pages are written, the five workstream pages share one design system, and index.html links its five workstream rows straight to the matching `workstream-*.html` files. There is no build step and no link fix outstanding. "Building" this site means previewing it, making content edits, and deploying. Do not add a framework, a bundler, or a backend. It is plain HTML and CSS on purpose.

## Design system, locked

Do not change these. New work matches them.

Colours:
- slate `#204640`, deep slate `#163029`, deeper slate `#0e201c`
- cream `#FAF6EC`, warm cream `#F2EBD8`
- mint `#B8E5DE`, dim mint `#98C8C0`
- gold `#B8902E`, bright gold `#D4A82E`
- ink `#1A2F2C`, soft ink `#3A4A47`, muted `#6B7A78`
- rules `#D9D2BE` and `#ECE4D0`

Type:
- Nunito for display and headings
- Source Serif 4 for body
- Section titles are a Nunito heading with one word set in italic Source Serif in gold. That is the house accent. Keep it.

Logo lockup: `that's clevermx.` with "that's" small and raised, and "mx" and the full stop in gold.

The CSS lives inline in each file. The five workstream pages share an identical `<style>` block (index.html has its own). If you change shared CSS, change it in every workstream page so they stay identical.

## House style for all copy

Easy to get wrong, so read it twice.

- Plain language. Write like a smart person talking, not like a consultancy brochure.
- No em-dashes. None. Use a full stop or a comma instead.
- No en-dashes in number ranges. Write 12-18, not 12 to 18 with a long dash.
- No emojis.
- No corporate or marketing-speak. No leverage, synergy, unlock, supercharge, seamless, world-class, or anything that smells like filler.
- No AI-tell phrasing. No "it's worth noting", "in conclusion", "delve", "tapestry", "boasts", and the rest of that family.
- Prose over bullet lists wherever prose works.
- Say less. Cut padding.

## The playbook depth dial

The workstream pages name every task in full and show the artefact, the evidence and the owner for each, then stop. They deliberately do not explain how each task is done. That is the product, sold through an engagement, not given away on the site. Keep that line. Name the work, never hand over the method. Do not add step-by-step how-to content.

## Deploy

Static site. Netlify, publish directory is the repo root, no build command. 404.html is the not-found page. Push to main to deploy.
