# n2medical-website

The static company website for **N2 Medical Ltd** — a single self-contained `index.html` with no
build step, no dependencies and no framework, deployed via GitHub Pages on a custom domain.

**Read `README.md` first.** It carries the deployment recipe, the two registered domains and their
registrars, and the staged registered-office privacy fix that the site footer depends on.

## Layout

```
n2medical-website/
├── index.html   the whole site — HTML, CSS and any script inline
├── CNAME        the one canonical custom domain GitHub Pages serves
└── README.md    domains, DNS records, deploy steps, the privacy to-do
```

## Editing

- Edit `index.html` directly. Everything is inline by design so the page stays a single artefact.
- UK English throughout. No emojis.
- GitHub Pages takes **one** canonical domain (the `CNAME`); the second domain 301-redirects to it.

## Do not change the footer address on its own

The footer shows the company's registered office, which it must by law (Companies (Trading
Disclosures) Regulations 2008). Any change is made at Companies House first and in the footer last.
The plan is in `docs/` — git-ignored, in the store, and not for this public repository.

## Done when

type: project

- [x] Single self-contained page written and deployed via GitHub Pages
- [x] Both company domains registered for a ten-year term
- [ ] Canonical domain serving over HTTPS, with the second domain redirecting to it
- [ ] Enquiries pointed at a mailbox on the company domain rather than a personal address
- [ ] Registered office moved to a service address, then the footer updated to match
