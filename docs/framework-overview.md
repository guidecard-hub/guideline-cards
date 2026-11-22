# Framework overview

This page summarises the framework behind the prototype. The full definitions are in the thesis.
The text of the cards in the prototype follows the lecturer guide of the thesis.

## The seven steps

1. **Purpose definition.** What should students be able to do after the conversation, and what will they do in it? (GC-01)
2. **Learner situation analysis.** What do students already know, which misconceptions are typical, and which teaching method fits? (GC-02, GC-03)
3. **Conversation role selection.** Which role does the chatbot take? (GC-04)
4. **Dialogue flow design.** In which order does the conversation run? (GC-05 to GC-09)
5. **Feedback and repair planning.** What happens after a correct, incorrect, misconceived or unclear answer? (GC-10 to GC-13)
6. **Boundary definition.** What does the chatbot refuse, and where does it send students? (GC-14)
7. **Review.** Is the design ready to be used? (checklist)

## The 14 guideline cards

Core cards apply in every design. The other cards are selected with the matrix below.

| Card | Name | Stage | Core | Use it when |
|---|---|---|---|---|
| GC-01 | Make the goal visible | 1 Purpose definition | yes | Opening of every conversation |
| GC-02 | Choose the teaching method | 2 Learner situation analysis | yes | Design time, at the end of stage 2, after you have defined the learning objective and the intended student activity and have analysed the learner situation |
| GC-03 | Diagnose before helping | 2 Learner situation analysis | no | After the opening, before any explanation or task |
| GC-04 | Declare the role and its limits | 3 Conversation role selection | yes | Opening of the conversation, together with GC-01 |
| GC-05 | One step at a time | 4 Dialogue flow design | no | Multi-step tasks such as modelling, calculating or analysing a case |
| GC-06 | Explain in small steps | 4 Dialogue flow design | no | The diagnosis shows a gap, or the student asks for an explanation |
| GC-07 | Ask for the reasoning | 4 Dialogue flow design | no | In tasks with an expected answer, the student gives a correct answer and the reasoning is needed. In reflective tasks, the student gives an unsupported judgement or describes an action without evaluating its consequences against the agreed criterion. |
| GC-08 | Set a goal and plan | 4 Dialogue flow design | no | After a reflection, or at the start of a self-study session |
| GC-09 | Close with reflection | 4 Dialogue flow design | no | End of the task or session |
| GC-10 | Hint before solution | 5 Feedback and repair planning | no | The student gives an incomplete or incorrect answer that does not match a known misconception |
| GC-11 | Address the misconception | 5 Feedback and repair planning | no | The answer matches a misconception that you listed in stage 2 |
| GC-12 | Clarify instead of guessing | 5 Feedback and repair planning | yes | The input of the student within the task is unclear or ambiguous |
| GC-13 | Feed forward | 5 Feedback and repair planning | no | After an answer has been evaluated, following GC-07, GC-10 or GC-11 where they apply |
| GC-14 | Redirect and escalate | 6 Boundary definition | yes | Requests outside the role, such as off-topic questions, requests to solve graded work, organisational or personal issues, or repeated failure |

## Selection matrix

The lecturer picks the row that matches the main purpose of the conversation.

| Purpose of the conversation | Teaching method | Suitable roles | Recommended cards |
|---|---|---|---|
| Introduce or explain unfamiliar content | Explanation with check questions | Tutor, Course assistant | GC-03, GC-06, GC-13 (Tutor also GC-07, GC-09, GC-10) |
| Examine and revise a particular misconception | Feedback on misconceptions | Practice partner, Tutor | GC-03, GC-06, GC-07, GC-10, GC-11, GC-13, GC-09 |
| Practise performing a task | Guided practice | Tutor, Scenario guide | GC-05, GC-07, GC-10, GC-11, GC-13, GC-09 (Tutor also GC-03) |
| Practise or examine a task in a simulated case | Guided practice or feedback on misconceptions | Scenario guide | GC-05, GC-07, GC-10, GC-11, GC-13, GC-09 |
| Evaluate own experience and plan improvement | Reflective prompting | Reflective companion | GC-07, GC-08, GC-09 |

## Roles

- **Tutor.** Guides the student through a task and gives hints and feedback.
- **Practice partner.** Works on a problem together with the student as an equal.
- **Course assistant.** Answers questions and points to course material.
- **Scenario guide.** Plays a character in a simulated situation, for example a stakeholder.
- **Reflective companion.** Asks open questions and supports planning and self-assessment without judging.

## Teaching methods

- **Explanation with check questions.** The chatbot explains one idea with an example and then checks understanding with a question.
- **Guided practice.** The student solves a task step by step and receives hints and feedback at each step.
- **Feedback on misconceptions.** The chatbot recognises a known misconception and lets the student test it against a counterexample.
- **Reflective prompting.** The student reflects on their own work and sets a goal for the next step.

## Review checklist (step 7)

1. Does every part of the conversation serve the learning objective of step 1?
2. Does the order contain opening, diagnosis, guidance, feedback, repair, progression and closing where they are needed?
3. Can you name the pedagogical goal of every chatbot move?
4. Does the chatbot state its role, and is there a response for every request outside the role?
5. Does the specification describe the design without depending on a particular chatbot tool?
6. Could a colleague without chatbot experience understand the specification?

## Output

The result is a conversation design specification. It contains the conversation order, the cards the lecturer chose and the values for the course. It does not depend on a particular chatbot tool, and no chatbot is built.
