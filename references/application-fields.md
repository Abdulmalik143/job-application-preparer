# Application Fields and Grounded Answers

Classify each application field before populating it.

## Consult the reusable profile first

Before asking for a field, read `APPLICATION_PROFILE.md` and `EXPERIENCE_PROFILE.md` when the user has opted into them. Use a confirmed, current entry only when the same answer is valid across unrelated employers and the field wording matches. Record the source as the appropriate profile and preserve any original-source link recorded there.

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

## Required but unsupported fields

Do not choose an arbitrary option to advance. Leave the field unresolved, explain the missing evidence or decision, and ask the user only if it is necessary to continue. A required blank is not a failure if truthful completion needs human input.

## Upload selection

Choose documents by role relevance and verified contents. Prefer the CV, portfolio, case study, or supporting document aligned to the selected professional profile. If multiple files are equally plausible, leave the upload unresolved and flag the alternatives. Never upload the first-discovered file merely for convenience.

## Review ledger

Before finishing, ensure each populated field can be tied to:

- an original candidate source for factual claims;
- candidate evidence plus the target job for derived answers; or
- an explicit user instruction made for the current application.

Treat stale autofill as unverified until checked. Report unsupported required fields, conflicts, and user decisions without converting them into guesses.
