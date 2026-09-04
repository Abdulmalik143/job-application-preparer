# Application Fields and Grounded Answers

Classify each application field before populating it.

## Consult the reusable profile first

Before asking for a field, read `APPLICATION_PROFILE.md` and `EXPERIENCE_PROFILE.md` when they are available. Use a confirmed, current entry only when the same answer is valid across unrelated employers and the field wording matches. Record the source as the appropriate profile and preserve any original-source link recorded there.

Do not treat either profile as permission to fill company-specific, role-specific, time-sensitive, sensitive, or legal questions. For profile setup and updates, read [application-profile.md](application-profile.md) or [experience-profile.md](experience-profile.md).

## A — Verified fact

Examples include name, contact details, education, known job titles and dates, employment history, portfolio links, and explicitly evidenced skills.

Fill when a reliable candidate source, a confirmed application-profile entry, or a confirmed experience-profile record supports the exact value and no unresolved conflict applies. Retain the source association in task context.

## Work-history sections

Use `EXPERIENCE_PROFILE.md` to fill employment-history sections. If the form requests complete work history, enter every verified record in chronological order. If it asks for relevant experience, select only records that support the target role.

For “Have you worked for <company> before?” or a similar question, an exact verified employer match supports `Yes`. A missing match does not support `No` unless the user confirms their profile contains their complete employment history. Do not treat similarly named subsidiaries or companies as an exact match without user review.

## B — Derived professional answer

Examples include interest in the role, relevant experience, a relevant project, fit for the position, or experience with a requested tool.

Generate only from the target job plus candidate evidence. Select the strongest relevant examples; do not maximize keyword quantity. Write naturally in the candidate's voice, answer the exact question, and stay concise unless the form requests detail. Do not add metrics, scope, leadership, technologies, outcomes, or years that sources do not support.

Company-specific answers must be generated independently for each employer. Do not reuse a “why this company” or similar answer across applications.

## C — User decision required

Examples include expected or current compensation, availability, notice period, relocation, preferred work arrangement, negotiation choices, and personal commitments.

Leave unanswered unless the user makes an explicit decision for the current application. Do not auto-fill a past answer from the reusable profile, and do not derive a choice from location, work history, or job interest.

## D — Sensitive, legal, or demographic

Examples include race, ethnicity, religion, gender, disability, medical or veteran status, criminal history, government identifiers, work authorization, legal declarations, and consent attestations.

Never infer. Use only information explicitly and intentionally provided for the exact purpose. Otherwise leave unanswered and flag for human review. A user may explicitly choose to keep a value locally in the profile for a repeated, identical question, but it remains sensitive and must be reviewed before use. Never make a declaration or consent choice on the user's behalf when its meaning or authorization is unclear.

## Never save as a reusable answer

Do not add any of the following to `APPLICATION_PROFILE.md`:

- passwords, password confirmation values, MFA codes, recovery codes, or credentials;
- one-off employer relationship, referral, relative, conflict, or supplier answers; store verified work history in `EXPERIENCE_PROFILE.md` instead;
- “How did you hear about us?”, “Why this company?”, and other company-specific prompts;
- expected compensation, start date, availability, negotiation choices, and other application-time decisions;
- applicant acknowledgements, terms acceptance, privacy consent, or declarations whose text may vary by employer.

## Chat answer loop

After inspecting the whole form or current step, group unresolved fields into one concise chat message. Before asking, update `APPLICATION_TRACKER.md` with `PAUSED — USER INPUT NEEDED`, the current page and stage, each exact label, whether it is required, the field type or available options, why it could not be answered from sources, whether its answer may be saved for future applications, and the next safe action. Keep the designated Chrome tab or popup open.

Wait for the user's reply before filling those fields. Map each answer only to the corresponding field; if the reply is ambiguous, ask a focused follow-up rather than guessing. Then:

- write a reusable cross-employer fact to `APPLICATION_PROFILE.md` and report that it was saved;
- write a confirmed job, project, responsibility, achievement, or date to `EXPERIENCE_PROFILE.md` and report that it was saved;
- use a company-specific, time-sensitive, sensitive, legal, or acknowledgement answer only for the current application and do not save it;
- return to the same Chrome tab or popup and fill only the fields supported by the user's reply;
- update the tracker with the resumed stage and any remaining unanswered fields.

Do not use chat answers to accept terms, attestations, or final submission actions. These remain under human control.

## Required but unsupported fields

Do not choose an arbitrary option to advance. Leave the field unresolved, explain the missing evidence or decision, and ask the user only if it is necessary to continue. A required blank is not a failure if truthful completion needs human input.

## Upload selection

Choose documents by role relevance and verified contents. Prefer the CV, portfolio, case study, or supporting document aligned to the selected professional profile. Inspect contents rather than trusting folder placement or filenames.

Before selecting a CV, check the target track's dedicated-CV coverage in `CANDIDATE_CONTEXT.md`. A multi-track CV placement inside a track folder does not make it dedicated. If the target track has no dedicated CV but an existing general or multi-track CV supports it, follow [ats-cv-writing.md](ats-cv-writing.md): ask whether the user wants a tailored ATS-friendly CV for this job or wants to use the current CV. Do not make that choice silently and do not upload a newly generated CV before it has been verified and shown to the user.

If multiple dedicated files are equally plausible, leave the upload unresolved and flag the alternatives. Never upload the first-discovered file merely for convenience.

## Review ledger

Before finishing, ensure each populated field can be tied to:

- an original candidate source for factual claims;
- candidate evidence plus the target job for derived answers; or
- an explicit user instruction made for the current application.

Treat stale autofill as unverified until checked. Report unsupported required fields, conflicts, and user decisions without converting them into guesses.
