# Review log, 22 November 2026

Two AI assistants reviewed the published prototype independently with the same task description. Claude Code reviewed for about 40 minutes
and ChatGPT Codex for about 20 minutes. Both ran the page in several browsers, ran axe-core, tested keyboard use, storage failures,
two tabs and injection of text, and compared the page with the lecturer guide. The reviews are development work. They are not an evaluation
with lecturers and they are not evidence for the thesis results.

The findings below are grouped by what was done. Findings were checked against the page and the guide before they were accepted.

## Fixed after the review

| Finding | Change |
|---|---|
| Missing doctype, character encoding, language and viewport. Phones showed a shrunk desktop page. Quotes broke when opened from disk in WebKit. | Added to the page head. |
| "Start empty" and "Load example" could delete entries without a confirmation. | Both ask whenever anything was entered or changed. |
| Failed saves gave no warning. Two tabs overwrote each other silently. | A notice appears when saving fails and when another tab changed the entries. |
| No way to keep a draft. | "Save to file" and "Load from file". The page rejects files from other sources and asks before replacing entries. |
| Keyboard focus was lost after every change. | Focus stays on the control, and moves to the heading when the step changes. |
| The checkbox "Use this card" sat inside the card header. | It is now a separate control. |
| Low contrast of the row "Create" and of input borders. Small checkboxes. | Colours and sizes changed. |
| Fonts were loaded from Google. | System fonts only. The page makes no external requests. |
| Start page was long. | Start buttons at the top, details behind "Read more". The step bar scrolls on phones. |
| "Instance fields" is a thesis term. | The interface says "course details". |
| GC-07 was missing in the step 5 overview. | Added, as in the guide. |
| The example filled the course details of only three of its twelve cards. | The example now follows Scenario 1 of the framework document in full, including the hints, the worked example and the acceptance criterion. Only the review in step 7 is left open on purpose. |
| Reflective designs asked for a response to a correct answer, required misconceptions and had no field for an action that the student has not evaluated. This error came from the page, not from the guide. | Step 5 shows the criterion, the response to an unsupported judgement and the response to an unevaluated action. Misconceptions are optional. |
| GC-02 asked for boxes that do not exist for a design-time card, and its text did not fit a chatbot. | GC-02 has no boxes. The specification states the chosen teaching method. |
| The results of the review (step 7) were not part of the specification. | The specification ends with a review record, marked as a note for the lecturer and developer. |
| The specification could only be copied. | It can also be downloaded as a text file. |
| Card boxes repeated answers from earlier steps. | Cards for GC-04, GC-05, GC-11 and GC-14 show the earlier content in a linked block with an edit button. The boxes are for what is new. |
| The buttons "Start empty" and "Load example" changed their label for 4 seconds and then switched back, which was confusing. The label could also stay stuck. | Both now show a message under the buttons that stays until you choose "Delete my entries" (or "Replace my entries") or "Cancel". Escape cancels. The message tells you to use Save to file first. |
| Every card asked for three boxes, and many repeated an earlier answer (45 percent of the typed text in the AI time tests). | Each card has one box "Your decision". The example from the course and the notes are optional and sit behind a link. GC-10 starts with its default of two hints. The badge in the card header updates while typing. |
| Ticking cards closed the other open cards. | Open cards stay open when the page updates. |
| On steps 3, 4 and 6 a card said "Nothing written in step N yet" while the lecturer was in that step, and the block did not update while typing. | On the same step the card shows a short note that it uses the answer above. The block "Taken from step N" stays for GC-11, whose content comes from step 2. |
| The checkbox "Use this card" had no card name for screen readers. | The name now includes the card id and title. |
| A stored design from an earlier visit opened without a question. | On the first visit of a browser session, the page asks to continue or to delete it and start empty. |
| Step 7 ticks were of little use and unclear. | Step 7 explains what to do, shows what the design says for each test input, highlights open items, links to the steps concerned and counts open items. All items must be ticked for the step to count as done. |
| The last two checklist questions needed the specification, so the lecturer had to leave step 7 and come back (second AI time test). | The two questions are on the specification page, below the text. Ticking them updates the review record in the specification and the list of open items. |
| The specification printed task steps, misconceptions and boundaries twice (in the worksheet and again in the card section). | The card section points to the section above ("Content: see section N"). Lists are printed once. The optional example is printed only when written. |
| GC-10 was prefilled with a default, and the specification listed it as a value chosen by the lecturer. | No prefill. The box shows the default as a hint, the badge says "Default is used", and the specification says "none given, default of the card". |
| GC-11 counted as filled because the misconceptions came from step 2, although the attempt limit was empty. | GC-11 needs its own decision. |
| The test input "an error that persists" did not show the GC-11 limit. | It shows the hint limit, the attempt limit and the boundary rows. |
| GC-05 is not recommended for the misconception row, but a task with steps needs it. | The card says that the matrix does not recommend it and that the lecturer may use it when steps were entered in step 4. |
| The button "Use all recommended cards of this step (N)" was unclear, and "instance fields" appeared in the specification. | The button reads "Tick the N recommended cards that are not ticked yet". The specification says "decisions for the cards". |
| The figure of the response order from the Word guide was missing in the web version. | Added to step 5 as a figure that is closed by default and opens larger on a click. It is the vector figure from draw.io (Figure 4, Response routing), embedded in the single file. The overview of the seven steps was already part of the start page as a clickable list. |
| The idea that a card is a ready-made rule and that the lecturer fills it in for the course was not stated in plain words. | One sentence in "How the cards work" on the start page, in the README and in the lecturer guide (v6). |

## Open, decided for later

| Finding | Status |
|---|---|
| Completeness is not checked in context, for example both sides of a pair. | To do. |
| Two candidate methods for simulated cases. | To do. |
| A second output written directly for a chatbot. | Decision needed. The framework treats the transfer to a chatbot as outside its scope. |
| Word download. | To do. |
| Browser Back leaves the page. | Minor. Not changed. |
| Content in a data block for easier editing. | After the walkthroughs. |
