# Security Policy

This repository contains the **website only** for `skrsi.skworld.io`. It holds
no cryptographic code, no credentials, no runtime service, and no network
surface of its own.

## Reporting a vulnerability

Report privately through GitHub Security Advisories on the upstream project:

<https://github.com/smilinTux/skrsi/security/advisories/new>

Please do not open a public issue for a security report.

## Scope

In scope for this repository:

- Content that misstates the SKRSI posture, for example a claim that SKRSI can
  authorize, merge, deploy, or actuate.
- Leaked private paths, private host names, or credentials in published files.
- Site supply chain concerns, such as an unpinned or unexpected external asset.

Out of scope here, and reportable upstream instead:

- Contract, schema, or evaluator behavior. Report those on
  <https://github.com/smilinTux/skrsi>.

## Published assets

The page loads webfonts from `fonts.googleapis.com` and `fonts.gstatic.com`.
Everything else, including all CSS, is served from this origin. There is no
analytics, no tracker, and no third-party script.
