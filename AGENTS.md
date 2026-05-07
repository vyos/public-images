# AGENTS.md

## Project purpose

Public metadata/landing repo for "publicly available rolling and stream release images" of VyOS. Created 2025-02-13. Currently contains only `README.md` — no build scripts, no workflows, no Debian packaging. Acts as a discoverable URL for image-distribution metadata.

## Tech stack

- None. Markdown only.

## Build / test / run

Nothing to build. Edit `README.md` and push.

## Repository layout

- `README.md` — single-line description ("Publicly available rolling and stream release images").

## Cross-repo context

Companion to `vyos/vyos-nightly-build` (the actual ISO-build scheduler that signs and publishes nightly images via GitHub Releases) and `VyOS-Networks/vyos-stream-builds` (the rolling/sagitta/circinus stream pipelines). Image publication itself lives elsewhere — this repo is the user-visible front door.

## Conventions

- Default branch `main` (not `current`).
- Commit / PR title format: `component: T12345: description` (Phorge task ID at https://vyos.dev) when the repo gets real content; today no PR-message workflow is configured.
- Public visibility — keep contents non-sensitive.

## Mirror relationship

No mirror twin. Lives only in `vyos`.

## Notes for future contributors

- This is effectively a placeholder. If image-distribution metadata (manifests, signing keys, release notes) is to live in git, this is the natural home — but coordinate with `vyos-nightly-build` (which already publishes minisign-signed releases) before duplicating.
- No branch protection on default branch (audit baseline 2026-04-18). Treat any new content as needing fresh repo settings.
