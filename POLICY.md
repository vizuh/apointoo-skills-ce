# Contribution & publishing policy

This repo is **public-ready**. Treat everything in it as if it were already public — anything merged
here may be made public at any time. The goal is to make it easy for **any developer** to integrate
Apointoo into their project, and nothing more.

## NEVER add (these leak internals)

- **Account identifiers:** Google Ads MCC / customer IDs, conversion-action IDs, GTM container IDs,
  tenant keys, API secrets, OAuth client ids.
- **Names:** client / customer / partner / person names; internal email addresses.
- **Internal references:** repo paths, `file:line` citations, commit SHAs, migration numbers,
  ticket / issue / PR numbers, internal doc names.
- **Product architecture internals:** the offline-conversion upload mechanics (Data Manager vs Ads
  API), the conversion-event ledger, per-event action mapping, tenant-store internals, MCC topology.
- **Security-guardrail specifics:** exact rate-limit numbers, the key-hashing scheme, the
  origin-allowlist implementation. (A general "intake is rate-limited and origin-gated" is fine;
  the exact mechanics are not — they help attackers more than integrators.)

## ALLOWED (the point of this repo)

- The public HTTP **intake contract** (endpoint, header name, request/response shape).
- The **dataLayer event contract** for conversion tracking.
- **Env-var names** and configuration conventions.
- "Get your slug + publishable key from your Apointoo dashboard."
- General, vendor-neutral best practices (GTM-only tracking, env-driven config, consent, dedupe).

## When in doubt, leave it out.

The full internal skill — with operational depth — lives in the private `vizuh/apointoo-skills`.
