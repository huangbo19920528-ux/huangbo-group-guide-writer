# Word Format

## Page and typography

- Page size: A4 portrait.
- Margins: top 2.0 cm, bottom 1.9 cm, left 2.4 cm, right 2.4 cm.
- Footer distance: 0.8 cm.
- Background: white.
- Text color: black. Small notes and page numbers may use medium gray.
- Chinese font: 楷体.
- Latin letters and numbers: Times New Roman.

Apply both the East Asian and Latin font attributes to every relevant Word style and direct run. Do not assume the visible Chinese title will inherit the correct East Asian font from `run.font.name` alone.

## Type hierarchy

| Element | Size | Treatment |
| --- | ---: | --- |
| Internal notice | 14 pt | Bold, centered, first page only |
| Document title | 22 pt | Bold, centered, Word Title style, no border |
| Subtitle | 15 pt | Centered |
| Heading 1 | 16 pt | Bold, black, keep with next paragraph |
| Heading 2 | 14 pt | Bold, black, keep with next paragraph |
| Heading 3 | 12 pt | Bold, black, keep with next paragraph |
| Body | 12 pt | 1.35 line spacing, 4 pt after |
| Small note | 10 pt | Gray, 1.2 line spacing |
| Table text | 9.8 to 10.5 pt | Choose by density; do not shrink below readability |
| Footer page number | 9 pt | Gray, centered |

Ordinary Chinese body paragraphs use a two-character first-line indent. Lists, numbered steps, notes, captions, examples, table cells, titles, and headings do not use first-line indentation.

## Tables

- Use light gray borders, normally `#D9D9D9`.
- A light gray header fill is acceptable; keep header text black and bold.
- Choose column widths from the content. Short labels should not receive the same width as explanations.
- Vertically center cell content. Center short labels and numbers; left-align explanations.
- Repeat the header row across pages and prevent individual rows from splitting.
- Leave space above and below tables. Avoid a table that exists only to box a paragraph.

## Images and screenshots

- Preserve aspect ratio and crop to the interface area needed for the step.
- Center the image and keep it with its caption or explanation when possible.
- Follow each operational screenshot with one or two sentences explaining what to click, paste, confirm, or expect.
- Do not include credentials, invitation codes, account balances, personal messages, manuscript IDs, or other identifiers unless they are required and the user authorizes them.
- Prefer the original screenshot or slide crop over recreated text when the visual arrangement carries meaning.

## Pagination and QA

- Use centered page numbers in the footer.
- Keep headings with the first paragraph or table that follows.
- Avoid a final page containing only a short note or one table row when the document can be reflowed naturally.
- Render the latest DOCX and inspect every page at full readable size. Text extraction alone does not validate layout.

