# Zelfx — Landing Page

Marketing landing page for **Zelfx**, self-service walk-in printing that turns existing
printers into a scan-pay-print kiosk.

## What's here

| File | Purpose |
|------|---------|
| `index.html` | The page. Authored in [Claude Design](https://claude.ai/design) as a `.dc.html` reactive template (`<x-dc>` + a `data-dc-script` state class). |
| `support.js` | Claude Design's client runtime. Loads React (UMD) from unpkg, parses the `<x-dc>` template, and renders it. |
| `zelfx-icon-mark.png` | Logo mark used in the nav, hero poster, and favicon. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (skip Jekyll processing). |

## Running locally

The runtime fetches from a CDN, so open it over HTTP rather than `file://`:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying

Served via **GitHub Pages** from the `main` branch (root). Pushing to `main` updates the live site.

## Editing

The page content lives in `index.html` inside `<x-dc>…</x-dc>`; interactive state
(mobile menu, FAQ accordion, scroll reveals, waitlist form) is the `Component`
class in the trailing `<script type="text/x-dc" data-dc-script>` block. It can also
be re-edited in Claude Design and re-exported.
