# Orphan Branch Upload / Download / Delete Examples

This repository provides minimal end-to-end examples for using:

- [daiji256/upload-to-orphan-branch](https://github.com/Daiji256/upload-to-orphan-branch)
- [daiji256/download-from-orphan-branch](https://github.com/Daiji256/download-from-orphan-branch)
- [daiji256/delete-orphan-branch](https://github.com/Daiji256/delete-orphan-branch)

The pattern demonstrates how to:

1. Generate small outputs (e.g. text, JSON, images) in a workflow.
2. Persist them in a single-commit orphan branch.
3. Download them from another workflow job (or a later workflow).
4. Periodically delete old orphan branches.

## When to Use

Use this pattern when you want to keep everything entirely within GitHub (no external storage) and need a simple way to persist and later reference lightweight generated outputs across workflows. Outputs stored on an orphan branch can be directly linked or embedded in Issues, PRs, or README via raw URLs like: `https://raw.githubusercontent.com/<user>/<repo>/<branch>/<path>`.

## Notes

- Branches are single-commit; overwriting replaces the commit.
- Keep outputs small to avoid repository growth.
- Always add a retention cleanup job if you generate many branches.

## License

[MIT](LICENSE) © [Daiji256](https://github.com/Daiji256)
