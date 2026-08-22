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

**Terminology:** when Vinícius says "career hub," he means the **whole workspace** — the hub repo plus all its sovereign children (this repo, `fishraposo.github.io`, the templates kit, the private business-portfolio with MINS nested inside, and the `Portfolio Projects/` finalization queue, which includes `aria-agent`). Do **not** restore or use the old retired `career-hub-legacy` repo (the pre-2026-07 job-hunting one).

**Era note (2026-08-11):** the workspace pivoted — everything is reference, not canon; there is no "north star" repo. The working pair is `IDENTITY.md` (who — the ikigai keystone) + `career-strategy/` (what/how — the operating layer) at the hub root. The old identity canon lives at `archive/career/`; the old `career/` directory path no longer exists.

The README is a living document. Keep it current with:
- Positioning — lead with the operator statement ("I build the systems that work while you don't") and the **personal expert brand**: AI reliability, systems engineering, and serious AI-assisted development (per `IDENTITY.md` §4 — never a three-domain worldview lead on a professional surface).
- Honest status (Shipped / Building / Designed / Consolidated); cited proof (WCP V5 and canonical ARIA) and the Expat Money anchor in a separate "shipped" context. Absorbed repositories are lineage, not independent flagships.
- Links to portfolio, LinkedIn, Upwork

**Status (2026-08-22):** synced to the shipped 2026-08-22 CVs (`career-strategy/cv/` in the hub) — added the "Now: Founding Engineer at Zap Viagens" line and corrected the Expat Money claim to the CV's wording (90% content-cost reduction, 50% faster content production; 2022–2025, created and led the AI function). Prior status: the README leads with canonical ARIA; mini-agent appears only as consolidated lineage. The unpublished Article 2 tease was removed from the writing line 2026-08-13 — the Article 1 mention stays. ARIA now lives in the hub's `Portfolio Projects/` finalization queue; the two permanent public-face repos are this one and `fishraposo.github.io`. Never copy private strategy details into this public repo.

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
- mini-agent — Agent Skills capabilities consolidated into ARIA; FishRaposo/mini-agent archived on GitHub 2026-08-12 and its local clone removed after backup (de-brand commit preserved as `../archive/mini-agent-debrand-2f712cf.patch`).
- `../IDENTITY.md` + `../career-strategy/` — the hub's working pair (identity keystone + operating layer); the old `../career/` canon is at `../archive/career/`

The workspace's business-portfolio layer (private) is a reference quarry — never quoted, linked, or excerpted in this public repo.

See the workspace-root `../AGENTS.md` for how the repos relate.
