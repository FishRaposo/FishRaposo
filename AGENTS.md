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

**Terminology:** when Vinícius says "career hub," he means the interconnected trio `career` + `fishraposo.github.io` + `FishRaposo`. Do **not** restore or use the old deleted `career-hub` repo as active canon.

The README is a living document. Keep it current with:
- Positioning statement — lead with the operator statement + thesis and the three-domain worldview, never a job title (per `the-core.md`)
- Kicker: "I build the systems that work while you don't."
- The **personal expert brand** — AI reliability, systems engineering, and serious AI-assisted development, shown build-in-public with honest status (Shipped / Building / Designed); cited proof (WCP V5, aria-agent) and the Expat Money anchor in a separate "shipped" context. (A Designed project links to its plan, not an empty repo; never present an empty repo as finished.)
- Links to portfolio, LinkedIn, Upwork

**Pending build step:** the live `README.md` still reflects the prior "Eight" AI repos; rebuilding it to the personal-expert-brand positioning is the open task. The surface spec lives in the workspace's private business-portfolio repo — read it there before rebuilding, and never copy private strategy details into this public repo. The formerly planned "Big 6" showcase repos are retired and will not be built; remove any claim that they are coming.

---

## Portfolio Hierarchy

```
business-portfolio (private north star — wins on conflict) → career/ (identity & voice canon) → fishraposo.github.io (polished proof) → FishRaposo/README (public face)
```

The profile README is the outermost layer — the one visible to every recruiter, client, and collaborator who visits GitHub. It should be the most concise and highest-signal representation of Vinícius.

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

These are sibling repos in the active career-hub trio, not a separate `career-hub` checkout:

- `../fishraposo.github.io/` — Portfolio (polished proof, repo showcase)
- `../career/` — Identity & voice canon (`the-core.md`, `Main Docs/`)

Above both sits the workspace's business-portfolio layer (private) — it is the north star and wins on conflict, but is never quoted, linked, or excerpted in this public repo.

See the workspace-root `../AGENTS.md` for how the repos relate and which layer wins on conflict.
