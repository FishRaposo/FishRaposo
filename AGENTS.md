# AGENTS.md — FishRaposo GitHub Profile

**This is the GitHub profile README repo.** The `README.md` file is the public GitHub profile page — what visitors see at github.com/FishRaposo.

---

## Git Sync Rule

Pull at start of every session, push at end.

```bash
git pull --rebase origin main  # start
git add -A && git commit -m "[description]" && git push  # end
```

---

## What This Repo Is

- **README.md** — The GitHub profile page. Lives at the root. Displayed on the public GitHub profile.
- Everything else — supporting assets (badges, icons, images) referenced by README.md.

**Terminology:** when Vinícius says "career hub," he means the **whole workspace** — the hub repo plus all its sovereign children (this repo, `fishraposo.github.io`, `mini-agent`, the templates kit, and the private business-portfolio with MINS nested inside). Do **not** restore or use the old retired `career-hub-legacy` repo (the pre-2026-07 job-hunting one).

**Era note (2026-08-11):** the workspace pivoted — everything is reference, not canon; there is no "north star" repo. The working pair is `IDENTITY.md` (who — the ikigai keystone) + `career-strategy/` (what/how — the operating layer) at the hub root. The old identity canon lives at `archive/career/`; the old `career/` directory path no longer exists.

The README is a living document. Keep it current with:
- Positioning — lead with the operator statement ("I build the systems that work while you don't") and the **personal expert brand**: AI reliability, systems engineering, and serious AI-assisted development (per `IDENTITY.md` §4 — never a three-domain worldview lead on a professional surface).
- Honest status (Shipped / Building / Designed); cited proof (WCP V5, aria-agent, mini-agent) and the Expat Money anchor in a separate "shipped" context. (A Designed project links to its plan, not an empty repo; never present an empty repo as finished.)
- Links to portfolio, LinkedIn, Upwork

**Status (2026-08-11):** the README was rebuilt around applied AI reliability — the operator statement + field lead replaces the three-domain worldview lead, mini-agent is in the proof list, the article series is mentioned. Remaining storefront items live in the hub's `career-strategy/06-github-audit.md` queue: the Command Code mods repo, GitHub-side repo archiving, and pins (owner UI actions). Never copy private strategy details into this public repo.

---

## Ordering (pivot era)

```
owner's current instructions → live repo state → IDENTITY.md + career-strategy/ → Business Portfolio/ (quarry) → archive/
```

The profile README is the outermost public layer — the one visible to every recruiter, client, and collaborator who visits GitHub. It should be the most concise and highest-signal representation of Vinícius.

---

## How to Update

The README uses markdown. No build step. Edit directly and push.

When updating:
- Keep it scannable (top 5 seconds must communicate value)
- Lead with proof, not description
- Link out to the portfolio (fishraposo.github.io) for details
- Keep skills section aligned with current positioning

---

## Related Repos

These are sibling repos in the workspace, not a separate `career-hub` checkout:

- `../fishraposo.github.io/` — Portfolio (polished proof, repo showcase)
- `../mini-agent/` — the hiring artifact (public)
- `../IDENTITY.md` + `../career-strategy/` — the hub's working pair (identity keystone + operating layer); the old `../career/` canon is at `../archive/career/`

The workspace's business-portfolio layer (private) is a reference quarry — never quoted, linked, or excerpted in this public repo.

See the workspace-root `../AGENTS.md` for how the repos relate.
