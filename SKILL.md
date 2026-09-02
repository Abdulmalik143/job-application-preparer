---
name: job-application-preparer
description: Prepare one or more job applications from candidate evidence found in the current workspace or user-provided files, including role matching, reusable application and experience profiles, grounded written answers, and mandatory Chrome browser form filling. Use when the user asks to prepare or fill an application, apply for a role, or leave applications ready for review. Never submit an application.
---

# Job Application Preparer

Prepare applications from evidence, leave unsupported decisions unresolved, and stop for human review. The skill knows the workflow; the workspace owns candidate data; the human owns submission.

## Non-negotiable boundaries

- Never submit, send, confirm, finish, or otherwise transmit a job application. Do not activate a control that may be the final submission action. End every prepared application with `READY FOR HUMAN REVIEW — NOT SUBMITTED`.
- Never invent, embellish, or silently resolve candidate facts. Blank is better than wrong.
- Never infer sensitive, demographic, legal, work-authorization, compensation, availability, relocation, or other personal-decision answers.
- Do not modify, rename, move, delete, or create convenience copies of candidate documents unless the user explicitly asks.
- Keep candidate data in the workspace and task context. Never copy it into this skill, its examples, or other public resources.
- On first use, inventory every file in the task workspace. Read every readable candidate or professional file, but never inspect credentials, secrets, caches, dependency folders, or unrelated binary data merely because it exists.
- Treat `APPLICATION_PROFILE.md`, `EXPERIENCE_PROFILE.md`, and `APPLICATION_TRACKER.md` as private, local candidate data. Never commit, upload, or include them in public repositories, prompts, examples, or summaries.
- Never store passwords, password hints, recovery codes, one-time codes, or other authentication secrets in a reusable profile or any task artifact.

## Workflow

1. Initialize the workspace before opening a browser. Recursively inventory the workspace, inspect readable candidate and professional files, and read existing `CANDIDATE_CONTEXT.md`, `APPLICATION_PROFILE.md`, `EXPERIENCE_PROFILE.md`, and `APPLICATION_TRACKER.md` when present.
2. On the first application-preparation run, create or refresh `CANDIDATE_CONTEXT.md` and create missing private `APPLICATION_PROFILE.md`, `EXPERIENCE_PROFILE.md`, and `APPLICATION_TRACKER.md` templates. Treat starting this workflow as permission to create these local files unless the user asks for read-only work. Prepopulate only high-confidence, non-sensitive facts or verified experience records; leave all sensitive and decision fields blank.
3. Open Google Chrome after workspace initialization. Inspect its tabs for the relevant job posting or application, and open the supplied job URL when one is available. Use one designated tab per application, process applications sequentially, and do not substitute another browser for form interaction.
4. Analyze the target job before choosing candidate materials. Capture the company, role, responsibilities, required and preferred qualifications, tools, seniority, location, employment type, and requested documents.
5. Identify the professional profile or combination of profiles that best matches the job. Select the CV, portfolio, projects, experience records, and links based on content and relevance—not discovery order or filenames alone.
6. Build a task-local application context and tracker entry: job identity, selected profile, chosen files, supported facts, reusable profile values, relevant experience records, conflicts, unknowns, user decisions, current page, and last safe stage. Keep each application isolated.
7. Inspect the entire form or current step before filling. Classify every field using [references/application-fields.md](references/application-fields.md) and check the reusable profiles before asking the user.
8. Fill verified facts and evidence-grounded professional answers. Upload only clearly role-appropriate files. Leave unsupported or ambiguous fields unresolved.
9. Advance through verified non-submitting steps such as `Next`, `Continue`, and `Review`; update the tracker after every meaningful step. A label is not enough: confirm the action advances or saves without sending an application.
10. Batch unresolved fields into a concise chat question. First mark the tracker `PAUSED — USER INPUT NEEDED` with the page, stage, exact labels, and next required action. After the user answers, map each answer to its exact form field, save only reusable facts or experience records to the appropriate local profile, and then resume the same Chrome tab.
11. Review for factual consistency, correct profile and uploads, suspicious autofill, conflicts, unanswered required fields, and accidental cross-application content.
12. Stop at the actual final review/submission boundary and report what is ready, unresolved, or blocked. Never activate the final control.

## Workspace routing

Read [references/workspace-discovery.md](references/workspace-discovery.md) whenever candidate files must be located, classified, or indexed. It defines first-run full-workspace inventory, source authority, conflict handling, and `CANDIDATE_CONTEXT.md` behavior.

Use semantic evidence from paths and contents. Folder names are hints, never requirements. Discover all career tracks dynamically; do not assume a profession or fixed directory layout. Ask the user only when required information cannot be found or safely inferred and no useful work can continue without it.

## Reusable profiles

Read [references/application-profile.md](references/application-profile.md) whenever collecting, using, or updating recurring application answers. It defines `APPLICATION_PROFILE.md`, including first-run setup, privacy, question classification, update rules, and the template to copy from `assets/application-profile-template.md`.

Use this profile to avoid repeating generic form questions, not to bypass a user decision. It is an explicit user-provided source for common application data but never overrides conflicting original documents. Reconfirm time-sensitive values and leave company-specific, role-specific, and legal acknowledgements out of the reusable profile.

Read [references/experience-profile.md](references/experience-profile.md) whenever creating, using, or updating the candidate's reusable work history. It defines `EXPERIENCE_PROFILE.md` and the template to copy from `assets/experience-profile-template.md`.

Use the experience profile to fill verified work-history sections. It stores jobs and projects, not one-off answers about a particular employer. A direct question such as “Have you worked for this company before?” can be answered `Yes` only with an exact verified employer match; absence of a match is not evidence for `No` unless the user confirms the profile is complete.

## Application continuity

Read [references/application-tracker.md](references/application-tracker.md) whenever opening, resuming, pausing, or recovering a browser-based application. It defines the private `APPLICATION_TRACKER.md`, its template at `assets/application-tracker-template.md`, the one-tab rule, and recovery behavior.

The tracker records workflow state—not passwords or personal field values. Never close, clean up, or replace an application tab or popup. If browser control disconnects, a page disappears, or an answer is needed, preserve the existing page, record the last known state, and tell the user exactly what is needed to resume. Do not open duplicate applications speculatively.

## Browser routing

Chrome is mandatory after workspace initialization and before any form work. Read [references/browser-and-review.md](references/browser-and-review.md) before interacting with a page. It defines safe multi-step progression, including LinkedIn Easy Apply, and the exact final-submission boundary. If Chrome cannot be opened or controlled, read [references/chrome-access.md](references/chrome-access.md), update the tracker, explain the appropriate setup path for the user's agent, and report `CHROME ACCESS REQUIRED — NOT SUBMITTED`; do not use another browser or claim that browser form preparation is complete.

Never bypass CAPTCHAs, ambiguous consent, login barriers, or unexpected confirmations. Stop the affected application at a safe point and continue other independent applications when possible.

## Unresolved-field chat loop

Read [references/application-fields.md](references/application-fields.md) when a form contains unsupported fields. Ask for unresolved fields in chat as a concise batch, wait for the user's answers, and only then fill the corresponding browser fields. The reference defines what may be saved for future applications and what must remain application-specific.

## Completion criteria

An application is prepared only when the selected profile and documents are evidence-based, every populated field is supportable, generated answers match the specific job, unresolved fields are identified, and the final submission control has not been used.

For several applications, also report counts for ready for review, needing user input, and blocked. `Submitted` must remain `0` because submission is outside this skill.
