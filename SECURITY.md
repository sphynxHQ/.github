# Security policy

Sphynx is a security product, so reports about it get priority over everything else.

## Reporting a vulnerability

Email **security@sphynx.site**. If that address is not yet live, use **help@sphynx.site** and
put `SECURITY` in the subject line.

Do not open a public issue, and do not test against sites you do not own.

Include, as far as you know it:

- what you found and the impact you think it has
- affected repository and version or commit
- the smallest reproduction you can manage
- whether the issue is already public anywhere

If you want to encrypt the report, ask for a PGP key in your first message and we will reply
with one.

## What to expect

| Stage | Target |
|---|---|
| Acknowledgement | within 3 working days |
| Initial assessment (real bug / not / needs info) | within 10 working days |
| Fix or mitigation plan for confirmed issues | within 30 days for critical, 90 days otherwise |
| Public disclosure | coordinated, after a fix ships, with credit if you want it |

## In scope

- the landing site and its signup endpoint (`sphynxHQ/landing`)
- the scoring service and its API (when published)
- the JS widget and challenge page (when published)
- the site-key and token model: forgery, replay, key confusion, origin bypass
- the XDP layer: rule injection, map exhaustion, bypass (when published)

## Out of scope

- findings that require a compromised device or a rooted browser
- volumetric or layer-3/4 DDoS, and reports that only say "you got flooded"
- missing headers on pages that serve no user data, unless they enable a concrete attack
- email spoofing of `@sphynx.site` (SPF, DKIM and DMARC are configured on the zone)
- social engineering of maintainers
- automated scanner output with no demonstrated impact

## Safe harbour

Testing your own installation, or a demo instance we point you at, is authorised. We will not
pursue legal action for research that stays within this policy, avoids privacy violations,
avoids degrading service for others, and is reported to us before it is published.

## No bug bounty

There is no paid bounty at this stage. Confirmed reporters get credit in the release notes
unless they ask otherwise.
