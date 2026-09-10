# skrsi.skworld.io

The landing site for **SKRSI**, the evidence-first improvement control plane for
SK software lifecycle orchestration. **SELF** means **Systematic Evaluation,
Learning, and Feedback**.

This repository holds the **website only**. It contains no runtime code, no
schemas, and no contracts.

- Custom domain (from `CNAME`): `skrsi.skworld.io`
- Upstream project: <https://github.com/smilinTux/skrsi> (Apache-2.0)
- Runtime components today: <https://github.com/smilinTux/skcapstone>
- Governance: <https://github.com/smilinTux/sk-standards>

## Posture (stated here so the repo matches what it publishes)

The published page carries this posture in the honesty banner, the meta
descriptions, the "Three things it will never do" section, and the footer. It is
repeated here deliberately.

- **SKRSI proposes; it never authorizes.** A valid SKRSI record confers no
  merge, deployment, credential, or actuation power. Feedback is proposal-only
  and routes through the adopter's existing authorization gates.
- **It cannot approve its own work.** Producer and independent evaluator
  identities must differ, enforced through an ordered, unique evaluation
  participant tuple.
- **An inconclusive experiment stays inconclusive.** No model, agent, or
  operator can relabel it as successful.
- **Documentation-first, and it says so.** Runtime components remain in
  SKCapstone until a governed extraction card moves them.
- **Improvement is never inferred from throughput alone.** Quality, security,
  reviewer independence, and missingness remain gates.
- **Canonical naming.** The readable name is "SK Recursive SELF Improvement".
  The canonical expansion is "SK Recursive Systematic Evaluation, Learning, and
  Feedback Improvement". Runtime identifiers stay lowercase `skrsi`.

## Layout

```
index.html      the page
style.css       the only stylesheet
CNAME           custom domain for GitHub Pages
.nojekyll       serve files verbatim, no Jekyll processing
robots.txt      crawler policy, AI crawlers explicitly welcomed
sitemap.xml     single-URL sitemap
llms.txt        machine-readable summary for language models
og-image.svg    social card source
og-image.png    social card, 1200x630, referenced by og:image
```

## Hosting

GitHub Pages, classic branch-based deploy from `main` at the repository root.
No Actions workflow deploys this site; `validate-site` only checks it.

DNS is Cloudflare. The record is a **DNS-only** (unproxied) `CNAME` from
`skrsi` to `smilintux.github.io`, which is what lets GitHub issue the
certificate and lets Pages enforce HTTPS. A proxied record breaks HTTPS
enforcement on Pages.

## Local preview

```bash
python3 -m http.server 8080
# then open http://localhost:8080/
```

## CI

- `validate-site`: confirms `CNAME` and `.nojekyll` exist, checks HTML
  well-formedness with the Python standard library, and verifies every internal
  link and anchor resolves.
- `secret-scan`: runs the pinned gitleaks binary over the full history.

License: Apache-2.0.
