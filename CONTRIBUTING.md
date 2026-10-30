# Contributing to Sphynx

Pre-launch, so this is short on purpose. It will grow with the code.

## Right now

The product repositories are private until the first release. The landing page is open:

- typo and copy fixes: send a pull request
- accessibility or performance fixes on the site: send a pull request
- anything about the scoring service, widget or XDP layer: open an issue to discuss first

## Ground rules

1. **Security first.** If you find a vulnerability, do not open a public issue — read
   [SECURITY.md](https://github.com/sphynxHQ/.github/blob/main/SECURITY.md).
2. **One change per pull request.** A PR that fixes a typo and reformats a file will be asked
   to split.
3. **No new dependencies without a reason.** The landing page ships zero third-party requests;
   keep it that way. Anything added to the product has to justify its weight and its licence.
4. **Match the house style.** Plain prose in docs, lowercase in code identifiers, no emoji in
   commit messages.
5. **Tests come with the code.** A behaviour change without a test is not finished.
6. **Licence check.** The landing page is Apache-2.0. Product licences are decided before the
   first public PR lands; contributions after that point are accepted under the same licence.

## Commit messages

    component: what changed

    Why it changed, in one or two sentences if the title is not enough.

Examples: `landing: fix email field on iOS Safari`, `scorer: reject payloads without schema version`.

## Review

Two things matter here more than usual: **false positives** (a real user blocked is worse than a
bot let through) and **latency** (the widget must stay under its budget). A PR that improves
detection but breaks either one gets sent back.

## Questions

[help@sphynx.site](mailto:help@sphynx.site)
