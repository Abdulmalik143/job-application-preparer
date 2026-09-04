# Managed Workspace Directory

The task workspace may contain unrelated files. To keep this skill self-contained, use one fixed managed directory at the workspace root:

```text
job-application-preparer/
```

This directory is candidate data created by the skill; it is not the installed skill folder. If `job-application-preparer/` already exists as a directory, use it. If it does not exist, create it before creating local profile files or organizing candidate materials. If an item with that name exists but is not a directory, stop and ask the user to resolve the naming conflict.

## Required contents

Keep all skill-created local files and the career hierarchy inside this directory:

```text
job-application-preparer/
├── CANDIDATE_CONTEXT.md
├── APPLICATION_PROFILE.md
├── EXPERIENCE_PROFILE.md
├── APPLICATION_TRACKER.md
└── Career/
```

All references to these Markdown files in this skill mean the copies at these managed paths. Source-file paths recorded in `CANDIDATE_CONTEXT.md` remain relative to the outer task workspace so they can be located reliably.

## Initialization and safety

Starting this skill authorizes creation of the managed directory, its local Markdown files, and the approved `Career/` structure. It also authorizes moving only candidate-professional files that have been confidently classified into the managed career structure.

Never move or inspect credentials, secrets, browser profiles, caches, dependency directories, version-control internals, unrelated personal files, or unreadable binary files merely because they are beside candidate files. Leave them outside the managed directory and record only their path and exclusion reason in the context map when relevant.

Do not overwrite an existing destination. If a filename collision or uncertain classification prevents a safe move, leave the source in place and report it for user review. Do not create duplicate copies.

If the task workspace uses Git, keep the whole `job-application-preparer/` directory untracked by adding the exact directory name to the local `.git/info/exclude`. Do not alter a shared `.gitignore` automatically.
