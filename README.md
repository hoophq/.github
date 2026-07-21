# hoophq/.github

Org-wide GitHub configuration and workflow templates.

## Workflow templates

Reusable Actions workflows any hoophq repo can adopt from **Actions → New workflow → "By hoophq"**.

### Sync issues to Linear

`workflow-templates/linear-sync.yml`

When a new GitHub issue is opened, this creates a card in the Linear **Support** team (routed to **Triage**) and comments the Linear link back on the issue. It's **one-way and creation-only**: GitHub edits/comments/closes don't sync, and Linear discussion stays private (safe for public repos).

**Setup for a new repo:**
1. Open the repo's **Actions** tab → **New workflow**.
2. Under **By hoophq**, pick **Sync issues to Linear** → **Configure** → commit.
3. That's it. The `LINEAR_API_KEY` secret is set at the org level, so every public repo already has it.

To change the target team, state, or behavior, edit `workflow-templates/linear-sync.yml` here. Note: templates are copied into a repo at setup time, so edits here apply to repos that adopt the template *after* the change.
