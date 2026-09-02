# Workspace Discovery

Use this guide to discover candidate evidence without imposing a folder structure or collecting unnecessary private data.

## Source authority

Original candidate documents are authoritative. `CANDIDATE_CONTEXT.md` is only a navigation map. A factual answer must be traceable to one or more original sources.

Use practical confidence levels:

- **High:** explicitly stated in a reliable candidate source.
- **Medium:** strongly supported but requires limited interpretation.
- **Low:** ambiguous, incomplete, inferred, or conflicting.

Automatically fill factual fields primarily from high-confidence evidence. Use medium-confidence evidence only when the form context makes the interpretation safe. Do not use low-confidence facts without human review.

## Discovery procedure

1. Check relevant attachments and list likely workspace files recursively. Prioritize names and formats associated with CVs, resumes, profiles, portfolios, case studies, projects, experience, education, certifications, preferences, and reusable application answers.
2. Read `CANDIDATE_CONTEXT.md` first if it exists. Confirm that referenced files still exist and verify important facts in original sources.
3. Inspect the contents of likely files using the appropriate document, PDF, image, or text capability. Do not classify on filename alone.
4. Distinguish shared facts from role-specific material based on evidence, not a predetermined schema.
5. Detect professional profiles from recurring roles, skills, projects, documents, and portfolio evidence. Allow overlap only when it is genuinely relevant to the target job.
6. Record missing information, ambiguous files, and conflicts. Do not select between conflicting sources without user confirmation or a clearly authoritative correction.

If the workspace is reasonably structured, respect it and use it directly. If it is unstructured or spread across several files, continue with semantic discovery rather than asking the user to reorganize it.

## `CANDIDATE_CONTEXT.md`

Create or update this file when a semantic map would materially help because the workspace is unstructured, partially structured, or difficult to navigate. Do not create it merely to restate one obvious CV. Keep paths relative to the workspace and preserve the existing structure.

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
```

When updating an existing map, preserve still-valid user-authored notes and make only evidence-supported changes. Removed, renamed, or changed sources should be noted or corrected. Never turn the map into a new source of truth.

## Conflict and privacy handling

For a conflict, name the fact, each source, each differing value only when necessary for review, and mark it `REQUIRES USER REVIEW`. Do not use the fact until resolved.

Do not inspect unrelated private files, export candidate data outside the task, or duplicate sensitive values across the index. User-provided application preferences are evidence only for the scope in which they were intentionally provided.
