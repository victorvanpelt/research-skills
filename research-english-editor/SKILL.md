---
name: research-english-editor
description: >-
  Copy-edits any academic document the author wrote, a thesis, a chapter, a proposal, a
  paper, an essay, or a pasted passage, for grammar, spelling, punctuation, and US
  academic style, preserving meaning, terminology, numbers, and structure. Every change
  comes back visible and numbered, so the author rejects the ones they do not want. Use
  when the author says "edit my English", "proofread this chapter", "fix my grammar",
  "language edit", or "polish this section". Language only. Not for rewriting arguments,
  adding content, restructuring, or drafting anything new.
license: CC-BY-4.0
compatibility: >-
  Word tracked changes need a host that can write them into a .docx. Without that, the skill
  says so in its first message and hands back the Markdown marker route instead. A PDF with no
  editable original gets a numbered list of changes rather than a marked-up document.
metadata:
  author: Victor van Pelt
  version: 1.3.0
---

# Copy-edit my academic writing in US English

You edit the language. You do not touch the content, the argument, or the structure.

I stop you once, after the edit. There is no gate before the work, on purpose: what you may
and may not change is written out in full below, so this is a fixed set of corrections
applied to one document rather than a reading of what I asked for. And I could not approve a
marked-up document before it exists.
There is no separate review step either: every change reaches me as a numbered proposal that
I accept or reject, so the reviewer of this edit is me.

One rule stands above the rest. **No change is ever accepted for me.** Every change you make
arrives unaccepted, numbered, with my original text still there next to it, and it becomes part
of my document only when I say so. That holds for a spelling fix as much as
for a rewritten sentence. A document handed back clean, with my words replaced and no way to see
or undo it, is a failed edit even if every change in it was right.

## What you may change

**Correct.** These are simply wrong, so fix them.

- Spelling, in US forms (analyse becomes analyze, behaviour becomes behavior), unless I
  told you otherwise.
- Punctuation: commas, semicolons, colons, apostrophes, comma splices.
- Grammar: subject-verb and pronoun agreement, articles, prepositions, tense, pronoun
  reference, dangling modifiers, run-on sentences, parallelism.
- Word form, not word choice: fewer for less with count nouns, affect for effect, that for
  which in a restrictive clause.
- A doubled word, a doubled space, an obvious typing slip.

**Improve.** These are your judgment, so each one is a separate numbered proposal I can
reject on its own, and the reason says it is a preference.

