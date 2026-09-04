# Career-Track File Organization

Use this layout only when the user explicitly asks to organize their professional files and approves a career-track structure. It is an approved preset for candidates whose work spans Front-End Development, Product Design, and Visual Identity; do not impose these tracks on a candidate whose sources or instructions do not support them.

## Approved layout

```text
Career/
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

`Unsorted` is for professional material whose role or purpose cannot be determined confidently. `Archive` is only for files the user identifies as superseded or no longer active; never archive a file merely because it is old.

## Safe organization process

1. Inventory and inspect candidate-professional files before deciding where they belong. Exclude secrets, browser data, dependency folders, version-control internals, and unrelated personal files.
2. Build a concise move plan: current path, proposed destination, detected purpose, career track, and confidence. Show ambiguous items separately.
3. Ask for confirmation of the plan before creating the directory tree or moving any existing file. The user's approval of the layout alone is not approval to move every file.
4. After confirmation, create the approved folders and move only the confirmed files. Preserve filenames, file contents, and modification times where the filesystem allows. Do not rename, overwrite, delete, or create duplicate copies.
5. Place a file in `Unsorted` only when it is clearly professional but cannot be assigned safely. Leave excluded, unrelated, unreadable, or sensitive files in place and report them without moving them.
6. Update `CANDIDATE_CONTEXT.md` with the new relative paths, detected purpose, and confidence. Do not copy personal values into it.
7. Report the completed moves, items left in place, and anything needing user review.

## Classification rules

- **CV:** Put role-targeted CVs in the matching track's `CV/`. When a CV is genuinely general, ask the user which track should own it rather than duplicating it.
- **Projects:** Put front-end implementation work in `Frontend-Development/Projects/`; identity deliverables in `Visual-Identity/Projects/`.
- **Product case studies:** Put documented UX, product, or interface case studies in `Product-Design/Case-Studies/`.
- **Portfolio:** Put product-design portfolios in `Product-Design/Portfolio/`; identity portfolios in `Visual-Identity/Portfolio/`.
- **Certificates:** Place track-specific certificates in the matching track. Place genuinely cross-disciplinary certificates in `Shared/Certificates/`.
- **Shared material:** Use `Shared/Education/` for education records and `Shared/Professional-Links/` for link documents or exported profile material. Do not copy contact values from private profile files into `Shared/Contact/`; move only explicit professional contact documents that the user wants organized.

If an item applies to more than one track, choose one primary destination based on its strongest evidence and record the other relevant tracks in `CANDIDATE_CONTEXT.md`. Do not duplicate it unless the user explicitly asks.
