# Dynamic Career-Track File Organization

Organize candidate-professional files automatically during workspace initialization inside `job-application-preparer/Career/`. Discover career tracks from the candidate's supported material; never apply a predefined set of professions, job titles, or technical domains.

## Dynamic layout

```text
job-application-preparer/
└── Career/
    ├── <Discovered-Career-Track>/
    │   ├── CV/
    │   ├── Projects/
    │   ├── Certificates/
    │   ├── Portfolio/
    │   └── Case-Studies/
    ├── <Another-Discovered-Career-Track>/
    │   └── <only relevant content folders>
    ├── Shared/
    │   ├── Contact/
    │   ├── Education/
    │   ├── Certificates/
    │   └── Professional-Links/
    ├── Unsorted/
    └── Archive/
```

Create a career-track directory only when reliable candidate evidence supports it. Create leaf folders only when relevant files exist or are needed. For example, a verified backend-focused role, project, or certificate may result in `Backend-Development/` and `Backend-Development/Certificates/`; it never appears merely because the skill assumes it.

`Unsorted` is for material that is clearly professional but cannot be assigned confidently. `Archive` is only for files the user identifies as superseded or no longer active; never archive a file merely because it is old.

## Discovering tracks

Read all relevant CVs, resumes, portfolios, project files, case studies, certificates, professional profiles, and user-provided work-history details. Identify a career track only when the same role, domain, toolset, or type of work has clear evidence. Use the candidate's own terminology where it is clear; otherwise use a concise, stable descriptive directory name.

Do not infer a track from a single keyword, a job advertisement, a generic skill list without supporting work, or the agent's installed skills. A track is about the candidate's demonstrated professional work, not the tools available to the agent.

When evidence supports several tracks, create all of them. When an item crosses tracks, select its strongest supported primary track and record the other relevant tracks in `CANDIDATE_CONTEXT.md`; do not duplicate the file.

## Automatic organization rules

1. Inventory the outer task workspace before moving anything. Skip the managed directory itself and exclude secrets, browser data, dependency folders, version-control internals, unrelated personal files, and unreadable binary data.
2. Discover the candidate's career tracks from all supported professional sources, then create only the necessary directories and content folders.
3. Move every high-confidence candidate-professional file into its best matching track and content folder. Preserve its filename and contents.
4. Put a clearly professional file with an uncertain track or purpose in `Career/Unsorted/`; do not invent a track.
5. Leave excluded, unrelated, unreadable, sensitive, and filename-collision files in place. Do not overwrite, rename, delete, or duplicate anything. Report them in the opening summary or context map as appropriate.
6. Update `CANDIDATE_CONTEXT.md` after moving files, recording their destination, detected purpose, track, and confidence. Do not copy personal values into it.

The move is automatic because every destination is inside the skill's dedicated managed directory and the source must be classified as candidate-professional material. It does not need a separate user confirmation.

## Content classification

- **CV:** Place a role-targeted CV in its matching discovered track's `CV/`. Put a genuinely general CV in `Career/Unsorted/` until the user identifies its primary track.
- **Projects, portfolio, and case studies:** Use the discovered track that best matches the work. Create `Projects/`, `Portfolio/`, or `Case-Studies/` only when those kinds of material exist.
- **Certificates:** Classify a certificate using its documented subject and the candidate evidence. A backend certificate belongs in the discovered backend track; a certificate that genuinely supports multiple tracks belongs in `Shared/Certificates/`.
- **Shared material:** Use `Shared/Education/` for education records and `Shared/Professional-Links/` for link documents or exported profile material. Do not copy contact values from private profile files into `Shared/Contact/`; move only explicit professional contact documents that are safe to organize.
