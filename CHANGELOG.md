# Changelog

All notable changes to the Apointoo integration skill (Community Edition) are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/); versions follow [SemVer](https://semver.org/).
A **major** bump = a breaking change to the integration contract (re-check your wiring); **minor** = additive
guidance; **patch** = clarifications/fixes. Each release notes the date it was verified against the live API.

## [1.0.1] — 2026-06-26
### Changed
- Repackaged under `skills/apointoo/SKILL.md` (was `apointoo/SKILL.md`) so the skill is discovered by the
  [skills.sh](https://www.skills.sh) CLI — installable via `npx skills add vizuh/apointoo-skills-ce`.
- README: added the `npx skills add` install method; fixed manual-install paths. No change to the integration contract.

## [1.0.0] — 2026-06-26
_Verified against the live Apointoo API on 2026-06-26._
### Added
- Initial public release.
- Intake API recipe — `POST /api/intake/<slug>/contact` with `X-Apointoo-Tenant-Key`, request/response shape, origin-gating note.
- Env-var contract — `APOINTOO_DASHBOARD_URL`, `APOINTOO_TENANT_SLUG`, `APOINTOO_TENANT_KEY` / `NEXT_PUBLIC_APOINTOO_TENANT_KEY`, `NEXT_PUBLIC_GTM_ID`.
- GTM / dataLayer conversion recipe — `generate_lead` with `event_id` + `transaction_id` (submissionId) for dedupe.
- Clean-integration rules + a curl/GTM-Preview verify step.
- `POLICY.md` anti-leak contribution policy; MIT license.

[1.0.1]: https://github.com/vizuh/apointoo-skills-ce/releases/tag/v1.0.1
[1.0.0]: https://github.com/vizuh/apointoo-skills-ce/releases/tag/v1.0.0
