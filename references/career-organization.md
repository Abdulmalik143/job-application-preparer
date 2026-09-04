# Career-Track File Organization

Organize candidate-professional files automatically during workspace initialization, inside the managed `job-application-preparer/Career/` directory. This isolates the skill's work from unrelated files in the task workspace.

## Approved layout

```text
job-application-preparer/
└── Career/
    ├── Frontend-Development/
    │   ├── CV/
    │   ├── Projects/
    │   └── Certificates/
    ├── Product-Design/
    │   ├── CV/
    │   ├── Case-Studies/
    │   ├── Portfolio/
    │   └── Certificates/
    ├── Visual-Identity/
    │   ├── Projects/
    │   ├── Portfolio/
    │   └── Case-Studies/
    ├── Shared/
    │   ├── Contact/
    │   ├── Education/
    │   ├── Certificates/
    │   └── Professional-Links/
    ├── Unsorted/
    └── Archive/
```

`Unsorted` is for material that is clearly professional but cannot be assigned confidently. `Archive` is only for files the user identifies as superseded or no longer active; never archive a file merely because it is old.

## Automatic organization rules

1. Inventory the outer task workspace before moving anything. Skip the managed directory itself and exclude secrets, browser data, dependency folders, version-control internals, unrelated personal files, and unreadable binary data.
2. Create the managed directory and complete career hierarchy when they are missing.
3. Move every high-confidence candidate-professional file into its best matching destination in `Career/`. Preserve its filename and contents.
4. Move a clearly professional file with an uncertain track or purpose to `Career/Unsorted/`; do not guess a career track.
5. Leave excluded, unrelated, unreadable, sensitive, and filename-collision files in place. Do not overwrite, rename, delete, or duplicate anything. Report them in the opening summary or context map as appropriate.
6. Update `CANDIDATE_CONTEXT.md` after moving files, recording their destination, detected purpose, track, and confidence. Do not copy personal values into it.

The move is automatic because every destination is inside the skill's dedicated managed directory and the source must be classified as candidate-professional material. It does not need a separate user confirmation.

## Classification rules

- **CV:** Put role-targeted CVs in the matching track's `CV/`. When a CV is genuinely general, move it to `Career/Unsorted/` and ask the user later which track should own it rather than duplicating it.
- **Projects:** Put front-end implementation work in `Frontend-Development/Projects/`; identity deliverables in `Visual-Identity/Projects/`.
- **Product case studies:** Put documented UX, product, or interface case studies in `Product-Design/Case-Studies/`.
- **Portfolio:** Put product-design portfolios in `Product-Design/Portfolio/`; identity portfolios in `Visual-Identity/Portfolio/`.
- **Certificates:** Place track-specific certificates in the matching track. Place genuinely cross-disciplinary certificates in `Shared/Certificates/`.
- **Shared material:** Use `Shared/Education/` for education records and `Shared/Professional-Links/` for link documents or exported profile material. Do not copy contact values from private profile files into `Shared/Contact/`; move only explicit professional contact documents that are safe to organize.

If an item applies to more than one track, choose one primary destination based on its strongest evidence and record the other relevant tracks in `CANDIDATE_CONTEXT.md`. Do not duplicate it.
