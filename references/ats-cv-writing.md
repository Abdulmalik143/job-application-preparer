# ATS-Friendly CV Writing and Verification

Use this guide when creating a new CV/resume, tailoring one to a job, or reviewing whether an existing document is suitable for upload. “ATS-friendly” means using conservative, parser-readable choices; it never means a guaranteed score, ranking, interview, or compatibility with every employer system.

## Preconditions

Before writing:

1. Read the complete job description and the candidate's relevant CVs, `CANDIDATE_CONTEXT.md`, `EXPERIENCE_PROFILE.md`, projects, portfolio material, education, and certificates.
2. Identify the target career track and distinguish required qualifications from preferred ones.
3. Build a private role-to-evidence matrix containing each important requirement, its exact source, confidence, and whether it is safe to use.
4. Mark unsupported requirements as gaps. Never turn a gap into a claim, add an unverified metric, inflate seniority, or infer years of experience.
5. Confirm the employer's accepted or preferred file type, language, page-size expectations, and any special instructions before choosing the output format.

Job-post wording is evidence of employer needs, not evidence that the candidate has a skill. Use an exact keyword only when candidate evidence supports the underlying fact. Write it naturally in a summary, skill category, or achievement; never repeat terms mechanically, hide text, or create keyword-only sections.

## Decide whether a dedicated CV exists

A CV is **dedicated to a career track** only when its headline or summary, section priority, selected experience, projects, skills, and terminology intentionally foreground that track. A general or multi-track CV can support the track without being dedicated to it.

Before uploading a CV for a target track:

1. Inspect the contents of every plausible CV; do not decide from filenames alone.
2. Prefer a current, dedicated CV whose evidence matches the role.
3. If no dedicated CV exists but a general or multi-track CV supports the role, stop before upload and ask in the conversation language:

   `هذه الوظيفة تركز على <المسار>. ملف <اسم الملف> يدعم هذا المسار، لكنه عام ويجمع أكثر من تخصص. هل تريد أن أنشئ CV مخصصًا ومتوافقًا مع ATS لهذه الوظيفة، أم نستخدم الـCV الحالي؟`

4. Treat this as a user decision. Do not choose silently. Record the decision only in the application context and `APPLICATION_TRACKER.md`; it is not a reusable preference for unrelated applications.
5. If the user chooses the existing CV, continue with it after checking freshness, relevance, accepted file type, and parsing quality.
6. If the user chooses a tailored CV, preserve the original unchanged and create a derivative inside `Career/<Target-Track>/CV/Tailored/`. Use a clear filename such as `<Candidate>-<Company>-<Role>-CV.docx` and/or `.pdf`, sanitized for the filesystem. Do not overwrite an existing version.

## Content architecture

Use reverse chronological structure unless the target context clearly requires an academic, federal, or other specialized CV format. Use standard section labels in the document language. A typical order is:

1. Name and target professional title
2. Contact information and verified professional links
3. Targeted professional summary, when useful
4. Relevant experience
5. Projects or case studies, when they add evidence
6. Education
7. Technical or objective skills
8. Certifications, awards, publications, or languages when relevant

Reorder optional sections according to role relevance, but keep headings conventional and unambiguous. Do not label a section creatively if a standard label such as `Experience`, `Projects`, `Education`, `Skills`, or their clear localized equivalent is more machine-readable.

### Header and contact information

- Put the candidate's name, phone, email, location at the appropriate granularity, and relevant URLs in the normal document body—not in a Word header/footer, text box, shape, or image.
- Show contact values as selectable text. Icons may be decorative only; never make an icon the sole representation of a contact method.
- Include only verified links relevant to the role, such as LinkedIn, GitHub, a portfolio, or a personal site.
- Do not add a photo, age, gender, marital status, national identifier, full street address, or other sensitive information unless the user explicitly requests it for a legitimate regional requirement.

### Summary

- Use two to four concise lines when a summary helps connect the candidate to the target role.
- State the supported professional identity, strongest relevant capabilities, and one grounded differentiator or scope indicator.
- Avoid first-person pronouns, clichés, unsupported adjectives, objectives about what the candidate hopes to receive, and long skill lists.

### Experience and projects

- Preserve accurate organization names, titles, locations, and dates. Never repair a gap or ambiguous date by guessing.
- Begin bullets with a precise action verb and express `action + context + outcome` where evidence allows.
- Quantify scale or results only when the number is explicitly supported or the user confirms it.
- Prioritize achievements and responsibilities that map to the target role; remove or compress weakly related material rather than deleting evidence needed to understand the career history.
- Use present tense for current work and past tense for completed work, consistently.
- Avoid dense paragraphs, vague claims, duplicated bullets, unexplained internal jargon, and statements such as “responsible for” when a precise action is known.

