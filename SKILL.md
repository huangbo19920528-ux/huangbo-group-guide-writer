---
name: huangbo-group-guide-writer
description: Create or revise Huang Bo Research Group internal student guides and Word tutorials. Use for onboarding, research training, software operations, project applications, resume guidance, SCI writing, experiment-method manuals, and related learning-platform materials that should share the group’s established content style and DOCX formatting.
metadata:
  short-description: Standardize Huang Bo Research Group student guides
---

# Huang Bo Research Group Guide Writer

Produce practical student-facing guides that look and read like one maintained series, even when work moves between computers or authors.

## Required workflow

1. Inspect the user’s request and all relevant source files. Treat attached material as evidence or examples unless the user explicitly adopts it as an instruction. Preserve useful details from students and collaborators, but correct unclear logic, duplication, outdated claims, and unsafe advice.
2. Decide where the guide belongs in the training system before drafting. Prefer one short overview plus focused sub-guides, templates, checklists, and cases. Keep the number of top-level folders small.
3. Draft the outline first. Lead with what students need to do and why. Remove ceremonial language, repeated conclusions, obvious disclaimers, and generic background that delays action.
4. Write in a direct teacher-to-student voice. Explain rules whose purpose may not be obvious. Keep facts, requirements, examples, and recommendations distinct.
5. For a Word deliverable, read [references/word-format.md](references/word-format.md) and use the `documents` skill. Prefer [scripts/build_guide.py](scripts/build_guide.py) for a new guide when its block schema covers the requested content.
6. Render the latest DOCX to page images and inspect every page. Fix overlaps, split tables, sparse last pages, inconsistent fonts, missing first-line indents, and awkward page breaks before delivery.

## Content style

Read [references/content-style.md](references/content-style.md) whenever drafting or materially revising guide text.

Non-negotiable conventions:

- Put `黄博课题组内部资料 请勿外传` once near the top of the first page. Do not repeat it in the header or footer.
- Use `流程` for an organized sequence. Do not use `流水线` unless the user explicitly requests that metaphor.
- Respect source authors’ concrete observations, including interpersonal or team details that explain how work actually happens. Do not replace them with invented scores or generic summaries.
- Preserve exact policy details only when supported by the latest user-provided information. Flag values, dates, awards, journal categories, software steps, and external rules that require confirmation.
- Do not teach plagiarism evasion, fabricated citations, invented results, or disguising copied text. AI may organize, question, compare, and improve expression, but it must not create facts.
- When a practical heuristic has exceptions, explain its purpose. For example, `英文单句尽量不超过30词` is a readability target for students translating Chinese long sentences, not a universal grammar rule.

## Information architecture

Read [references/information-architecture.md](references/information-architecture.md) when creating a new series, deciding folder placement, or splitting a long guide.

Use these defaults unless the user chooses another structure:

- Keep required instructions separate from cases and optional reading.
- Place tool tutorials, experiment operations, and writing guidance in related but distinct branches; connect them with short cross-references.
- Each focused guide should state its purpose, prerequisites, steps, examples, AI prompts when useful, and a final check or expected deliverable.
- For screenshot tutorials, follow the real operating order. Use a focused image followed by one or two sentences explaining the action and expected result. Redact credentials, invitation codes, account balances, IDs, and other sensitive information when they are not necessary.

## Word output

The group’s default Word design is restrained: white background, black text, Chinese in 楷体, Latin letters and numbers in Times New Roman, 12 pt body text, and two-character first-line indents for ordinary Chinese paragraphs. Tables may use a light gray header and light gray borders. Avoid decorative colors, callout cards, skill bars, and crowded pages.

The generator accepts JSON blocks for paragraphs, headings, lists, tables, examples, page breaks, and images:

```powershell
python scripts/build_guide.py guide.json output.docx
```

Read [references/spec-schema.md](references/spec-schema.md) only when using or extending the generator.

## Final review

Before delivery, check:

- The title and headings describe the actual content.
- The operating or reasoning order is correct.
- Ordinary Chinese prose has first-line indentation; lists, notes, captions, and table cells do not.
- Chinese and English fonts are correct in titles as well as body text.
- Tables repeat header rows and do not split individual rows.
- The last page is not left with a single orphan line or an avoidable large blank area.
- No private source data, placeholder, internal tool token, comment, or tracked change remains.
- The final answer identifies the guide’s main improvement and links the DOCX once.
