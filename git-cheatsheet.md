# Git / GitHub cheatsheet (for someone coming from Dropbox)

## The one rule that matters in cloud sessions

The cloud session runs in a throwaway container. **If it isn't pushed to
GitHub, it does not exist.** Dropbox saved continuously; GitHub only ever
receives what you explicitly push.

## Translation table

| Dropbox idea              | Git / GitHub equivalent                           |
|---------------------------|---------------------------------------------------|
| Your synced folder        | Your *clone* (a local copy of the whole history)  |
| Dropbox's servers         | GitHub (the "remote", nicknamed `origin`)         |
| Automatic sync            | `git push` — manual, on purpose                   |
| Version history sidebar   | `git log` — the main event, not a side feature    |
| Copying a folder to experiment | A *branch* — free, tracked, throwaway        |
| (no equivalent)           | A *commit* — a labelled snapshot you choose to take |
| (no equivalent)           | A *pull request* — "please review and merge this" |

## The five commands that cover 95% of use

    git status                      # what's changed, where am I
    git add .                       # stage everything for the next snapshot
    git commit -m "message"         # take the snapshot, locally
    git push -u origin <branch>     # send it to GitHub
    git log --oneline               # list the snapshots

## The normal workflow

1. Start on a branch that isn't `main`.
2. Make changes.
3. Commit them (one commit per logical change, not one per file).
4. Push the branch to GitHub.
5. Open a pull request so the change can be reviewed before it joins `main`.
6. Merge the pull request. The branch's work is now part of `main`.
7. Delete the branch. Its commits live on in `main`.

## Useful to know

- A commit is a snapshot of the *whole project*, not of one file.
- Commits are cheap and local. Push is the networked, public step.
- `main` is just a branch — the one everyone agrees is the real version.
- Nothing is lost by committing. Things are lost by *not* committing.
