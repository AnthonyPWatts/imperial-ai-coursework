# Document Style Guide

Internal working notes for Word handouts, PDF exports, and code-along documents.

This style was established from the reviewed `ml-foundations/first-practical-workflow` documents, especially documents `01` to `04`. Use Word `.docx` as the editable source of truth, and only export to PDF when a separate review/share artifact is useful.

## Overall feel

- Practical, calm, and readable.
- More like a guided code-along than a textbook chapter.
- Colour is used to signal document structure, not as decoration.
- Keep pages airy. Avoid dense walls of prose.
- Prefer small, inspectable steps over compact cleverness.

## Page structure

- A4 portrait.
- Small grey running header at the top: document family plus step number.
- Page number in small grey text at the bottom right.
- Large blue title on the first page.
- Subtitle below the title: `A First Practical Machine Learning Workflow`.
- Numbered blue section headings, for example `3. Import pandas when the table needs it`.

## Colour roles

Use colour consistently:

- Blue heading text: major section titles and document titles.
- Dark-blue table header rows: ordinary comparison or summary tables.
- Pale-blue boxes: purpose, setup, and `Why this cell exists`.
- Pale-green boxes: `What to look for`, concept reinforcement, and positive reading guidance.
- Pale-amber boxes: rules, warnings, common mistakes, and "do not over-read this" notes.
- Light-grey boxes: code cells, terminal commands, paths, and formula-like snippets.

Do not flatten all callouts into the same neutral style. The colour coding is part of the teaching flow.

## Teaching rhythm

The preferred rhythm is:

1. Say where the step sits.
2. Explain the idea before the code.
3. Introduce one new tool only when it is needed.
4. Give a small code cell.
5. Explain what to look for in the output.
6. Add a checkpoint before moving on.

Keep repeating this rhythm. It makes the material feel safe to follow.

## Terms sections

- Each PDF/chapter should end with a lightweight `Terms to say out loud` or `Glossary` section.
- Aim for 5-10 entries, but use fewer in very early chapters if the chapter has not introduced enough terminology yet.
- Keep entries short and retrieval-focused: the reader should be able to say the term and a plain-English meaning without turning the notes into a dictionary.
- Repeat important terms across nearby PDFs when repetition helps drill the workflow.
- Maintain a separate cumulative `Glossary of Terms` PDF for the sequence.

## Code cells

- Label code blocks as `Code cell` when they are meant for the notebook.
- Put code in light-grey boxes.
- Keep imports close to the first point where the imported object is needed.
- Avoid introducing multiple new concepts in one cell.
- Prefer explicit intermediate variables over clever one-liners.
- If a display value should be rounded, keep raw values for calculation and round only for display.

## Language

- Use plain English first.
- Explain why a cell exists before asking the reader to run it.
- Use direct phrases such as `What to look for`, `Why this cell exists`, and `Avoid this common mistake`.
- Avoid grand claims from toy data.
- Use hyphens rather than decorative dashes.
- Use `fit()`, `predict()`, `X_train`, and similar code terms inline when they are the exact object of attention.

## Tables

- Use tables for compact comparisons, not for everything.
- Table headers should be dark blue with white or high-contrast text.
- Keep rows short enough to scan.
- Wrap long cell text cleanly. Never allow columns to collide.
- In `Where this step sits` tables, show a local window of the sequence rather than the whole course: maximum 5 documents.
- Aim to put the current document in the middle of that window. For the first and last few documents, shift the window gracefully so it still shows useful neighbouring steps.
- Clearly mark the current document row using the pale blue row highlight and bold text. Do not add a separate pointer arrow or marker; it is visually noisy and creates fragile layout artifacts.

## Review checklist

Before considering a PDF done:

- It visually matches the established family: blue headings, colour-coded boxes, grey code cells, and page footer.
- `Where this step sits` tables use a maximum 5-row local window and clearly mark the current document with row highlighting and bold text only.
- The final terms/glossary section exists and stays lightweight.
- No section or checkpoint is stranded on a mostly empty final page.
- No table text overlaps or collides.
- Code blocks fit inside their boxes.
- The page count feels intentional.
- The final rendered pages have been inspected, not just generated.
