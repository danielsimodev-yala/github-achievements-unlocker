# GitHub Achievements Unlocker

Automatically unlock GitHub profile achievements using a single GitHub Actions workflow — no manual steps required after setup.

---

## Achievements Unlocked

| Achievement | Description |
|---|---|
| **YOLO** | Merged a pull request without a code review |
| **Quickdraw** | Closed a pull request within 5 minutes of opening |
| **Pull Shark** | Opened pull requests that got merged (×2, ×16 tiers) |
| **Pair Extraordinaire** | Co-authored commits included in merged pull requests |

---

## How It Works

The workflow runs entirely inside GitHub Actions:

1. Ensures the repository has an initial commit (handles empty repos)
2. Creates a new branch, appends a log entry, and commits with a `Co-authored-by` trailer
3. Opens a pull request and immediately merges it without requesting a review
4. Repeats 10 times — covering all four achievements in one run

---

## Setup

### 1. Fork or create a new public repository

Achievements only count on **public** repositories.

### 2. Add the workflow file

If setting up manually, create `.github/workflows/achievements.yml` with the contents from this repo, then commit it.

If you cloned or forked this repo, the file is already in place.

### 3. Run the workflow

Go to the **Actions** tab → select **Unlock GitHub Achievements** → click **Run workflow**.

The workflow takes about 1–3 minutes to complete.

---

## Requirements

- Public repository
- No branch protection rules on `main` (default for new repos)
- GitHub Actions enabled (enabled by default)

No secrets or tokens need to be configured — the workflow uses the built-in `GITHUB_TOKEN`.

---

## Notes

- Achievements may take a few hours to appear on your GitHub profile
- Running the workflow multiple times is safe — branch names are timestamped to avoid conflicts
- The `Co-authored-by` line uses a placeholder user; replace it with a real GitHub account email if you want the co-authorship to reflect on another profile

---

## License

MIT
