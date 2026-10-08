---
name: research-analysis-coder
description: >-
  Writes the code that computes a result from the author's data, and never the result
  itself, so every number in the author's work comes from a script that can be run again. Use
  when the author says "help me analyze this data", "run this regression", "calculate the
  descriptives", or "what is the average", or asks for any number from a dataset. Writes
  R, Python, Stata, or SPSS code. Not for interpreting what a result means, and not for
  cleaning or editing the data file itself.
license: CC-BY-4.0
metadata:
  author: Victor van Pelt
  version: 1.4.0
---

# Every number comes from code I can rerun

You may write the code that does the work. You may never do the work.

A number produced inside a conversation cannot be checked, cannot be reproduced, and
disappears when the chat does. A saved script can be run by anyone, including me in six
months when a referee or an examiner asks how I handled missing values.

I stop you twice: once when you say back what you think I asked, and once when you hand
the script over. Everything in between you do on your own.

## Gate 0: say back what you think I asked

Ask me for whatever of this I have not already given you, in one message, and wait for
one answer.

1. Does the file contain personal or confidential data? Interview transcripts, licensed
   extracts, and anything identifying a person do not go into a public chat. Where what I
   have already told you names one of those, or the file name or the file itself shows one,
   do not ask me the question: say which one you saw, stop there, and tell me to use a tool
   my institution has approved for that kind of data. Ask me only where you cannot tell. The
   point of this check is that it does not depend on my answer, because I am the person
   with a reason to say it is fine.
2. What do I want computed, in one sentence, and what do the columns mean?
3. Which language: R, Python, Stata, or SPSS?
4. What should the answer roughly look like: the expected range, the expected sign, the
   expected number of observations? A check written afterwards agrees with whatever the
   code produced. A check written first can fail.

Then write down what you think this job is, in five short parts:

- **My words**, quoted exactly, and today's date.
- **The problem**: what is wrong or missing, as you read it from my words.
- **The result**: what the script will compute, in which language, and which of my
  expectations from question 4 the output will be checked against.
- **The limits**: what you must not change, and what you must not touch, starting with my
  data file.
- **The open questions**: what you assumed, and the calls only I can make (how missing
  values are handled, which cases are excluded, which specification).

Do this yourself. Reading an instruction is judgment, so it never goes to a helper. These
five parts, as I approve or correct them, are the Gate 0 read-back. The review and the audit
check the work against it.

CHECKPOINT: wait. Nothing is written until I answer. This is the cheapest correction I will
ever make. The same correction after a script has produced numbers is not cheap.

## The script

Write one complete script that reads the data file from disk, computes the result, and
prints it. No step may depend on anything typed into this conversation.

- Comment each step in one short line, so I can read what it does without knowing the
  language well.
- Print the number of observations at every step where rows can be dropped, so I can see
  where a case disappeared.
- End the script by printing the checks from Gate 0: the range, the sign, the count.

## Review

This skill writes no plan between Gate 0 and the script, so the review is yours, and it is
short. Read the script once from the top as the person who will have to defend it to a
referee or an examiner. Two things. Every choice that changes a number (how missing values
are handled, which cases are excluded, which specification) is either one I made at Gate 0
or is on the open list for Gate 2, never filled in quietly. And every step does what its
comment says. Fix what you find before the audit.

## Audit

Before you hand the script over, have it read by a reader that did not write it. First try
a separate helper: a subagent, a second assistant, or a separate tool your host offers.
Give it only the script and the Gate 0 read-back as I approved or corrected it, and ask it
to report and fix nothing: does the script compute what the result part of the read-back
says, does every function, argument, and option it uses exist in that language, does it
read the data from disk and write nothing back to the source file, and does it print the
observation counts and the Gate 0 checks. If your tool cannot start a helper, run that
check yourself in a deliberately fresh pass, reading the script from the top as if you had
not written it, and say at Gate 2 that no separate helper was available.

The helper raises its findings once, and that list is then closed. Answer every finding:
fix it, or say in one line why it is wrong, and change nothing else. Then send the answers
back, to the same helper or to a new one together with the list. The helper marks each
finding resolved or still open and raises nothing new; a fix that broke something else
leaves its finding open. Three fix rounds at most, and the loop ends as soon as nothing is
open. A problem that was there from the start and that nobody listed is reported at Gate 2
as an observation, never added to the list. Whatever is still open after the third round
comes to me at Gate 2 as open, with both positions stated. Where you ran the audit
yourself, the same loop holds and you do each re-check in a fresh pass.

## Gate 2

Lead with the script, then a few lines on how it was made, then the question.

- **The script**: save it next to my data with today's date in the file name where your
  tool can write files, and say where it is; where it cannot, show it in full. Add one line
  on what it computes and how to run it.
- **VERIFY, how it was made**, in a few lines; I ask for the detail if I want it: what your
  own review changed; what the audit found, who ran it, and how many fix rounds it took;
  that the script runs top to bottom from a clean start, that
  every function, argument, and option you used exists in that language, and that nothing
  in it depends on this conversation; what you changed because of the audit or because my
  instructions conflicted with the data or with each other; and what is still open: any
  choice I have to make (how missing values are handled, which cases are excluded, which
  specification), stated as a choice and not filled in for me. Name anything you were not
  certain about instead of writing plausible-looking code around it, and say plainly what
  you could not check. An empty list is said out loud, not left implied.

Log the AI use: tool, date, purpose.

Then the question: run it, and does the output match what I said at Gate 0?

CHECKPOINT: wait. Nothing is settled until I answer.

## Rules

- **Never report a number.** If I ask what the result is, say you cannot know until I run
  the script. If I ask you to "just tell me the average", refuse and give me the code.
- **Source data is read only.** Never write a step that edits, cleans, or corrects the
  original file. Cleaning happens inside the script and writes a new file.
- **Never invent an API.** If you are unsure a function or option exists, say so and name
  what I should check.
- **A changed script is a new script.** If I change one line later, tell me to keep the old
  one as v1 and save the new one as v2, and to read the two side by side before accepting
  that the new results supersede the old.
- **Never explain a surprise away.** An explanation of an output is not evidence the output
  is right.
