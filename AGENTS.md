# Home repo

This is my **home repo** for running coding agents across projects (inspired by Matt Pocock’s “Home Repo” pattern). Run agents from this repo.

- **Shared config/docs:** agent skill setup lives here in `AGENTS.md` and `docs/agents/`.
- **Repo index:** other repos are listed below as sibling checkouts under `~/Repos` (`/home/mende/Repos`). Use this to resolve a repo named in conversation.
- **Working in another repo:** `cd` to its local path (or open it). If it’s missing, clone it from the listed remote into `~/Repos`. Before changing a child repo, read its `AGENTS.md`/`CLAUDE.md` (if present) and follow its conventions.

## Agent skills

### Issue tracker

GitHub Issues for `Mende/dev-home` (via `gh`). See `docs/agents/issue-tracker.md`.

### Triage labels

Default canonical triage label vocabulary (label string = role name). See `docs/agents/triage-labels.md`.

### Domain docs

Single-context layout (`GLOSSARY.md` at repo root, ADRs in `docs/adr/`). See `docs/agents/domain.md`.

## Creating a new project

1. Create the repo on GitHub under `Mende` with the appropriate visibility, then clone it into `~/Repos/<name>` (e.g. `gh repo create Mende/<name> --private --clone`, run from `~/Repos`). Work from that checkout, not from `dev-home`.
2. Add the repo to the **Other repos** table below (local path, clone command, visibility, one-line description). That table is how agents resolve repo names.
3. From the new repo, run `/setup-matt-pocock-skills` and answer:
   - Issue tracker: **GitHub** — issues in GitHub Issues via the `gh` CLI.
   - Triage labels: **defaults** — `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`.
   - Domain docs: **single-context** (`GLOSSARY.md` + `docs/adr/`).
   - Agent instructions file: `AGENTS.md` (matching the other repos).
4. Commit and push the generated config so every project starts with the same agent setup.

## Other repos

Base directory: `~/Repos` (siblings next to `dev-home`, e.g. `../<repo>` from this repo).

| Repo | Local path | Clone from (if missing) | Visibility | Description |
| --- | --- | --- | --- | --- |
| [Mende/the-scribbler](https://github.com/Mende/the-scribbler) | `../the-scribbler` | `git@github.com:Mende/the-scribbler.git` | private | — |
| [Mende/lore-keeper](https://github.com/Mende/lore-keeper) | `../lore-keeper` | `git@github.com:Mende/lore-keeper.git` | private | — |
| [Mende/typing-practice](https://github.com/Mende/typing-practice) | `../typing-practice` | `git@github.com:Mende/typing-practice.git` | private | — |
| [Mende/fin](https://github.com/Mende/fin) | `../fin` | `git@github.com:Mende/fin.git` | private | — |
| [Mende/dnd-agents](https://github.com/Mende/dnd-agents) | `../dnd-agents` | `git@github.com:Mende/dnd-agents.git` | public | — |
| [Mende/Mende](https://github.com/Mende/Mende) | `../Mende` | `git@github.com:Mende/Mende.git` | public | Config files for my GitHub profile. |
