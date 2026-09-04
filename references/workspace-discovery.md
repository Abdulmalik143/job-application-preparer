# Workspace Discovery

Use this guide to discover candidate evidence from every relevant file in the task workspace without imposing a folder structure or collecting unnecessary private data.

## Source authority

Original candidate documents are authoritative. All local Markdown files named in this guide live in the managed `job-application-preparer/` directory; read [managed-workspace.md](managed-workspace.md) first. `CANDIDATE_CONTEXT.md` is only a navigation map. `APPLICATION_PROFILE.md` is an explicit, private user-provided source for recurring application answers, and `EXPERIENCE_PROFILE.md` is an explicit, private user-provided source for verified work history. `APPLICATION_TRACKER.md` records browser workflow state only and is never evidence for a candidate fact. A factual answer must be traceable to one or more original sources or a confirmed profile entry.

Use practical confidence levels:

- **High:** explicitly stated in a reliable candidate source.
- **Medium:** strongly supported but requires limited interpretation.
- **Low:** ambiguous, incomplete, inferred, or conflicting.

Automatically fill factual fields primarily from high-confidence evidence. Use medium-confidence evidence only when the form context makes the interpretation safe. Do not use low-confidence facts without human review.

## First-run workspace initialization

At the start of the first skill conversation in a workspace, resolve or create `job-application-preparer/` at the task-workspace root, then recursively inventory every file and folder outside it. Classify each file as candidate-professional, profile data, irrelevant, unreadable, or excluded. For every readable candidate-professional file, inspect enough of its content to classify it and extract supported evidence; use the appropriate document, PDF, image, or text capability. Do this before asking the user for a job link or opening a browser.

Do not open credentials, secret files, browser profiles, caches, dependency folders, version-control internals, or unrelated binary data. Record excluded and unreadable files in `CANDIDATE_CONTEXT.md` by path and reason without copying their contents.

Create or refresh the local navigation, reuse, and continuity files inside `job-application-preparer/` during this initialization:

- `CANDIDATE_CONTEXT.md` - semantic workspace map; never duplicate personal values.
- `APPLICATION_PROFILE.md` - private reusable generic application data.
- `EXPERIENCE_PROFILE.md` - private reusable work history and projects.
- `APPLICATION_TRACKER.md` - private state for open, paused, and ready-for-review applications; never store field values or authentication data here.

Starting the skill authorizes creation of this managed directory, the local files, and the evidence-discovered career hierarchy unless the user explicitly requests read-only work. Keep the entire managed directory untracked when the workspace uses Git. Prepopulate only high-confidence, non-sensitive values and verified experience records with their source paths; leave sensitive and decision fields blank.

## Discovery procedure

1. Use the first-run inventory when needed; otherwise rescan changed, added, or previously unclassified files outside the managed directory. Prioritize candidate-professional files including CVs, resumes, profiles, portfolios, case studies, projects, experience, education, certifications, preferences, and reusable application answers.
2. Read managed `CANDIDATE_CONTEXT.md` first if it exists. Confirm that referenced files still exist and verify important facts in original sources.
3. Read managed `APPLICATION_PROFILE.md`, `EXPERIENCE_PROFILE.md`, and `APPLICATION_TRACKER.md` if they exist. Confirm profile entries are current enough for the target application and do not use them to silently resolve a conflict with an original document. Use the tracker only to resume or report the browser workflow.
4. Inspect the contents of likely files using the appropriate document, PDF, image, or text capability. Do not classify on filename alone. For files classified as a CV or resume, retain the accessible filesystem last-modified time only as a freshness signal for the opening conversation; it is not career evidence.
5. Distinguish shared facts from role-specific material based on evidence, not a predetermined schema.
6. Detect professional profiles from recurring roles, skills, projects, documents, and portfolio evidence. Allow overlap only when it is genuinely relevant to the target job. For every CV, determine whether it is dedicated to one discovered track, materially supports several tracks, or is general without clear track evidence.
7. Record missing information, ambiguous files, and conflicts. Do not select between conflicting sources without user confirmation or a clearly authoritative correction.

Read [career-organization.md](career-organization.md) during initialization. Discover career tracks from supported candidate sources, then automatically organize high-confidence candidate-professional files within the managed career structure while leaving excluded and unrelated files outside it.

## `CANDIDATE_CONTEXT.md`

Create or update this managed file during first-run workspace initialization, then refresh it when relevant files change. Keep source paths relative to the outer task workspace and preserve the existing structure.

The map should primarily contain source paths, classifications, brief summaries, profile associations, confidence, conflicts, unknowns, and navigation notes. Avoid copying full documents or PII values when a source reference is enough.

Use this adaptable shape; omit empty sections and add role-specific labels as discovered:

```markdown
# Candidate Context

## Workspace Status

Structure: Structured | Partially Structured | Unstructured
Last analyzed: <date when useful>

## Shared Candidate Information

### <category>
Sources:
- ./relative/source

## Discovered Professional Profiles

### <discovered profile>
Resume:
- ./relative/resume
Portfolio or evidence:
- ./relative/evidence
Detected evidence:
- <brief supported item>
Confidence: High | Medium | Low

## CV Coverage

| Canonical CV | Type | Supported tracks | Visible placements | Dedicated coverage | Confidence |
|---|---|---|---|---|---|
| ./relative/resume | Dedicated | <track> | <paths> | <track> | High |
| ./relative/resume | Multi-track | <tracks> | <paths and link/copy type> | None or <verified track> | High |

## Application Preferences

Verified:
- <preference and source>
Unknown:
- <unresolved preference>

## Reusable Application Answers

- <only intentionally provided reusable answer, with source>

## File Map

| File | Detected purpose | Professional profile | Confidence |
|---|---|---|---|
| ./relative/file | <purpose> | <profile> | High | Medium | Low |

## Conflicts

- <fact>: <source A> conflicts with <source B>; requires user review

## Unknown or Unclassified Files

- ./relative/file — <why classification is uncertain>

## Excluded Files

- ./relative/file — <excluded because it is a secret, cache, dependency, version-control internal, or unrelated binary>
```

When updating an existing map, preserve still-valid user-authored notes and make only evidence-supported changes. Removed, renamed, or changed sources should be noted or corrected. Never turn the map into a new source of truth.

## Conflict and privacy handling

For a conflict, name the fact, each source, each differing value only when necessary for review, and mark it `REQUIRES USER REVIEW`. Do not use the fact until resolved.

Do not inspect unrelated private files, export candidate data outside the task, or duplicate sensitive values across the index. User-provided application preferences are evidence only for the scope in which they were intentionally provided.

`APPLICATION_PROFILE.md`, `EXPERIENCE_PROFILE.md`, and `APPLICATION_TRACKER.md` are separate managed files. They may contain user-entered reusable form data, verified work history, and application workflow state, respectively, and must remain private and untracked; never copy their values or browser state into `CANDIDATE_CONTEXT.md`.
