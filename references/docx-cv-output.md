# DOCX CV Output and Hyperlinks

Read this guide whenever creating a new tailored CV or making a substantive CV revision. It governs the editable Word master, professional links, PDF derivation, and final quality checks.

## Output decision

1. Create a polished `.docx` master by default. Store it in `Career/<Target-Track>/CV/Tailored/` without changing the source CV.
2. Create a text-based PDF from that final DOCX when the application requests PDF, accepts PDF as the selected upload type, or the user asks for it. Never make a separate PDF-only design that can drift from the Word master.
3. If the application explicitly requires another accepted format, follow that instruction while retaining the DOCX master when feasible.
4. Use a DOCX-capable authoring workflow that can create actual external hyperlink relationships and render the document for visual review. When the `documents` capability is available, use it. If the active agent cannot create and verify a real DOCX, say so before claiming a DOCX is ready.
5. Use the page size required by the application. If it does not specify one, preserve the page size of the candidate's current approved reference CV when available; otherwise choose A4 for markets where A4 is standard and US Letter only when it is the relevant local expectation. Do not accept a generic document-tool default without checking.

## Contact and professional links

Use only values supported by candidate evidence or intentionally confirmed by the user. Put the contact row in the normal document body, near the name and title; do not hide it in a header, footer, table, text box, image, or icon-only element.

Every link must have two separate parts:

- **Display label:** short, professional, readable text.
- **Hyperlink target:** the exact verified URL, `mailto:` email address, or `tel:` phone number.

Create a real external hyperlink relationship in the DOCX. Plain text that resembles a URL is insufficient.

Use the candidate's verified preferred labels when available. Otherwise apply these defaults:

| Link kind | Display label | Hyperlink target |
|---|---|---|
| GitHub profile | the verified GitHub handle, e.g. `Abdulmalik143` | verified GitHub profile URL |
| LinkedIn profile | `LinkedIn` or the candidate's professional name | verified LinkedIn profile URL |
| Portfolio or Behance | `Portfolio`, `Behance`, or verified portfolio name | verified portfolio URL |
| Email | the verified email address | `mailto:<verified email>` |
| Phone | the verified international-format number | `tel:<verified number>` when supported |
| Personal website | a concise verified site or brand name | verified website URL |

Do not use raw `https://...` text as the visible label unless the user explicitly requests it. Do not shorten, normalize, redirect, or guess a destination URL. Do not include a link merely because the platform is common; it must be verified in the candidate's files or confirmed by the user.

For ATS readability, use visible text labels separated by simple punctuation such as ` | `. Icons can be omitted; if the user requests them, they must remain decorative and the adjacent text must still be selectable and linked.

## DOCX construction and review

- Use the conservative ATS layout in [ats-cv-writing.md](ats-cv-writing.md): core content in one reading column, plain headings, selectable text, no layout tables, sidebars, or text boxes.
- Use the user-supplied FlowCV example only as visual direction: clean A4 page, black text, clear hierarchy, whitespace, and restrained rules. Do not copy its template, and do not sacrifice ATS parsing for visual imitation.
- Build each experience entry as a scan-friendly unit: a bold job title, company and location, a consistently aligned date range, then separate bullet paragraphs. Never place multiple responsibilities in one unbulleted line or paragraph.
- Use bold strategically: name, section headings, role titles, company names when helpful, skill-category labels, and at most one short verified emphasis phrase inside a bullet. Do not bold full sentences, every keyword, or several phrases per bullet; the contrast must remain meaningful.
- Treat a one-page CV as a balanced composition. If it ends with a conspicuously empty lower third while verified evidence remains, first add or restore relevant bullets, projects, certifications, or skill categories; do not stretch line spacing, widen margins, or add generic text to fill it.
- When evidence warrants more content than a readable one-page design can hold, use a second page rather than reducing body text below the ATS-safe minimum or removing meaningful professional range.
- Build every URL as a native DOCX external hyperlink relationship; do not rely on application auto-detection of typed URLs.
- Render every DOCX page and inspect it at normal reading size. Re-render after any formatting or OOXML hyperlink change.
- Test each display label and confirm it maps to the correct verified destination. Confirm that email and phone text remains visible even if the viewer does not support `mailto:` or `tel:` links.
- When creating a PDF, export from the reviewed DOCX, verify selectable text and reading order, and confirm that required hyperlinks remain clickable in the exported PDF.
- Remove document metadata that could expose unrelated personal information when the available authoring workflow can do so safely. Do not remove the candidate's intentional name or contact information from the document body.

Read [cv-composition-and-emphasis.md](cv-composition-and-emphasis.md) before content selection and final review.

## Completion report

Report the target role, output paths, selected upload format, and any verified links included by label. Do not echo sensitive values unnecessarily. State that the files are ready for user review and are not uploaded or submitted.
