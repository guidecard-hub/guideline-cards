# How to use the prototype

## Before you start

You need three things for one conversation you want to design.

- One learning objective from a course you teach.
- The course material for it.
- The mistakes students typically make in this topic.

Plan about 45 to 60 minutes for a first run. The page does not need an account or an installation.

## Open the page

Go to https://guidecard-hub.github.io/guideline-cards/ in a current browser.
You can also download `index.html` from this repository and open it by double click.

Two buttons are at the top right.

- **Load example** fills in a constructed example about modelling a process in BPMN. Use it to see how a finished design looks.
- **Save to file** writes your entries to a small file on your computer. Do this before you close the page for the last time.
- **Load from file** reads a file saved with the button before. A file from another source is rejected.
- **Start empty** clears all entries.

Load example, Load from file and Start empty ask you to confirm whenever you have entered anything, so that your work is not replaced by accident.

## The seven steps

| Step | Question | Cards |
|---|---|---|
| 1 Purpose | What should students be able to do after the conversation? | GC-01 |
| 2 Learner situation | What do students know, which misconceptions are typical, which teaching method fits? | GC-02, GC-03 |
| 3 Role | Which role does the chatbot take? | GC-04 |
| 4 Dialogue flow | In which order does the conversation run? | GC-05 to GC-09 |
| 5 Feedback and repair | What happens after a correct, incorrect, misconceived or unclear answer? | GC-12, GC-07, GC-10, GC-11, GC-13 |
| 6 Boundaries | What does the chatbot refuse and where does it send students? | GC-14 |
| 7 Review | Is the design ready to be used? | Checklist |

The overview of the seven steps is the list on the start page. Select a step to jump to it. In step 5 you can open a figure that shows what the chatbot does after a student answer. Select the figure to see it larger. It is closed by default, so you only open it if you want it.

In steps 2 to 6 you open the cards of the step. Each card has one box for your decision. You can also add an example from your course and a note, but you do not have to. The button "Use all recommended cards of this step" ticks the cards that the
selection matrix recommends. Nothing is ticked without a click.

You do not write anything twice. If a card needs content that you already wrote in an earlier step (the role and opening sentence for GC-04, the steps of the task for GC-05, the misconceptions for GC-11, the contacts for GC-14), the card shows it in a block "Taken from step N" with a button to edit it there. If that step is still empty, the card shows a warning instead. On the same step the card only reminds you that it uses your answer above. The decision box is for what is new in the card. GC-02 has no boxes because the teaching method is chosen at design time.

## Step 7 Review

Step 7 tells you what to do. It lists the test inputs, each with what your design says the chatbot does (taken from your own entries in steps 5 and 6), and four checklist questions, each with links to the steps concerned. The two checklist questions about the specification (independent of a chatbot tool, understandable for a colleague) are on the page of the specification, below the text, because you can only answer them after reading it. Items that are not ticked have a coloured edge, and a counter shows how many are still open. If your design has nothing written for a situation, the page says "Nothing written yet" and a button takes you to the step. The test inputs show whether every situation that a student can cause is covered in your content. They are not a check that fields are filled. They are also the acceptance test for a chatbot built later from the specification.

## Reflective conversations

If your purpose is to evaluate your own experience and plan improvement, choose the last row of the selection matrix. Step 2 then needs no
misconceptions. Step 5 asks for the criterion against which students evaluate their actions and for two responses, one to an unsupported
judgement and one to an action whose consequences the student has not evaluated. There is no response to a correct answer.

## The specification

The last page shows the specification with the conversation order, the cards you chose and your values.
At the end, a review record shows the ticks of step 7. It is a note for you and the developer, not an instruction to the chatbot. Missing items, including open review questions, are listed above it. Copy the text or download it as a text file and keep it as a document. Update it when your course changes.

## Tips

- Take a real objective from your course, not a general one. The cards are easier to fill in with concrete content.
- Start with the example if you are unsure what a good entry looks like.
- If you are unsure about the role, read the role descriptions on the start page and in step 3. You decide, the page does not.
- If nothing in the design describes what the chatbot does after a type of answer, go back to the step concerned.

## Frequently asked questions

**Does the page build a chatbot?** No. It produces a specification. A developer, or you, can use it to build or prompt a chatbot.

**Where are my entries stored?** Only in your browser on this device. They are not sent anywhere. Clearing the browser data removes them.
If the browser cannot store them, the page shows a notice. Use "Save to file" to keep a copy. If you open the page in two tabs, the page warns you that the other tab changed the entries.

**Can I use it on a phone?** Yes, but a larger screen is easier for the text boxes.

**My objective is to create something. What do I choose?** The level "Create" is not covered by this version.
Choose another objective for the conversation, or note which row you use instead and why.

**Which chatbot tool do I need?** None. The specification does not depend on a tool.

## Feedback

Please send comments and problems to the author or open an issue in this repository.
