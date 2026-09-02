# Reusable Experience Profile

Use this guide to maintain `EXPERIENCE_PROFILE.md`: a private, local record of the candidate's verified employment history, projects, responsibilities, achievements, tools, and dates. It makes work-history sections reusable across applications without copying an entire CV into every form.

## Purpose and authority

`EXPERIENCE_PROFILE.md` is separate from `APPLICATION_PROFILE.md` and `CANDIDATE_CONTEXT.md`.

- It is the structured source for reusable work-history entries.
- It should reflect original CVs, portfolios, project files, or explicit user confirmation.
- It does not replace original sources. Preserve a source path or confirmation date on each record.
- It remains private and untracked. Never copy it into a public repository, context map, or public summary.

## First run and maintenance

When the user opts in, inspect their existing candidate sources before asking questions. Create the profile from `assets/experience-profile-template.md`, populate only supported records, and ask the user to verify ambiguous dates, employer names, job titles, or gaps.

Add a new record when the user supplies a job, project, responsibility, achievement, or date that is useful across applications. Update a record when the user corrects it, retaining its original source and confirmation date. Never invent a responsibility, metric, employer, title, or date to complete a form.

## Record design

Each employment record should include the employer, title, location when known, employment type when known, start and end dates, current status, concise supported responsibilities, achievements, tools, source, and last confirmation date. Keep project records separate when they were not employment.

Do not store salary, manager contact details, confidential employer data, credentials, or one-off company-relationship answers in this profile.

## Filling a work-history section

Read the form label and instructions first.

- For a complete employment-history section, use every verified employment record in chronological order.
- For a relevant-experience prompt, choose only records that materially support the target role and write a grounded summary.
- For a project section, use verified project records; do not label a project as paid employment unless the source supports that.
- For a question about a named employer, answer `Yes` only when an exact verified employer match exists. Do not answer `No` from absence unless the user confirms the profile is complete.
- Flag missing fields or conflicts for review rather than filling a plausible guess.

## Privacy and update rules

Keep this file local. If the workspace uses Git, add the exact filename to `.git/info/exclude` only after user approval; do not change a shared `.gitignore` automatically.

When adding a new item, tell the user what was saved. Do not add company-specific motivations, referrals, relatives, legal acknowledgements, or application decisions; those are not work-history records.
