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
| The specification could only be copied. | It can also be downloaded as a text file. |

## Open, decided for later

| Finding | Status |
|---|---|
| Card boxes repeat earlier answers and take too long. | To do. Prefill from the step answers and no boxes for GC-02. |
| The example is incomplete. | To do. Use the complete specification of Scenario 1 from the framework document. |
| Completeness is not checked in context. | To do. |
| Reflective designs ask for a correct-answer response. | To do. |
| Two candidate methods for simulated cases. | To do. |
| Step 7 results are not part of the specification. | Decision needed. |
| A second output written directly for a chatbot. | Decision needed. The framework treats the transfer to a chatbot as outside its scope. |
| Word download. | To do. |
| Browser Back leaves the page. | Minor. Not changed. |
| Content in a data block for easier editing. | After the walkthroughs. |
