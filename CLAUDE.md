# clevermx site, working notes for Claude Code

This repo is the clevermx website. It is a hand-written static site. No framework, no build step, HTML and CSS only, fonts loaded from Google Fonts. It deploys to Netlify by pushing to the main branch.

Read this whole file before changing anything.

## Two parts of the site

1. The main site, at the repo root (index.html, plus any pages added beside it). This is the public clevermx marketing operations consultancy site. It is meant to be found on Google. It is allowed to have calls to action and a contact link, because it is the consultancy's own site. Its copy is an early draft and is being shaped, so do not rewrite its positioning unless asked.

2. The m-IPO section, in /m-ipo/. A private, unlisted resource on pre-IPO marketing readiness, sent to a client by direct link. Rules for it:
   - Every page carries `<meta name="robots" content="noindex, nofollow">`. It is already there. Do not remove it.
   - Never link to it from the main site or its menu.
   - It keeps its own tab-strip navigation internally. Its logo links back up to the main site at "/".
   - No calls to action, no promotion, no contact pitch inside /m-ipo/. It is a learning resource, not a sell.

## Confidentiality, applies everywhere

Nothing about any specific client ever goes anywhere in this repo. No client names, no identifying sector detail, no IPO dates or timing, no named individuals, no deal specifics. The m-IPO section is sent to a client but is written generally, to the specialism, never about them. If unsure whether something is too specific, leave it out. This matters more than any feature or deadline.

## Indexing

Crawling is allowed in robots.txt on purpose, so the noindex tag on the /m-ipo/ pages is actually seen and obeyed. Do not disallow /m-ipo/ in robots.txt: a blocked page cannot have its noindex read, and the URL could still surface in search. The mechanism that keeps m-IPO private is the noindex tag plus never linking to it. Keep both. Note this is obscurity, not access control. If real privacy is ever needed, that is a sign-in and a separate build.

## Design system, locked (both parts share it)

Do not change these. New work matches them.

Colours: slate `#204640`, deep slate `#163029`, deeper slate `#0e201c`, cream `#FAF6EC`, warm cream `#F2EBD8`, mint `#B8E5DE`, dim mint `#98C8C0`, gold `#B8902E`, bright gold `#D4A82E`, ink `#1A2F2C`, soft ink `#3A4A47`, muted `#6B7A78`, rules `#D9D2BE` and `#ECE4D0`.

Type: Nunito for display and headings, Source Serif 4 for body. Section titles are a Nunito heading with one word set in italic Source Serif in gold. That is the house accent. Keep it.

Logo lockup: `that's clevermx.` with "that's" small and raised, and "mx" and the full stop in gold. Text lockup for now. If a real logo asset is supplied, replace the lockup in the nav and footer of every page and keep it consistent.

## House style for all copy

- Plain language. Write like a smart person talking, not like a consultancy brochure.
- No em-dashes. None. Use a full stop or a comma.
- No en-dashes in number ranges. Write 12-18.
- No emojis.
- No corporate or marketing-speak. No leverage, synergy, unlock, supercharge, seamless, world-class.
- No AI-tell phrasing. No "it's worth noting", "in conclusion", "delve", "tapestry", "boasts".
- Prose over bullet lists wherever prose works. Say less.
- The main site may use calls to action. The m-IPO section may not.

## m-IPO navigation

Every /m-ipo/ page carries one persistent tab strip in the sticky header: Overview, then A to E with their short names, current tab marked. Identical on all six pages, horizontally scrollable on narrow screens, with a tiny inline script that scrolls the active tab into view. Keep it identical everywhere. No navigation block at the bottom of pages.

## How the numbers nest (m-IPO)

The numbers have to nest, not compete. There are 8 workstreams in an IPO. Marketing is 1 of them. Marketing divides into 5 workstreams, A to E. Every task is judged by the same 3 questions: what artefact, what evidence, who owns it. Keep to 8, 5 and 3. Do not reintroduce headline counts like "eight conditions", "six artefacts" or "seven tasks".

## Build and deploy

Static site. Netlify, publish directory is the repo root, no build command. 404.html at the root is the not-found page. Push to main to deploy.
