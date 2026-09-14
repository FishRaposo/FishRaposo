# AGENTS.md — FishRaposo (GitHub profile README)

**Permanent public GitHub profile README** for Vinícius Raposo / FishRaposo. This repo is the most compressed public face — a single `README.md` rendered on the GitHub profile.

## Self-sufficiency

This repo is **self-sufficient**. There is no build step, no install, and no dependency on career-hub to edit or publish.

- All changes happen **in this repository** and commit to `FishRaposo/FishRaposo`.
- **career-hub** registers this repo in `sync-repos.mjs` and clones it as a local pointer only. The hub does not own or deploy this content.

## Branch & commit boundary

- **Default branch:** `main`
- **Tracked content:** `README.md` (public copy) and this file (agent guidance).
- **Commit here, not in career-hub**, for any profile README change.

```bash
git pull --rebase origin main
# edit README.md
git add README.md   # and AGENTS.md if changed
git commit -m "[brief description]"
git push origin main
```

Never leave profile README edits uncommitted. Do not commit secrets, tokens, or private strategy details.

## Agent rules

- **English only** in tracked files.
- **Surgical README edits** — smallest change that solves the problem; no full rewrites unless the owner directs one.
- **Positioning:** keep copy aligned with the public face — applied AI reliability, production RAG and agents, deterministic scaffolding. Do not invent claims, metrics, or proof points; only reflect what is already stated or verified elsewhere.
- **No secrets** — no API keys, private emails beyond the published contact block, or hub-internal strategy in this repo.
- **No structural fiction** — do not add build commands, test suites, or dependencies that do not exist. This repo is Markdown only.

## Relationship to other public surfaces

| Surface | Role |
|---------|------|
| This repo (`FishRaposo/FishRaposo`) | Profile README — shortest public summary |
| `fishraposo.github.io` | Full portfolio catalog and project pages |
| career-hub | Private coordination; clones this repo, does not source it |

When positioning or proof copy changes, reconcile with the portfolio site and hub identity docs — but commit the README change **here**.
