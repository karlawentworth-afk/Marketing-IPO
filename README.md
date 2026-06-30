# clevermx

The clevermx website. Static HTML and CSS, no build step, deploys to Netlify.

## Structure

- index.html and root pages: the public marketing operations consultancy site (findable on Google).
- m-ipo/: a private, unlisted resource on pre-IPO marketing readiness, sent to a client by direct link. Every page is noindexed and the section is never linked from the main site.
- 404.html: site-wide not-found page.
- robots.txt: allows crawling so the noindex on /m-ipo/ is honored.

## Run it locally

    python3 -m http.server 8000

then visit http://localhost:8000 (main site) and http://localhost:8000/m-ipo/ (the section).

## Deploy

Push to main. Netlify builds nothing and publishes the repo root.

## Before editing

Read CLAUDE.md. It holds the two-part structure, the locked design system, the house style, the confidentiality rule, and the noindex rule that keeps the m-IPO section out of search.
