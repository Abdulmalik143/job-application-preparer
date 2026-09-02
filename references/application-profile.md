# Reusable Application Profile

Use this guide to maintain `APPLICATION_PROFILE.md`: a private, local record of generic application answers the user wants to reuse. It reduces repeated form entry without turning company-specific or personal decisions into defaults.

## Purpose and authority

`APPLICATION_PROFILE.md` is not a CV, portfolio, work-history file, or replacement for `CANDIDATE_CONTEXT.md`.

- It holds user-confirmed answers to recurring application fields.
- It is a private operational source, not a public skill resource.
- Employment history, responsibilities, achievements, and project records belong in `EXPERIENCE_PROFILE.md`.
- Original candidate documents remain authoritative for career history, education, skills, projects, and role-specific evidence.
- When an original source conflicts with the profile, do not decide silently; flag the conflict for the user.

## First run and storage

When no profile exists, first inspect candidate sources. At the beginning of an application-preparation workflow, create `APPLICATION_PROFILE.md` from `assets/application-profile-template.md` unless the user requests read-only work. Do not force a long setup wizard: prepopulate only high-confidence, non-sensitive facts with their sources, then collect only the generic answers required by the current form.

If the workspace is a Git repository, keep the profile untracked. Prefer adding the exact filename to the local `.git/info/exclude`; do not silently modify a shared `.gitignore`.

Tell the user when a new reusable answer is saved. If they ask not to maintain a profile, use their answer only for the current application and do not update the file.

## What belongs in the profile

Save an answer only when all of the following are true:

1. It remains true or appropriate across unrelated employers.
2. The user explicitly supplied or confirmed it for reuse.
3. It does not require a decision for this particular role, company, country, or date.
4. It is not a credential, acknowledgement, or prohibited sensitive value.

Common reusable entries include contact details, exact English name spelling, general address and residence details, education, stable professional links, and a preferred generic CV location. Record a source or confirmation date for each entry so stale information can be reviewed. Store employment history in `EXPERIENCE_PROFILE.md`, not here.

## Questions that must not become defaults

Never save company-specific questions or answers, including referral details, relatives or friends connected to that company or its suppliers, “How did you hear about us?”, and “Why do you want to work here?”. Store verified prior jobs in `EXPERIENCE_PROFILE.md`; do not store a one-off yes/no answer to “Have you worked here before?”.

Never save or auto-fill expected salary, current salary, start date, availability, notice period, relocation, work arrangement, or negotiation choices. These are application-time decisions, even when a prior answer exists.

Never save passwords, password confirmations, MFA or recovery codes, government-portal credentials, or any authentication secret. Ask the user to handle those directly in their password manager or browser.

Do not accept terms, privacy notices, applicant acknowledgements, or legal attestations on the user's behalf. Their wording and implications can vary by employer.

## Sensitive and legal data

Do not solicit sensitive values during ordinary profile setup. This includes government ID numbers, date of birth, gender, marital status, work authorization, criminal history, disability or accommodations, and similar legal or demographic information.

If the user explicitly asks to save an exact sensitive value locally for a repeated, identical field, place it only in the template's sensitive section, label it with the user's approval date, and keep it untracked. Before using it, confirm that the field has the same meaning and flag it for user review. Never repeat the value in a summary, context map, or public file.

## Learning from a new form field

When a new question appears:

1. Read the wording and classify it as verified fact, derived answer, user decision, sensitive/legal, company-specific, or credential.
2. Check the profile and candidate sources before asking the user.
3. If the answer is genuinely reusable, ask once in chat, state that it will be saved for future applications, and add it with a confirmation date and source.
4. If it is company-specific, time-sensitive, legal, sensitive without explicit storage permission, or a credential, use it only for the current application or leave it for review. Do not add it to the profile.

## Keeping it current

Review profile entries when the user updates contact details, location, eligibility, CVs, or preferences. For each changed value, retain the current answer and update its confirmation date. Do not treat an old profile entry as more authoritative than a newer candidate document or explicit user correction.
