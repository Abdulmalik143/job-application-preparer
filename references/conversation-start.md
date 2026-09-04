# Conversational Start

Begin a new workspace conversation by discovering and organizing candidate material before asking for a job link or opening Chrome. Respond in the user's language and use a warm, concise conversational tone.

## When professional material is present

After discovery and local-file setup, show a compact, privacy-aware summary. List useful source paths or filenames grouped by purpose—such as CVs, portfolios, projects, certificates, professional profiles, or existing application-memory files. State what each group can support, but do not repeat contact details, addresses, identifiers, or other personal values in the opening.

Then say that the local application memory has been created or updated and ask whether the user has anything new to add. Invite them to upload files, place them in the workspace, or paste relevant professional information. Explain that the skill will verify, categorize, and retain only reusable information in the appropriate private local file.

Use this shape, adapting it to the actual findings and the user's language:

```text
I found and organized:
- CVs: <paths or filenames>
- Portfolio/projects: <paths or filenames>
- Certificates or supporting material: <paths or filenames>

I updated the local application memory from the supported information. Do you have anything new to add—such as an updated CV, project, certificate, link, or work-history correction? Send it here or add it to this workspace, and I will organize it for future applications.

When you are ready, send a job link, a social post, or tell me what you want to prepare.
```

Omit empty categories. Do not claim a file was read or a profile was updated when it was excluded, unreadable, or unsupported.

## When the workspace has no usable professional material

Say plainly that no usable candidate-professional material was found. Explain that the skill can build the local organization from whatever the user provides, without requiring a particular folder structure.

Invite the user to add a CV, portfolio, project or case-study file, certificate, professional profile, or a pasted work-history summary. If they do not have files yet, ask them to share only the basic professional information they want the skill to use; do not pressure them to provide sensitive, legal, demographic, or authentication information.

Use this shape, adapting it to the user's language:

```text
I could not find any usable CV, portfolio, project, certificate, or professional profile in this workspace yet.

Add or upload any material you have, or paste a short professional summary. I will sort it into a candidate map, reusable application information, and verified work history so it is ready for future applications.

You can start with a CV, a portfolio link, a project description, or your work-history details. What would you like to add first?
```

## Conversation rules

- Ask one helpful next question, not a long intake questionnaire.
- Do not ask for a job URL until after the orientation unless the user has already supplied one.
- If the user provided a specific job, post, or outreach task in the opening message, still give a brief discovery summary, then continue directly to that task instead of waiting for a separate confirmation.
- Keep the distinction clear: `CANDIDATE_CONTEXT.md` maps sources, `APPLICATION_PROFILE.md` stores reusable generic answers, `EXPERIENCE_PROFILE.md` stores verified experience, and `APPLICATION_TRACKER.md` records application progress.
