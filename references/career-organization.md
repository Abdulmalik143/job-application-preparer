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
    │   ├── CV/
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

When evidence supports several tracks, create all of them. Most cross-track files still use one strongest supported destination, but a CV or resume that materially supports several tracks follows the special multi-track CV rules below so it is available from every relevant track without creating independent sources of truth.

## Automatic organization rules

1. Inventory the outer task workspace before moving anything. Skip the managed directory itself and exclude secrets, browser data, dependency folders, version-control internals, unrelated personal files, and unreadable binary data.
2. Discover the candidate's career tracks from all supported professional sources, then create only the necessary directories and content folders.
3. Move every high-confidence candidate-professional file into its best matching track and content folder. Preserve its filename and contents. Apply the multi-track CV procedure instead of the single-destination rule when the document substantively represents more than one discovered track.
4. Put a clearly professional file with an uncertain track or purpose in `Career/Unsorted/`; do not invent a track.
5. Leave excluded, unrelated, unreadable, sensitive, and filename-collision files in place. Do not overwrite, rename, or delete anything. The only permitted duplication is a byte-identical fallback placement for a multi-track CV when safe links are unavailable, as defined below. Report conflicts in the opening summary or context map.
6. Update `CANDIDATE_CONTEXT.md` after moving files, recording their canonical destination, visible placements, detected purpose, supported tracks, specialization status, and confidence. Do not copy personal values into it.

The move is automatic because every destination is inside the skill's dedicated managed directory and the source must be classified as candidate-professional material. It does not need a separate user confirmation.

## Content classification

- **CV:** Place a role-targeted CV in its matching discovered track's `CV/`. Put a truly general CV with no defensible track in `Career/Shared/CV/`; do not force an arbitrary primary track. Use the multi-track procedure when one CV materially supports several discovered tracks.
- **Projects, portfolio, and case studies:** Use the discovered track that best matches the work. Create `Projects/`, `Portfolio/`, or `Case-Studies/` only when those kinds of material exist.
- **Certificates:** Classify a certificate using its documented subject and the candidate evidence. A backend certificate belongs in the discovered backend track; a certificate that genuinely supports multiple tracks belongs in `Shared/Certificates/`.
- **Shared material:** Use `Shared/Education/` for education records and `Shared/Professional-Links/` for link documents or exported profile material. Do not copy contact values from private profile files into `Shared/Contact/`; move only explicit professional contact documents that are safe to organize.

## Multi-track CV procedure

A CV is multi-track only when its substantive content demonstrates two or more discovered career tracks through roles, projects, case studies, portfolio evidence, education, or certificates. A keyword mention or generic skill list alone is insufficient.

1. Move the original CV to `Career/Shared/CV/<filename>` as the single canonical copy.
2. Make the same CV appear in each materially supported `Career/<Track>/CV/` directory:
   - prefer a relative symbolic link to the canonical file when the filesystem and active agent can preserve and use links safely;
   - otherwise create a byte-identical copy in each relevant track as a compatibility fallback.
3. Never create an independent edited version from a placement. Edit or replace the canonical file only with explicit user authorization. When the canonical file changes, refresh every fallback copy and verify content identity.
4. Never overwrite a collision. If a link or copy cannot be created safely, leave that placement missing and report the exact track and conflict.
5. Record in `CANDIDATE_CONTEXT.md`:
   - canonical relative path;
   - every supported track and evidence for the association;
   - every link or fallback-copy path and its placement type;
   - checksum or equivalent identity check for fallback copies;
   - whether the CV is `Dedicated`, `Multi-track`, or `General`.
6. A linked or copied placement improves discovery only. It does not make a multi-track CV dedicated to that career track.

## Dedicated-CV coverage

After organizing CVs, record which discovered tracks have a current dedicated CV and which are covered only by a multi-track or general CV. A dedicated CV must intentionally foreground the track through its title or summary, section order, selected evidence, projects, skills, and terminology; folder placement alone is not enough.

When a target job belongs to a track without a dedicated CV, do not silently generate one or upload the first available file. Ask the user whether to create a tailored ATS-friendly CV for that job or continue with the best existing CV. Read [ats-cv-writing.md](ats-cv-writing.md) for the exact decision prompt, generation rules, storage path, and verification procedure.
