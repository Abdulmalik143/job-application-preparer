# Conversational Start

Begin a new workspace conversation by discovering and organizing candidate material before asking for a job link or opening Chrome. Start in Arabic and use a warm, concise conversational tone. End the opening with a short English option to continue in English. If the user ignores that option, continue in Arabic.

## When professional material is present

After discovery and local-file setup, show a compact, privacy-aware summary. List useful source paths or filenames grouped by purpose—such as CVs, portfolios, projects, certificates, professional profiles, or existing application-memory files. State what each group can support, but do not repeat contact details, addresses, identifiers, or other personal values in the opening.

Then say that the local application memory has been created or updated and ask whether the user has anything new to add. Invite them to upload files, place them in the workspace, or paste relevant professional information. Explain that the skill will verify, categorize, and retain only reusable information in the appropriate private local file.

Use this Arabic shape, adapting it to the actual findings:

```text
وجدت ورتبت:
- السير الذاتية: <paths or filenames>
- البورتفوليو أو المشاريع: <paths or filenames>
- الشهادات أو الملفات الداعمة: <paths or filenames>

حدّثت ذاكرة التقديم المحلية بالمعلومات الموثقة. هل لديك شيء جديد تريد إضافته، مثل CV محدث أو مشروع أو شهادة أو رابط أو تصحيح لخبرة سابقة؟ أرسله هنا أو أضفه إلى هذا المجلد، وسأرتبه لاستخدامه في التقديمات القادمة.

عندما تكون جاهزًا، أرسل رابط وظيفة أو إعلانًا أو أخبرني بما تريد تجهيزه.

If you'd prefer to continue in English, just reply: English.
```

Omit empty categories. Do not claim a file was read or a profile was updated when it was excluded, unreadable, or unsupported.

## When the workspace has no usable professional material

Say plainly that no usable candidate-professional material was found. Explain that the skill can build the local organization from whatever the user provides, without requiring a particular folder structure.

Invite the user to add a CV, portfolio, project or case-study file, certificate, professional profile, or a pasted work-history summary. If they do not have files yet, ask them to share only the basic professional information they want the skill to use; do not pressure them to provide sensitive, legal, demographic, or authentication information.

Use this Arabic shape, adapting it to the user's context:

```text
لم أجد في هذا المجلد حتى الآن CV أو بورتفوليو أو مشروعًا أو شهادة أو ملفًا مهنيًا يمكن استخدامه.

أضف أو ارفع أي مادة لديك، أو اكتب ملخصًا مهنيًا قصيرًا. سأرتبها إلى خريطة للملفات، ومعلومات تقديم قابلة لإعادة الاستخدام، وخبرات موثقة لتكون جاهزة للتقديمات القادمة.

يمكنك البدء بـCV أو رابط بورتفوليو أو وصف مشروع أو تفاصيل خبراتك. ما الذي ترغب في إضافته أولًا؟

If you'd prefer to continue in English, just reply: English.
```

## Conversation rules

- Ask one helpful next question, not a long intake questionnaire.
- Keep Arabic as the conversation language unless the user explicitly requests English or clearly writes a conversational reply in English. Do not switch merely because a supplied CV, job post, or attachment is in English.
- Include `If you'd prefer to continue in English, just reply: English.` as the last line of the first orientation only.
- Do not ask for a job URL until after the orientation unless the user has already supplied one.
- If the user provided a specific job, post, or outreach task in the opening message, still give a brief discovery summary, then continue directly to that task instead of waiting for a separate confirmation.
- Keep the distinction clear: `CANDIDATE_CONTEXT.md` maps sources, `APPLICATION_PROFILE.md` stores reusable generic answers, `EXPERIENCE_PROFILE.md` stores verified experience, and `APPLICATION_TRACKER.md` records application progress.
