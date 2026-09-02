# Application Tracker and Recovery

Use `APPLICATION_TRACKER.md` as a private, local continuity log for browser-based applications. It prevents a paused or interrupted application from becoming an unexplained lost tab.

## Purpose and limits

The tracker records the state of each application, not candidate evidence or form answers. It must not contain passwords, authentication codes, government identifiers, exact sensitive values, or a copy of the completed form.

Create it from `assets/application-tracker-template.md` on the first application-preparation run unless the user requests read-only work. Keep it untracked in Git by adding its exact filename to the local `.git/info/exclude`; do not modify a shared `.gitignore` automatically.

## One record per application

Create or update a record before entering data into a designated Chrome tab or popup. Include only what is needed to resume safely:

- company, role, URL, and tab or popup label when known;
- status: `IN PROGRESS`, `PAUSED — USER INPUT NEEDED`, `BLOCKED — NOT SUBMITTED`, or `READY FOR HUMAN REVIEW — NOT SUBMITTED`;
- current page and last confirmed safe stage;
- selected documents and profile, using paths or labels rather than copied contents;
- filled field labels or a count, without values;
- exact unresolved labels, blockers, and the next safe action;
- date or time of the latest update.

Do not mark an application submitted. The only terminal state this skill may write is `READY FOR HUMAN REVIEW — NOT SUBMITTED`.

## Update moments

Update the record when any of these occur:

1. A tab or popup is designated for the application.
2. A form advances to a new named step, including LinkedIn `Next` or `Review`.
3. The agent asks the user for an answer or manual action.
4. Browser control fails, reconnects, or cannot find the tracked page.
5. The final review stage is visible.

The tracker should let the user resume without rediscovering the application: it must state where it stopped and exactly what is needed next.

## Recovery rules

When a tab is unreachable or control disconnects:

1. Do not close any browser page and do not create a duplicate application page.
2. Record the interruption and last known stage in the tracker.
3. Reattach to the existing normal Chrome session and locate the designated tab by URL, company, role, or visible stage.
4. If the page cannot be found, report that it is unavailable rather than inventing its status. Ask the user to reopen the tracked URL in Chrome if necessary.

When an answer is missing, keep the page open and record the exact question before sending the chat request. On the user's reply, return to the designated tab, update the record, and continue only the safe next step.
