# Chrome Access and Setup

Chrome is required for browser form work in this skill. Use the user's existing standard Chrome profile and signed-in session; do not use Incognito, a temporary profile, or another browser.

## When Chrome control is available

Open or attach to the current Chrome session, inspect its tabs, and use the tab containing the application. If the user supplies a URL, open it in that same profile.

## When Chrome cannot be opened or controlled

Do not continue browser form work. Preserve any existing Chrome pages, update `APPLICATION_TRACKER.md` with the last known URL, stage, and recovery step, then report `CHROME ACCESS REQUIRED — NOT SUBMITTED`. Name the capability that is missing and give the user the setup path appropriate to their agent. Do not invent menu labels or setup steps that are not visible in the current environment.

- **Codex:** Ask the user to make its Chrome-control or browser-control capability available in the active Codex environment, then open Chrome with the desired signed-in profile and retry.
- **Claude or Cursor:** Ask the user to enable or connect a Chrome-capable browser automation integration supported by that agent, such as its native browser feature or a configured browser-control MCP. Then open Chrome with the desired signed-in profile and retry.
- **Other agents:** Ask the user to enable a browser-control capability that can attach to Chrome, list tabs, open URLs, inspect pages, and type into forms. Then retry.

Offer the following minimal steps when the exact UI is unknown:

1. Open Google Chrome normally and sign in to the required job-site account.
2. Open the target job or application tab.
3. Enable or connect the agent's Chrome-control or browser-control integration.
4. Ask the agent to retry the application preparation.

Until Chrome control is available, the agent may organize workspace data and draft answers only if the user explicitly asks for that limited work. It must not claim that the form was completed.
