---
name: job-application-preparer
description: Prepare one or more job applications from candidate evidence found in the current workspace or user-provided files, including role matching, document selection, grounded written answers, and mandatory Chrome browser form filling. Use when the user asks to prepare or fill an application, apply for a role, or leave applications ready for review. Never submit an application.
---

# Job Application Preparer

Prepare applications from evidence, leave unsupported decisions unresolved, and stop for human review. The skill knows the workflow; the workspace owns candidate data; the human owns submission.

## Non-negotiable boundaries

- Never submit, send, confirm, finish, or otherwise transmit a job application. Do not activate a control that may be the final submission action. End every prepared application with `READY FOR HUMAN REVIEW — NOT SUBMITTED`.
- Never invent, embellish, or silently resolve candidate facts. Blank is better than wrong.
- Never infer sensitive, demographic, legal, work-authorization, compensation, availability, relocation, or other personal-decision answers.
- Do not modify, rename, move, delete, or create convenience copies of candidate documents unless the user explicitly asks.
- Keep candidate data in the workspace and task context. Never copy it into this skill, its examples, or other public resources.
- Inspect only files relevant to the application; do not search unrelated private material.

## Workflow

1. Open Google Chrome at the start of every application request. Inspect its tabs for the relevant job posting or application, and open the supplied job URL when one is available. Do not substitute another browser for form interaction.
2. Analyze the target job before choosing candidate materials. Capture the company, role, responsibilities, required and preferred qualifications, tools, seniority, location, employment type, and requested documents.
3. Discover candidate evidence before asking questions. Search the current workspace, relevant attached files, and files the user intentionally provides. Read `CANDIDATE_CONTEXT.md` early when present, but verify material facts against original sources.
4. Identify the professional profile or combination of profiles that best matches the job. Select the CV, portfolio, projects, experience, and links based on content and relevance—not discovery order or filenames alone.
5. Build a task-local application context: job identity, selected profile, chosen files, supported facts, relevant evidence, reusable answers, conflicts, unknowns, and user decisions. Keep each application isolated.
6. Inspect the entire form or current step before filling. Classify every field using [references/application-fields.md](references/application-fields.md).
7. Fill verified facts and evidence-grounded professional answers. Upload only clearly role-appropriate files. Leave unsupported or ambiguous fields unresolved.
8. Review for factual consistency, correct profile and uploads, suspicious autofill, conflicts, unanswered required fields, and accidental cross-application content.
9. Stop at the final review/submission boundary and report what is ready, unresolved, or blocked.

## Workspace routing

Read [references/workspace-discovery.md](references/workspace-discovery.md) whenever candidate files must be located, classified, or indexed. It defines structured and unstructured workspace behavior, source authority, conflict handling, and the optional `CANDIDATE_CONTEXT.md` map.

Use semantic evidence from paths and contents. Folder names are hints, never requirements. Discover all career tracks dynamically; do not assume a profession or fixed directory layout. Ask the user only when required information cannot be found or safely inferred and no useful work can continue without it.

## Browser routing

Chrome is mandatory for every application request. Open it before any application analysis or form work, then read [references/browser-and-review.md](references/browser-and-review.md) before interacting with a page. If Chrome cannot be opened or controlled, report `CHROME ACCESS REQUIRED — NOT SUBMITTED`; do not use another browser or claim that browser form preparation is complete.

Never bypass CAPTCHAs, ambiguous consent, login barriers, or unexpected confirmations. Stop the affected application at a safe point and continue other independent applications when possible.

## Completion criteria

An application is prepared only when the selected profile and documents are evidence-based, every populated field is supportable, generated answers match the specific job, unresolved fields are identified, and the final submission control has not been used.

For several applications, also report counts for ready for review, needing user input, and blocked. `Submitted` must remain `0` because submission is outside this skill.
