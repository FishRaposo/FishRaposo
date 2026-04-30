# AGENTS.md — FishRaposo GitHub Profile

**This is the GitHub profile README repo.** The `README.md` file is the public GitHub profile page — what visitors see at github.com/FishRaposo. It is a sales and credibility document, not a code repository.

---

## Git Sync Rule

Pull at start of every session, push at end.

```bash
git pull --rebase origin master  # start
git add -A && git commit -m "[description]" && git push  # end
```

---

## What This Repo Is

- **README.md** — The GitHub profile page. Lives at the root. Displayed on the public GitHub profile.
- Everything else — supporting assets (badges, icons, images) referenced by README.md.

The README is a living document. Keep it current with:
- Current role / positioning statement
- Top skills (AI Infrastructure, systems, reliability)
- Key project highlights with links to live demos/repos
- Links to portfolio, LinkedIn, Upwork
- GitHub stats (stars, commits, contribution graph)

---

## Portfolio Hierarchy

```
unified-memory (raw) → career-hub (curated) → fishraposo.github.io (polished) → FishRaposo/README (public face)
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

- `~/fishraposo.github.io` — Full portfolio site (fishraposo.github.io)
- `~/career-hub` — Career engine (proposals, bios, content)
- `~/unified-memory` — System memory (events, strategy, lane specs)
