# Guideline Cards Prototype

An interactive version of a lecturer guide for designing one educational chatbot conversation.
A lecturer answers one question in each of seven steps and receives a conversation design specification
that can be copied as text. No chatbot is built and no technical knowledge is needed.

**Try it:** https://guidecard-hub.github.io/guideline-cards/

The prototype belongs to a master thesis at the FHNW School of Business (MSc Business Information Systems):
*Conversation Design for Educational Chatbots: A Guideline-Based Conversation Design Framework with
Lecturer-Facing Guideline Cards for Higher Education*.

## What a lecturer does

1. Opens the page and reads the start page. The button "Load example" fills in a constructed example.
2. Works through the seven steps (purpose, learner situation, role, dialogue flow, feedback and repair, boundaries, review).
3. Uses the 14 guideline cards that the selection matrix recommends. Five cards are core cards and apply in every design.
4. Copies the finished specification and hands it to whoever sets up the chatbot, or uses it as a system prompt draft.

A lecturer needs one learning objective from a course they teach, the course material and the mistakes
students typically make in the topic.

## Documentation

| Page | Content |
|---|---|
| [How to use the prototype](docs/how-to-use.md) | Step by step guide for lecturers, tips and frequently asked questions |
| [Framework overview](docs/framework-overview.md) | The seven steps, the 14 cards, the selection matrix, roles and teaching methods |
| [Development notes](docs/development-notes.md) | How the page is built, how to change it, what was tested, known limits and the plan |

## Privacy

The page is one HTML file. It runs in the browser and sends nothing anywhere. Entries are stored only in the
browser of the person using it (local storage) and can be removed with the reset button or by clearing the browser data.
The only external request is an optional web font. Without it the page uses a default font.

## Browsers and devices

Tested so far in Chromium (Chrome and Edge engine) on desktop and at phone width, including opening the file
without an internet connection. Safari and Firefox have not been tested yet.

## Status

Prototype. It supports the application of the framework and has not been evaluated with lecturers yet.
The example in the tool is a constructed scenario, not a tested chatbot design. The wording of the cards follows
the lecturer guide of the thesis. The thesis is the authoritative source.

## Limits

- It does not build or run a chatbot.
- It covers one conversation for one learning objective at a time. The objective level "Create" is not covered.
- Entries are not synchronised between devices.

## Roadmap

- Shorter start page and plainer wording.
- Save and load of the entries as a file, and a download of the specification as a Word file.
- Accessibility check and tests in more browsers.
- Evaluation in walkthrough sessions with lecturers, as planned in the thesis.

## Use of AI

AI assistance (Claude by Anthropic) was used to develop this prototype, to check it against the thesis documents
and to draft the documentation. All content decisions and the final review are by the author.
The use of AI is declared in the thesis as well.

## Author and supervision

Gazmend Shefiu, FHNW School of Business.
Supervisors: Charuta Pande and Andreas Martin.

## Licence

No licence has been chosen yet. Until one is added, all rights are reserved by the author.

## How to cite

A citable version with a DOI will be added after the thesis is submitted.
