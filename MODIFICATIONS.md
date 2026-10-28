# Modifications in this fork (AGPL-3.0, section 5 notice)

This repository is a fork of [666ghj/MiroFish](https://github.com/666ghj/MiroFish)
(commit `7657031ac01184afe2cb220f5ee3545573b5e843`, 2026-10-02), licensed under the
GNU Affero General Public License v3.0. The full license is in `LICENSE`.

Purpose of the fork: run MiroFish for Brazilian Portuguese users without changing its
behaviour otherwise. Business logic of any product built around this engine lives
outside this repository and talks to it only through its HTTP API.

| Date | File | Change |
|---|---|---|
| 2026-10-28 | `locales/pt.json` | New Brazilian Portuguese translation of the UI and backend messages (based on `locales/en.json`). |
| 2026-10-28 | `locales/languages.json` | Stronger `llmInstruction` for `pt`, covering personas, posts and reports; label "Português (Brasil)". |
| 2026-10-28 | `backend/app/utils/locale.py` | Fallback locale comes from `MIROFISH_DEFAULT_LOCALE` (default still `zh`) instead of the hard-coded `zh`. |
| 2026-10-28 | `.env.example` | Documents `MIROFISH_DEFAULT_LOCALE`. |
| 2026-10-28 | `MODIFICATIONS.md` | This notice. |

Upstream remains the canonical project; this fork is published so that anyone who
interacts with a deployment of it over a network can obtain the modified source, as
required by AGPL-3.0 section 13.
