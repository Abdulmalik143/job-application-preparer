# Job Application Preparer

> 📄 An evidence-grounded Agent Skill that prepares job applications without submitting them.

<p align="center">
  <strong>Prepare with evidence. Review with confidence.</strong>
</p>

Job applications are repetitive, but a candidate's story should not be. Job Application Preparer discovers the professional evidence a candidate has intentionally placed in their workspace, matches it to each role, and leaves the application ready for human review.

## ✨ What it does

- 🔎 **Discovers candidate evidence** from resumes, portfolios, projects, and reusable answers in structured or unstructured workspaces.
- 🎯 **Matches the right profile** to the role, selecting the most relevant CV, portfolio, and project evidence.
- ✍️ **Writes grounded answers** that are concise, role-specific, and supported by candidate sources.
- 🧭 **Handles uncertainty honestly** by flagging conflicts, unknowns, sensitive questions, and personal decisions instead of guessing.
- 🌐 **Works with browser forms** when capabilities are available, while always stopping before final submission.

## ⚡ Install

```bash
npx skills add Abdulmalik143/job-application-preparer
```

> To target a specific agent, add `--agent <agent-name>`.

## 🧭 Use

Ask your compatible agent:

```text
Use $job-application-preparer to prepare this job application for my review without submitting it.
```

## 🛡️ Safety by design

- 📂 Candidate information is discovered from the workspace or files the user explicitly provides; it is never hardcoded into the skill.
- 🔗 Every factual answer must be traceable to candidate evidence.
- 🧩 Unsupported, conflicting, sensitive, and user-decision fields remain unresolved for human review.
- 🚫 The skill never submits, sends, confirms, or otherwise finalizes a job application.

## 👋 Built by Abdulmalik Alhindi

Abdulmalik Alhindi is a Front-End Developer and Product Designer who turns ideas into cohesive digital experiences - from visual identity and interface design to polished front-end implementation. He blends creative thinking with user-centered design and code to give each product a distinct, intentional character.

### 🌐 Connect

- 🐙 [GitHub](https://github.com/Abdulmalik143)
- 💼 [LinkedIn](https://www.linkedin.com/in/abdulmalik-alhindi/)
- 🎨 [Behance](https://www.behance.net/Abdulmalik-Alhindi)
- ✉️ [Email](mailto:abdulmalik.alhindi@outlook.sa)

## 📄 License

Released under the [MIT License](LICENSE).