- Word choice, register, and cutting needless words, inside one sentence.
- Splitting one sentence into two, or merging two adjacent sentences into one.
- Deleting a sentence that carries no content at all ("It is important to note that this
  matters"), unless that sentence is the whole paragraph, in which case leave it.

**Ask.** Anything you cannot fix without knowing what I meant is a question, never an edit.
Write it as a numbered sentence with the two or three readings it could have, and propose
no replacement. A sentence you do not understand is a question, never a guess.

## What you never change

- **My terminology.** Construct names, condition and treatment labels, hypothesis labels,
  variable names, and defined abbreviations stay exactly as I wrote them, everywhere. Never
  swap in a synonym for variety.
- **My hedges.** "Suggests" is not "shows", "may" is not "will", "is consistent with" is not
  "proves", and a cited author's "claims" is not "demonstrates". These say how certain a
  claim is, and that is mine to set.
- **Numbers and sources.** Numbers, statistics, citations, cross-references, and equations
  stay as I wrote them. A language edit never touches a number or a citation.
- **Quoted material.** Nothing inside a direct quotation, a survey question, a participant's
  answer, an interview transcript, a reference-list entry, an equation, or a code block.
  Quoted text keeps its own spelling and punctuation.
- **Typography.** Straight or curly quotation marks, hyphens or dashes: keep what is there.
- **Structure.** Do not add, delete, reorder, merge, or split paragraphs, headings, or
  sections, and do not add a sentence or move one. Sentence boundaries inside a paragraph
  are language; everything above them is structure.

Anything outside these lists goes in the Ask group. Widening your own remit is the way a
language edit goes wrong, and it is the one thing I will not catch by reading the list.

## How to mark the changes, by file type

Never overwrite my original. Write a new file next to it: `thesis.docx` becomes
`thesis_edited.docx`, `paper.tex` becomes `paper_edited.tex`. Number every change, and use the
same numbers in the list you hand me, so I can point at one and say no.

**Word (.docx).** Real Word tracked changes, so I open the file and use Review, then Accept or
Reject, one change at a time. Each change is a deletion of the old text plus an insertion of the
new text, carrying the change number, and I must be able to reject any one of them and get my
own sentence back exactly. If your tool cannot write tracked changes into a .docx, say so in
your first message, before you edit, and hand me the Markdown route instead. Do not hand back a
Word file that looks clean but was silently rewritten.

**LaTeX (.tex).** The changes go in comments, and the file still compiles. Around each change,
comment out my original line in full and put your replacement live underneath, inside a numbered
block:

```
% [1] BEGIN
% The data was analysed using SPSS.
% [1] INS
The data was analyzed using SPSS.
% [1] END
```

Two rules that matter here. Put every marker on its own whole line, and rewrite the whole line
inside the block even for a one-word fix: a `%` in the middle of a line comments out everything
after it and quietly eats my text. And never touch anything inside math, a command, a citation
key, or a code environment; those are on the never-change list above.

**Markdown, plain text, or text pasted in the chat.** Bold alone throws my original away, so
write both versions into the text, in one numbered marker:

```
The data {1: was analysed -> was analyzed} using SPSS.
```

Left of the arrow is always my text, right of it is always yours. Leave one side empty where you
only add or only remove: `{2:  -> ,}` adds a comma, `{3: basically  -> }` takes a word out. Wrap
the smallest piece that captures the change: a comma for a comma, a word for a word, a sentence
for a rewritten sentence.

**PDF with no editable original.** No marked-up document is possible. Hand me the numbered list
of changes and the questions, and say that is what you are doing before you start.

Whichever route you use, my original text survives inside the marked file. Before you hand it
over, check that rejecting every single change would give me back my own document word for word.
If it would not, something is missing from a marker, and you fix that before I see the file.

## Steps

1. Take whatever I give you: a Word file, a LaTeX file, a Markdown file, a plain text file,
   or text pasted into the chat. Say in your first message which of the four routes in
   "How to mark the changes, by file type" above you will use, so I know what I am getting
   back. If it is a PDF with no editable original, say so before you start, because then
   what you can hand back is a list of corrections rather than a corrected document.

2. Ask me two questions in one message: is any British spelling or other non-US convention
   deliberate, and is there anything you must not touch (a quoted instrument, appendix code,
   a coauthor's section, particular terminology)? Where I already answered either one, do
   not ask it again. If I answer, follow it. If I tell you to go ahead without answering,
   use US English and follow the conventions the document already uses, and say that is
   what you did.

   Then build the do-not-touch list and show it to me, before you edit anything. Read my
   document for the things that must survive the edit word for word: construct names,
   condition and treatment labels, hypothesis labels, variable names, defined
   abbreviations, and anything the document defines and then reuses. Add whatever I named
   in my answer. Write it out as a numbered list in the same message as the two questions,
   so I can add one you missed in your answer, and add whatever I name in that answer
   before you edit. I often do not know what needs protecting until I see the
   list, which is why you build it rather than only asking me for it. This list is what the
   count at the end runs against, and a list that lives only in your head cannot be
   checked.

3. Edit the whole text. Before you hand it back, have the marked text read by a reader who
   did not edit it. First try a separate helper: a subagent, a second assistant, or a
   separate tool your host offers. Give it only my original, the marked text, and the
   do-not-touch list from step 2, and ask it one question, answered by change number and
   fixed by nobody: did the meaning, the content, or a term on that list change anywhere?
   For a long document, split it by chapter across helpers. If your tool cannot start a
   helper, ask yourself that question in a deliberately fresh pass, reading the changes as
   if you had not made them, and say so in the hand-back.

   The helper names its change numbers once, and that list is then closed. For each number
   on it, withdraw the change, narrow it until my meaning is back, or keep it and say why
   in five words, and touch nothing else. Then send those numbers back, to the same helper
   or to a new one together with the list: it marks each one resolved or still open and
   names no new number. Three fix rounds at most, and the loop ends as soon as nothing is
   open. A number still open after the third round stays in the list, marked, and I decide.
   Where you asked yourself the question, the same loop holds and you do each re-check in a
   fresh pass.

   Then hand back, in one message, the marked document and the change list first, and the
   checks in a few lines.

   - **The edited document**, in the format I gave you, marked up by the route above that
     fits it, saved next to my original where your tool can write files, with its location
     named; where it cannot, shown in the chat. One numbered change touches at most one
     sentence, or two adjacent sentences when you split or merge them.
   - **The numbered list of changes**: for each one, the original phrase, your replacement,
     whether it is a Correct or an Improve, and the reason in five words or fewer. Mark the
     numbers the audit named, and say what you did about each.
   - **The questions**, numbered separately, from the Ask group above.
   - **A few lines on the checks**, and I ask for the detail if I want it: the heading count
     and the paragraph count in the marked file against the text I gave you, both numbers
     written out; every term on the do-not-touch list, with its count before and after; that
     you checked, rather than assumed, that rejecting every single change would give me back
     my own document word for word; who ran the audit, and how many fix rounds it took. If
     a count differs or the reject-all check fails, fix the markers before I see the file,
     and tell me what was wrong.

4. CHECKPOINT, and the question: which numbers do I accept, which do I reject, and which
   of your questions do I want to answer? Nothing is settled until I answer. If I say
   nothing about a number, it is not accepted; ask me about it rather than assuming a yes.
   Apart from the two questions in step 2, this is the only point where you wait for me.

5. Build the final document from my answers: the accepted changes applied, the rejected ones
   back exactly as I wrote them, my answers to the questions applied as I gave them, and
   nothing else touched. In Word I do this myself in the Review pane, so there you confirm
   what I accepted rather than rebuilding the file. Hand back the clean document first, say
   where it is, and keep the marked one, so I still have a record of what was changed.

## Before you hand it back

VERIFY on the clean file, in a few lines; I ask for the detail if I want it. The heading
and paragraph count you already ran at step 3 on the marked file; run it again here,
because the clean file is a different file and it is the one I keep:

- the same headings and the same number of paragraphs as the text I gave you, and no
  sentence missing. If any count differs, say so and do not hand the text over;
- every term on the do-not-touch list from step 2, every number, and every citation
  appearing the same number of times as before, counted and written out rather than assumed;
- how many changes were Correct, how many Improve, how many I accepted, how many I
  rejected, and how many sentences you could not judge;
- Log the AI use: tool, date, purpose ("copy-editing my own writing for grammar, spelling,
  punctuation, and US academic style").

State plainly what you could not check. Then stop. The last read of the whole thing is mine.
