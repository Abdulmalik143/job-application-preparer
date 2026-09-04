# Job Application Preparer

> 📄 An evidence-grounded Agent Skill that prepares job applications without submitting them.

<p align="center">
  <strong>Prepare with evidence. Review with confidence.</strong>
</p>

Job applications are repetitive, but a candidate's story should not be. Job Application Preparer discovers the professional evidence a candidate has intentionally placed in their workspace, matches it to each role, and leaves an application or outreach draft ready for human review.

## ✨ What it does

- 🔎 **Discovers candidate evidence** from resumes, portfolios, projects, and reusable answers in structured or unstructured workspaces.
- 💬 **Starts conversationally** by showing what professional material it found, asking for any new additions, and organizing them into private local application memory.
- 🗂️ **Creates one dedicated workspace folder** named `job-application-preparer`, then discovers career tracks from the candidate's evidence and sorts verified professional files without assuming a profession.
- 🧱 **Bootstraps the workspace** by creating a candidate map plus private application, work-history, and application-tracking files on first use.
- 🗂️ **Remembers common form answers locally** in a private application profile, so users do not repeat the same generic information for every application.
- 💼 **Builds a reusable work-history profile** from verified experience, making employment sections faster to complete.
- 🎯 **Matches the right profile** to the role, selecting the most relevant CV, portfolio, and project evidence.
- 🧭 **Handles multi-track CVs** by keeping one canonical resume and making it available from every career track it genuinely supports.
- 📄 **Creates tailored ATS-friendly CVs on request** with evidence-grounded content, conservative FlowCV-inspired styling, and visual plus text-order verification.
- 🙋 **Keeps the CV choice human-controlled** when a role has no dedicated resume: create a tailored version or continue with the existing multi-track CV.
- ✍️ **Writes grounded answers** that are concise, role-specific, and supported by candidate sources.
- ✉️ **Prepares tailored outreach** from social-media job posts, turning an advertised email address or phone number into a short, evidence-led draft that is ready to paste—not automatically sent.
- 🧭 **Handles uncertainty honestly** by flagging conflicts, unknowns, sensitive questions, and personal decisions instead of guessing.
- 🌐 **Works safely in Chrome** using the user's current signed-in session: one tab per application, never closing an application page, and always stopping before final submission.
- 📍 **Keeps a local resume point** for each application, including its last safe stage and the exact input or action needed to continue.
- 💬 **Asks only what is missing** in chat, then returns to the form with the user's answers.

## ⚡ Install

```bash
npx skills add Abdulmalik143/job-application-preparer
```

> To target a specific agent, add `--agent <agent-name>`.

## 🧭 Use

Ask your compatible agent:

```text
Use $job-application-preparer to prepare this job application for my review without submitting it.

Use $job-application-preparer to draft a short email for this social-media job post without sending it.
```

## 🛡️ Safety by design

- 📂 Candidate information is discovered from the workspace or files the user explicitly provides; it is never hardcoded into the skill.
- 🔗 Every factual answer must be traceable to candidate evidence.
- ✅ ATS guidance favors standard headings, one-column readability, truthful role keywords, and verified exports; it never promises an ATS score or guaranteed pass.
- 🧩 Unsupported, conflicting, sensitive, and user-decision fields remain unresolved for human review.
- 🔒 Passwords, verification codes, employer-specific answers, and legal acknowledgements are never saved as reusable profile data.
- 🚫 The skill never submits, sends, confirms, calls, or otherwise finalizes a job application or outreach message.

## 👋 Built by Abdulmalik Alhindi

Abdulmalik Alhindi is a Front-End Developer and Product Designer who turns ideas into cohesive digital experiences - from visual identity and interface design to polished front-end implementation. He blends creative thinking with user-centered design and code to give each product a distinct, intentional character.

### 🌐 Connect

- 🐙 [GitHub](https://github.com/Abdulmalik143)
- 💼 [LinkedIn](https://www.linkedin.com/in/abdulmalik-alhindi/)
- 🎨 [Behance](https://www.behance.net/Abdulmalik-Alhindi)
- ✉️ [Email](mailto:abdulmalik.alhindi@outlook.sa)

## 📄 License

Released under the [MIT License](LICENSE).
