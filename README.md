# n2medical-website

Static company site for **N2 Medical Ltd** — single self-contained `index.html`.
Deployed via GitHub Pages with a custom domain.

## Domain

Both registered 2026-07-05 for a **10-year term** (expire ~2036-07):

- **`n2medical.uk`** — registrar **Cloudflare** (same account as `skeletalsurgery.com`; DNS native to Cloudflare)
- **`n2medical.co.uk`** — registrar **Gandi.net** (DNS at Gandi, or delegate nameservers to Cloudflare for one dashboard)
- **Company:** N2 Medical Ltd — Companies House **10631273**

GitHub Pages takes **one** canonical custom domain (the `CNAME`); the other
should 301-redirect to it. Decide which is primary (see below), then point the
canonical domain's DNS at GitHub Pages and set up a redirect on the other.

## Deploy
1. Push to the `n2medical-website` GitHub repo.
2. Settings > Pages > deploy from `main` (root).
3. Set the custom domain to `n2medical.uk` (writes `CNAME`, provisions HTTPS).
4. Add DNS records (at Gandi, or Cloudflare if delegated):
   - Apex `n2medical.uk` — four A records:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `www` — CNAME → `nigelgummerson.github.io`
   - If using Cloudflare: set these **DNS only (grey cloud)**, not proxied.
5. Tick **Enforce HTTPS** in GitHub Pages once the certificate provisions.

## Contact

Site enquiries currently point to `skeletalsurgery@icloud.com`; swap for an
`@n2medical.uk` mailbox once email is set up on the domain.

## Registered office in the footer

The footer shows the company's registered office, as the Companies (Trading
Disclosures) Regulations 2008 require. If the registered office changes,
update it at Companies House first and the footer second; the footer must match
the register at all times. The plan for that change is kept in `docs/`
(git-ignored, in the store).
