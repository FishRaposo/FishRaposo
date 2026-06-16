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
- Positioning statement — lead with the operator statement + thesis, never a job title (per doc1 §0)
- Kicker: "I build the systems that work while you don't."
- Top skills (production AI systems, reliability, evaluation, observability)
- Key project highlights with links to live demos/repos
- Links to portfolio, LinkedIn, Upwork

---

## Portfolio Hierarchy

```
career (positioning + strategy) → fishraposo.github.io (polished proof) → FishRaposo/README (public face)
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
- `../career/` — Positioning source of truth (`POSITIONING.md`, `Main Docs/`)

See the workspace-root `../AGENTS.md` for how the three repos relate and which layer wins on conflict.
