# Legacy bridge note

This directory is no longer the public integration surface.

Use the provider-native Codex or Claude hook configuration plus the generic local ingress:

```bash
clawhip native hook --provider codex --file payload.json
clawhip native hook --provider claude --file payload.json
```

Install provider hooks globally, let clawhip derive repo/worktree identity from git context,
and use `.clawhip/hooks/` only for additive augmentation. Legacy project-scoped hook installs
should be migrated to the global path.
