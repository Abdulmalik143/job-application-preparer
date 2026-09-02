# Browser Interaction and Human Review

Use Google Chrome to inspect and fill application pages while preserving human control of submission.

## Mandatory Chrome start

Open Google Chrome after workspace initialization and before analyzing a form or preparing a browser-based application. Inspect open tabs for the relevant company, role, and application page. When the user supplies a job URL, open it in Chrome; otherwise, use the relevant existing Chrome tab when one is available.

Do not substitute another browser for application interaction. If Chrome cannot be opened or controlled, stop browser form work and report `CHROME ACCESS REQUIRED — NOT SUBMITTED`. Do not claim the application was prepared in a form. Offline document selection or answer drafting may continue only when the user asks for that limited work.

## Interaction boundary

Inspect visible page state and understand the current form or step before editing. Navigation through a multi-step application is allowed only when the action clearly saves or advances without submitting. If a button such as **Apply Now**, **Continue**, **Confirm**, **Finish**, or **Complete** could transmit the application, do not click it until its non-submitting effect is unambiguous; never click it when it is the final action.

Never submit an application, even if the user earlier asked to “apply.” Stop on the final review page or immediately before the final submission control. The user must perform submission manually.

Do not bypass CAPTCHAs, login or identity-verification barriers, ambiguous consent, unexpected confirmation dialogs, broken forms, external redirects, or upload uncertainty. Stop safely and report the location and unresolved issue.

## Per-application isolation

Treat every job and browser tab as an independent application. Before filling a tab, identify its company, role, URL, job context, selected profile, and selected documents. Never carry company-specific text, form choices, or uploads from one application into another.

Track in task context:

- company, role, and URL;
- selected professional profile;
- chosen CV and portfolio or supporting file;
- fields filled and source status;
- generated answers;
- unanswered and user-decision fields;
- warnings, conflicts, blockers, and review status.

After filling, reread the page for suspicious browser autofill, hidden required fields, incorrect dropdown choices, truncated answers, wrong uploads, and accidental submission controls.

## Single-application summary

Provide a concise review handoff:

```text
Company: <company>
Role: <role>
Professional profile: <selected profile>
CV: <relative path or unresolved>
Portfolio/supporting file: <relative path, not required, or unresolved>
Filled: <count when known>
Generated professional answers: <count when known>
Needs manual review: <count and field names>
Unanswered: <field names>
Warnings: <warnings or None>
Status: READY FOR HUMAN REVIEW — NOT SUBMITTED
```

If blocked before review, use `BLOCKED — NOT SUBMITTED` and explain the blocking point. Never label an application ready if unsupported required fields or ambiguous uploads still prevent a meaningful review.

## Multi-application summary

Also report totals for applications prepared, ready for review, needing user input, and blocked. Report `Submitted: 0`. Continue other independent applications after one is blocked when doing so is safe.
