# What I Learned in GitHub Fundamentals 🎓

> TL;DR — I can fork, clone, branch, commit, push, and open PRs with confidence. I’m still wrapping my head around rebase vs merge, squash strategies, and how protected branches + required checks interact.

---

## Highlights I’m Proud Of ✅

- Stronger Git mental model: snapshots, commit hashes, and DAGs.
- Branching habits: short-lived feature branches; keep `main` clean; use `develop` for integration.
- Commit discipline: small, atomic commits with Conventional Commits (e.g., `feat: add X`).
- Pull Requests: clear descriptions, checklists, and linking issues (e.g., `Fixes #12`).
- Issues & Projects: labels, milestones, assignees; simple Kanban for flow.
- Markdown superpowers: headers, lists, tables, task lists, code, and collapsible details.


## Still Confused / Want More Reps 🤔

1. Rebase vs merge in team settings — when is history rewrite safe vs risky?
2. Squash merge vs merge commit vs rebase-merge — pros/cons for traceability.
3. Handling merge conflicts that span many files (and binary files).
4. Protected branches — who can bypass required checks and when?
5. GitHub Actions basics — matrices, caching, workflow permissions.


## My Everyday Git Flow

```powershell
# Start a feature
git switch -c feature/my-change

# Make changes, stage, and commit
git add .
git commit -m "feat: describe change"

# Publish and open a PR
git push -u origin HEAD
# Optional (if GitHub CLI is installed):
# gh pr create --fill --web
```


## Quick Reference Table

| Concept                 | My Status         | Confidence |
|-------------------------|-------------------|------------|
| Branching               | Using daily       | 8/10       |
| PR etiquette            | Comfortable       | 8/10       |
| Rebase vs merge         | Needs practice    | 5/10       |
| Protected branches      | Basics known      | 6/10       |
| GitHub Actions          | Just starting     | 3/10       |


## Mini Checklist

- [x] Create a branch
- [x] Commit and push changes
- [x] Open a pull request
- [ ] Try an interactive rebase
- [ ] Resolve a multi-file conflict
- [ ] Set up a basic CI workflow


## Mental Model (Collapsible)

<details>
<summary>Click to expand</summary>

```
main ──●──●────●─────────●───────────▶
          \      \        \
featureA   ●──●───●─(PR)───● (merge)
featureB      ●──● (rebase) ●
```

- Keep `main` green and deployable.
- Branch off the latest `main`.
- Prefer small PRs; rebase locally to keep history tidy when appropriate.
</details>


## Notes & Reminders

> “Commit early, commit often — but keep each commit meaningful.”

- Pull before you push; resolve conflicts locally.
- Reference issues in PRs for auto-close (`Fixes #123`).
- Write READMEs for humans; automate checks for machines.


## How You Can Help Me Improve 🙏

- Share a safe, team-friendly rebase workflow.
- Examples of when squash merging caused pain (or saved the day).
- Tips for debugging tricky merge conflicts.


---

I’m following Conventional Commits for clarity.[^cc]

[^cc]: https://www.conventionalcommits.org/en/v1.0.0/
