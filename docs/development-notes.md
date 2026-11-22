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
- Automated click-through with Playwright in Chromium at desktop and phone width.
- Opening the file from disk without an internet connection. No script errors and no sideways scrolling.

This is a check of correctness by the author and the AI assistant. It is not a usability test with lecturers.

## Known limits

- Not tested in Safari and Firefox.
- No accessibility audit yet. Keyboard use and screen readers have not been checked systematically.
- The start page is long. About 900 words on three screens.
- The term "instance fields" comes from the thesis and is not a lecturer's word.
- Entries live in one browser only. There is no save to file yet.
- The specification can only be copied as text.

## Plan

1. Shorter start page and plain wording.
2. Save and load of the entries as a file. Download of the specification as a Word file.
3. Accessibility check and tests in more browsers.
4. A decision whether to split data and code into separate files, after the walkthroughs.
5. Evaluation in walkthrough sessions with lecturers.

## Use of AI in development

The prototype was developed with the help of Claude (Anthropic). The AI assistant wrote and tested the code and drafted
the texts. The author gave the requirements, decided on the content and reviews the result. The thesis documents are the
reference for correctness.
