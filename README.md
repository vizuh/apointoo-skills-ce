# apointoo-skills-ce

**Community Edition** of the Apointoo integration skill for [Claude Code](https://claude.com/claude-code) —
a focused, vendor-neutral guide that lets any developer wire **Apointoo** (booking / lead capture +
conversion tracking) into any project by calling the skill.

> Private for now; **built public-ready**. What may be added here is governed by [`POLICY.md`](POLICY.md).

## What it covers

- Sending leads to the Apointoo **intake API** (language-agnostic HTTP).
- The **env-var** contract for configuring a tenant.
- Firing conversions cleanly via **GTM + dataLayer** (no hardcoded gtag/fbq).
- A verify step.

It does **not** contain Apointoo internals (architecture, account IDs, security mechanics) — see `POLICY.md`.

## Install

```bash
ln -s "$(pwd)/apointoo" ~/.claude/skills/apointoo
```
…or copy `apointoo/` into a project's `.claude/skills/`. Then ask Claude to
*"use the apointoo skill"* / *"add Apointoo to this project"*.

## Prerequisites

An Apointoo account with a tenant. Get your **slug** and **publishable key** from your
Apointoo dashboard, and add your site's origin to the tenant's allowed origins.

## Updates & versioning

Versioned with [SemVer](https://semver.org/) — see [`CHANGELOG.md`](CHANGELOG.md). The current version and
the date it was last verified against the live Apointoo API are stamped at the top of
[`apointoo/SKILL.md`](apointoo/SKILL.md). To stay current, **watch this repo's Releases** or `git pull`.
A **major** version bump signals a breaking change to the integration contract — re-check your wiring.

## License

MIT — see [`LICENSE`](LICENSE).

---
Vizuh devs: the full internal skill (operational depth) is the private `vizuh/apointoo-skills`.
