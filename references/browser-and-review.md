# Browser Interaction and Human Review

Use Google Chrome to inspect and fill application pages while preserving the user's existing signed-in session, browser state, and control of submission.

## Mandatory Chrome start

Open Google Chrome after workspace initialization and before analyzing a form or preparing a browser-based application. Inspect open tabs for the relevant company, role, and application page. When the user supplies a job URL, open it in the same normal Chrome profile; otherwise use the relevant existing Chrome tab when one is available.

Do not substitute another browser for application interaction. If Chrome cannot be opened or controlled, stop browser form work, update `APPLICATION_TRACKER.md`, and report `CHROME ACCESS REQUIRED — NOT SUBMITTED`. Do not claim the application was prepared in a form. Offline document selection or answer drafting may continue only when the user asks for that limited work.

## Preserve tabs and application state

Use exactly one designated Chrome tab or application popup for each active application. Process a list of jobs sequentially; do not open a tab for every job up front.

- Never close, clean up, dismiss, or deliberately replace a tab or popup that was opened or found for an application, including a duplicate or a page that appears blocked.
- If duplicates already exist, choose one as the designated tab, record the duplicate in `APPLICATION_TRACKER.md`, and leave both open. Do not retry by opening another copy unless the user asks or the original URL is demonstrably unavailable.
- Keep the designated tab open while waiting for user input or after browser-control interruption. Before switching away, record its URL, current stage, and next intended safe action in the tracker.
- If control disconnects, first try to reattach to the existing Chrome session and locate the tracked tab. Do not assume a missing page was submitted, rejected, or safely disposable. If it cannot be located, record that fact, the last known stage, and the recovery action needed.

Read [application-tracker.md](application-tracker.md) for the tracker structure and pause/recovery requirements.

## Safe multi-step progression

Inspect the visible page state before editing or activating any control. Once the effect is clear, filling verified fields, uploading an approved document, and advancing through a non-submitting step do not need a separate confirmation.

`Next`, `Continue`, `Save and continue`, and `Review` may be activated only when visible context shows that they save or advance the current form without transmitting an application. Update the tracker after the transition. Do not treat the first button in a modal, or a button whose label includes `Next`, as an application submission merely because it completes the first visible step.

Buttons such as **Apply Now**, **Continue**, **Confirm**, **Finish**, or **Complete** require closer inspection. Activate one only when its non-submitting effect is unambiguous, such as opening an application form or moving to a named next step. Never activate it when it is the final action or when its effect is unclear.

### LinkedIn Easy Apply

Treat each Easy Apply modal stage independently. The contact-information stage (for example email and phone number) is an ordinary early step, not the end of the application.

1. Inspect the stage label, visible required fields, and button text.
2. Fill only supported fields. For an unresolved required field, mark the tracker paused and ask the user in chat; leave the modal open.
3. When the control is `Next` and the modal indicates another step, activate it and verify that the stage changed. Continue this pattern for later `Next` stages.
4. When the control is `Review`, activate it only when it moves to the review stage rather than submitting. Verify that the review page/modal is visible.
5. Stop only when the real final action is visible, commonly `Submit application` or a `Submit` control in the final review stage. Do not click it. Mark the tracker and handoff as `READY FOR HUMAN REVIEW — NOT SUBMITTED`.

If a button's effect cannot be established from the visible state, do not guess. Preserve the modal, record the ambiguity, and ask the user to review or authorize the next safe interpretation.

## Interaction boundary

Never submit an application, even if the user earlier asked to “apply.” Stop on the final review page or immediately before the final submission control. The user must perform submission manually.

Do not bypass CAPTCHAs, login or identity-verification barriers, ambiguous consent, unexpected confirmation dialogs, broken forms, external redirects, or upload uncertainty. Keep the affected page open, record the location and issue in the tracker, and report the precise blocker.

## Per-application isolation

Before filling a designated tab, identify its company, role, URL, job context, selected profile, and selected documents. Never carry company-specific text, form choices, or uploads from one application into another.

Track in `APPLICATION_TRACKER.md`:

- company, role, URL, and designated tab or popup label when known;
- current state and last safe stage;
- selected professional profile and documents;
- fields filled as labels or counts, without copying sensitive values;
- unanswered fields, user-decision fields, warnings, and blockers;
- the exact next action or answer required to resume.

After filling or advancing, reread the page for suspicious browser autofill, hidden required fields, incorrect dropdown choices, truncated answers, wrong uploads, and accidental submission controls.

## Review handoff

Provide a concise review handoff:

```text
Company: <company>
Role: <role>
Chrome state: <current page or final review stage>
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

If user input or access is needed before review, use `PAUSED — USER INPUT NEEDED` or `BLOCKED — NOT SUBMITTED`, include the tracker path, last safe stage, and the exact fields or action needed. Never label an application ready if unsupported required fields or ambiguous uploads still prevent meaningful review.

For multiple applications, report totals for ready for review, needing user input, and blocked. Report `Submitted: 0`.