### Skills

- Group objective hard skills under plain labels such as `Languages`, `Frameworks`, `Design Tools`, `Methods`, or other evidence-supported categories.
- Mirror a job-description term only when it accurately describes verified candidate evidence; include a spelled-out term with its acronym on first use when the acronym is not universally clear.
- Demonstrate soft skills through experience bullets. Do not fill space with unsupported lists of traits.
- Do not use skill bars, stars, charts, percentages, logos, or icon-only labels.

## Conservative ATS layout

Use these defaults unless the employer or user has a specific documented requirement:

- Single reading column for all core content.
- A4 or US Letter according to locale or application instructions; do not mix page sizes.
- Common readable font, normally 10–12 pt for body text, with a larger name and modestly larger section headings.
- Margins roughly 0.5–1 inch (12.7–25.4 mm), with consistent spacing and enough white space to scan comfortably.
- Black text on a white background. Use bold weight, spacing, and thin horizontal rules for hierarchy.
- Standard round bullets and simple punctuation.
- No tables for layout, multi-column core sections, sidebars, text boxes, floating shapes, photos, charts, background graphics, rating bars, WordArt, or essential information encoded only as an image.
- Align dates with paragraph tab stops or a stable single-column text layout, not a table or floating container.
- Do not shrink type or margins below readable limits to force one page. Early-career resumes should usually be one page; use two pages when relevant verified content genuinely warrants it.

## FlowCV-inspired presentation

When the user asks for a FlowCV-like result, reproduce the restrained visual character rather than copying proprietary templates or weakening parsing:

- A clean A4 page, white background, black typography, and generous white space.
- A prominent candidate name with a concise target title.
- A visible plain-text contact row.
- Uppercase or clearly emphasized standard section headings with thin horizontal rules.
- Bold role or organization labels and consistently aligned dates.
- Conventional bullets and a strong vertical reading rhythm.

The supplied FlowCV example uses this general visual language. Its skills block is visually split into columns; flatten skills into one sequential column or plain grouped lines for the conservative ATS version. Preserve FlowCV-like clarity, not every visual detail.

## File formats and export

- Follow the application instructions first. If the employer requests DOCX, upload DOCX; if it requests PDF, upload PDF; if both are accepted, choose the verified format most appropriate for that form.
- When creating a new tailored CV and both formats are useful, keep an editable `.docx` source and export a text-based `.pdf` with embedded fonts.
- Never deliver an image-only PDF. Do not rasterize the CV into a PDF.
- Use a descriptive filename containing the candidate name and optionally the target role or company. Do not expose sensitive identifiers in filenames.
- Preserve the source CV unchanged. Generated outputs are new, traceable derivatives whose source evidence and target role are recorded in `CANDIDATE_CONTEXT.md`.

## Required verification

Do not call a CV finished merely because it exported successfully.

1. Render every page and visually inspect clipping, overlaps, orphaned headings, broken bullets, crowded regions, inconsistent dates, unexpected blank pages, and unreadably small text.
2. Extract text from the final PDF or DOCX in reading order. Verify that the name, contact text, headings, organizations, titles, dates, bullets, skills, and URLs appear in a logical sequence.
3. Confirm that the file is searchable/selectable text, not a page image, and that essential links display readable labels.
4. Compare every claim and metric against the role-to-evidence matrix and source documents. Remove or flag anything unsupported.
5. Confirm that important truthful job terms appear naturally and that no keyword stuffing, hidden content, or copied employer language creates a misleading claim.
6. Check page size, page count, filename, accepted type, and reasonable file size for the target system.
7. If an ATS-simulation or parsing checker is available, treat it as an additional heuristic only. Report the actual checks performed; never invent an ATS score or promise that a resume will pass.
8. Present the generated files and a concise change summary to the user for review. Never upload a newly generated CV until the user has chosen that option and the document has passed these checks.

## Research basis

This guide synthesizes conservative recommendations from [FlowCV](https://flowcv.com/), [Greenhouse resume parsing support](https://support.greenhouse.io/hc/en-us/articles/200989175-Unsuccessful-resume-parse), [UC Berkeley Career Engagement](https://www.career.berkeley.edu/prepare-for-success/resumes/), [University of Pennsylvania Career Services](https://careerservices.upenn.edu/channels/resume/), [MIT Career Advising & Professional Development](https://capd.mit.edu/resources/make-your-resume-ats-friendly/), and [Harvard's Mignone Center for Career Success](https://careerservices.fas.harvard.edu/resources/hes-create-impactful-resumes-and-cover-letters/). Employer systems differ, so application-specific instructions always take priority.
