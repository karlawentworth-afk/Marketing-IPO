# clevermx

Public marketing site for clevermx. Static HTML and CSS, no build step, deploys to Netlify.

## Run it locally

Open index.html in a browser, or serve the folder:

    python3 -m http.server 8000

then visit http://localhost:8000

## Structure

- index.html, homepage
- workstream-numbers.html, A, the numbers
- workstream-operations.html, B, the operations spine
- workstream-narrative.html, C, the narrative
- workstream-alignment.html, D, sales and marketing alignment
- workstream-team.html, E, team and capability
- 404.html, not-found page

## Deploy

Push to main. Netlify builds nothing and publishes the repo root.

## Before editing

Read CLAUDE.md. It holds the locked design system, the house style rules, the playbook depth dial, and the confidentiality rule that keeps client detail off the public site.
