# Development notes

## Structure

The prototype is one file, `index.html`, with markup, styles and script together. It uses plain JavaScript,
no framework and no build step. This keeps it easy to hand out. Opening the file or the published page is all that is needed.

The content is held in a few constants at the start of the script.

| Constant | Content |
|---|---|
| `CARDS` | The 14 guideline cards with stage, core status, suitable roles, use, chatbot move, example, limits and decision |
| `ROWS` | The five rows of the selection matrix with purpose, teaching method, roles and recommended cards |
| `CHECKS` | The six questions of the review checklist |
| `TESTS_TASK`, `TESTS_REFL` | The test inputs for the review of a task design and of a reflection design |
| `EXAMPLE` | The constructed example (BPMN order process) |
| `EMPTY` | The empty state of a design |

The state of a design is stored in the browser under the local storage key `gc-proto-v2`. Reading and writing are
wrapped in try and catch, so the page still works if the browser blocks storage.

## How to change the content

Change the constants and keep them consistent with the thesis. The wording in the cards, the matrix, the checklist and the
test inputs must match the lecturer guide. After a change, open the page, load the example and go through all seven steps.

## What was tested

- A blind click-through with an own learning objective (business mathematics) for a calculation task and for a reflective task.
- Comparison of all 14 cards, the matrix, the checklist and the test inputs with the guide and the framework document.
- Automated click-through with Playwright in Chromium at desktop and phone width, including save and load, blocked storage, two tabs, keyboard focus and downloads.
- Step 5 figure (response order): opens and closes with click, button and Escape, stays open while typing, readable in light and dark mode and at phone width.
- Opening the file from disk without an internet connection. No script errors and no sideways scrolling.
- Two independent AI-assisted reviews on 22 November 2026 (Claude Code and ChatGPT Codex). See [review-log.md](review-log.md).

These are checks of correctness by the author and AI assistants. They are not a usability test with lecturers.

## Findings during development

- **Specification not self-contained (22 November 2026).** The author pasted a specification into a general chatbot.
  The chatbot could not know what a guideline card or the label GC stands for, because the text only named the cards.
  Change: the specification now starts with a short explanation of how to read it and lists, for every selected card,
  when it applies, what the chatbot does, its limits and the values chosen by the lecturer. The role description is included.
  This matches the thesis, where the specification contains the worksheet and the selected cards.

## Known limits

- Not tested in Safari on a Mac or iPhone, on touch hardware or with a screen reader.
- Accessibility was checked with automated tools by the reviewers, not with assistive technology.
- A full design may take longer than 60 minutes. Three AI time tests on 23 November 2026 estimated 69 to 150 minutes for a lecturer (estimates, not measurements with lecturers). The study plans 60 to 90 minutes and a preparation by the lecturer.
- The page does not check that a design is complete in context, for example both sides of a pair.
- The specification can be copied or saved as a text file. A Word file is not available yet.
- The specification is written as a design document. It has not been tested systematically with different chatbots.
- The page uses the thesis term "instance fields" only in the explanation of the term. The interface says "your decision" for the card box and explains the term.

## Plan

1. Check of completeness in context.
2. Download of the specification as a Word file.
3. Decision whether the specification needs a second version written directly for a chatbot.
4. Decision whether to move the content into a data block, after the walkthroughs.
5. Accessibility check with a screen reader and tests in Safari.
6. Evaluation in walkthrough sessions with lecturers.

## Use of AI in development

The prototype was developed with the help of Claude (Anthropic). The AI assistant wrote and tested the code and drafted
the texts. The author gave the requirements, decided on the content and reviews the result. The thesis documents are the
reference for correctness.

## Linked card content

`LINKS` lists the cards that reuse an earlier answer (GC-04, GC-05, GC-11, GC-14). `linkText(id)` builds the text from the step entries.
`testSource(k)` does the same for the test inputs of step 7. When you add a card that reuses a step answer, add it to `LINKS`.
`counts:false` (GC-11) means the linked text does not count as the decision of the card. `sec` and `secname` give the section of the specification that holds the text, so the card section only points to it.

## Defaults and review questions

`DEF` holds defaults of cards (GC-10). A default is never written into the box. `statusOf(id)` gives the badge (decision filled in, taken from step N, default is used, write your decision). `SPECCK` lists the checklist questions that are answered on the specification page (indexes 4 and 5). `refreshSpec()` updates the text and the list of open items when one is ticked.
