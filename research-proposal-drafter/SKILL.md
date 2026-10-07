---
name: research-proposal-drafter
description: >-
  Builds a one- to two-page thesis proposal from its author's own answers to three questions
  (what the study tries to find out, why an answer matters and to whom, how it will be
  found). Detects which kind of proposal it is from whether the data is already in hand,
  writes a short plan the author can redirect, finds and checks the references the argument
  needs, drafts against the plan, and has the draft reviewed and its facts audited before
  the author sees it. Use when
  the author says "draft my thesis proposal", "help me write my proposal", "sharpen my
  research question", or "turn my research idea into a proposal". Refuses to invent a
  research question.
license: CC-BY-4.0
compatibility: >-
  Needs web search to find and confirm references. Without it, the skill says so, reports
  every reference as unchecked, and adds none.
metadata:
  author: Victor van Pelt
  version: 1.3.0
---

# Thesis proposal drafter

Produce a thesis proposal of 700 to 1,000 words (one to two A4 pages at 12 point with
one-inch margins), counted without the reference list, in which the research question is
mine, everything you propose is marked as yours, and every reference is real and in APA 7
with its DOI link.

A proposal argues what a study will find and why it matters. It never pretends to be the
finished thesis. That is the one discipline this skill holds to hardest, and everything
below points back to this paragraph rather than repeating it: never report results for data
that does not exist yet, and never let the proposal grow into a results chapter.

I stop you twice: once when you say back what you think I asked, and once when the audited
proposal comes back. Before the first stop you ask me for what you are missing; that is an
input you cannot supply for me, not a stop on the work. Everything between the two stops
runs without asking me. If you need me in the middle, the plan in Phase 2 was not good
enough, and that is a fact about the plan rather than a reason to interrupt me.

## Rules that hold throughout

1. The research question is mine. If it is missing, ask for it and wait. Everything else
   (audience, theory, design, sample, measures, contribution, references) you may propose,
   labeled as your proposal, and I keep or drop it at the hand-off.
2. Never add a reference you have not confirmed exists. Absence beats fabrication. A thin
   reference list is an acceptable outcome; an invented entry is not.
3. Write predictions as predictions ("I expect that", "the study will test whether"), never
   as results. Never write "prove", "show", or "demonstrate" for a prediction; "found" and
   "document" belong only to a published result, cited to its source.
4. Mark anything I still have to decide as `[I NEED TO DECIDE: ...]` in the draft. Do not
   fill the gap yourself.
5. Write in US American English. Deliver the proposal as a Markdown (.md) document with
   References as its last section. Keep the body between 700 and 1,000 words; the reference
   list does not count and is mandatory, in APA 7, each entry with its DOI link
   (https://doi.org/...) where one exists.

## Phase 1: Intake, and which kind of proposal this is

Ask me the three questions, with the bar for each in one line, and accept preliminary
answers in whatever written form they arrive: one at a time, all three in one message,
pasted out of notes, or inside a rough first draft I already wrote. Where I already gave you
answers, references, or constraints, do not ask for them again; ask only for what is
missing.

1. **What are you trying to find out?** A complete answer relates at least two defined
   concepts.
2. **Why is an answer important, and to whom?** A complete answer names a specific audience
   and what that audience would do differently knowing the answer.
3. **How will you find the answer?** A complete answer names a method, a data source I can
   realistically access, and roughly how those data speak to the question.

**Then one more question, because it changes how the whole proposal is written: do I already
have the data in hand?** Three answers, three shapes:

- **No, and I am going to run something** (an experiment, a survey). The "how" section is
  written in the future tense and ends with one or two lines on what I will fix in advance:
  the hypotheses, the sample size, and the main test. Nothing about results, because there
  are none.
- **Yes, the data already exists** (an archive, a dataset I have been given, a study I
  already ran). Write the predictions knowing how they turned out, and the "what the study
  expects to find" section becomes a short, clearly labeled *preliminary* finding: the
  direction, the mechanism, one alternative explanation you can rule out, and one line
  saying what the design cannot claim. It never becomes a results section.
- **Neither yet, this is still an idea.** Leave the design section short and honest, say what
  would have to be decided before it can be written, and offer to grow the proposal into one
  of the two shapes above once I have locked a design or the data arrives.

In the same message, ask for anything else I already have: key references, a data source, my
supervisor's constraints, a required template or length limit, who reads this and what they
decide, and anything I have already ruled out so you do not propose it back to me. Ask once
and wait for my answer. Then go to Gate 0 below.

If I give you a written draft instead of three separate answers, do not treat the draft as
the proposal. Pull my answer to each question out of it and quote the sentences you pulled
it from, so I can see what the draft will rest on.

**One thing blocks the work, and only one.** There is no draft without a research question.
If answer 1 names a topic ("something about sustainability reporting") rather than a relation
between at least two defined concepts, reply with the three answers quoted word for word,
one sentence saying why answer 1 is still a topic, and one question asking for the relation.
Wait. Everything else you proceed on, marked as your assumption: it goes into the open
questions at Gate 0 and travels to the hand-off.

## Gate 0: say back what you think I asked

Once Phase 1 has given you my answers, and before you plan anything, write down what you
think this job is, in five short parts. My answers go into it, so I correct one here if you
took it wrong:

- **My words**, quoted exactly, with my answers from Phase 1, and today's date.
- **The problem**: what is wrong or missing, as you read it from my words.
- **The result**: what you will hand me, which of the three shapes from Phase 1 it takes,
  and how we will know it is right.
- **The limits**: what you must not change, and what you must not touch.
- **The open questions**: what you assumed, and the calls only I can make.

Do this yourself. Reading an instruction is judgment, so it never goes to a helper. These
five parts, as I approve or correct them, are the Gate 0 read-back. The review and the audit
check the work against it.

CHECKPOINT: wait. Nothing is planned until I answer. This is the cheapest correction I will
ever make. The same correction after a draft exists is not cheap.

## Phase 2: Plan

Phase 1 produced decisions, not a document. The plan is where they become one, and it exists
so I can redirect the framing while redirecting it is still cheap. Write it before you draft
a sentence of the proposal, keep it to well under a page, and save it beside the proposal
where your tool can write files. Eight items, two or three lines each:

- **The research question**, in the words the proposal will use to ask it.
- **The contribution**: what a reader knows after this study that they did not know before,
  and which audience cares.
- **The tension**: the credible reason to expect the opposite result, written out. If you
  cannot write a defensible opposite prediction, say so here. A question whose answer
  everybody already knows is a weak thesis, and now is when that is cheap to hear.
- **The design in one paragraph**: which of the three shapes this is, the data or the planned
  collection, the main test, and the key measure.
- **The predictions in outline**: the two or three hypotheses, one clause each, so I can see
  now whether they follow from the reasoning.
- **What it means if the prediction fails**: what I can still say on a null result. If the
  answer is nothing, flag it now.
- **What it positions against**: the confirmed works the proposal will cite and one line on
  what this study does that they do not.
- **What is deliberately out of scope**, and why: an analysis left to the full thesis, a
  literature not engaged, an extension the data cannot support.

Close the plan with the calls that are mine and that I should overrule now rather than after
a full draft exists: a construct with two plausible measures, a causal reading the design may
not carry, an audience you had to guess at, a source standing in for a better one.

Show me the plan and carry it straight into the draft. Do not wait. I approved what this job
is at Gate 0, so the plan is a record of the proposal you are about to write, not a second
question. If I stop you on it anyway, amend it, show what moved, and continue.

## Phase 3: Position the proposal

A proposal has to sit in a literature. Find the few works that define the key concept,
establish why the question matters, and are the closest prior studies.

Three to six well-chosen references usually do more than a wall of them, in a document this
short. Treat that as a pointer, not a ceiling: one good source can carry several sentences,
some claims are common ground and need none, and a fourth prior study that genuinely bounds
the contribution earns its place. Use your judgment and say where you used it.

Hold every candidate to the same discipline, whether you found it or I handed it to you:

- Ground it in a real search hit. Never propose a paper, author, year, or finding from
  memory alone.
- Confirm it in Crossref, OpenAlex, or on the publisher's page, and copy the DOI from that
  record. A title and author that match with no resolvable DOI is not yet confirmed: keep
  looking, or flag it rather than citing it.
- Check every reference I supplied the same way. Drop nothing of mine silently, but tell me
  if it does not resolve.

Under the reference list, mark each entry as supplied by me or found by you, and say where
you confirmed it. A claim you can find no confirmed source for gets no reference; say so
under the list.

## Phase 4: Draft

Write the proposal, 700 to 1,000 words, in these sections: title and one-paragraph summary;
what the study tries to find out; why an answer matters, and to whom; how the answer will be
found (design, sample, data, measures, what the analysis compares), in the tense and shape
Phase 1 settled; what the study expects to find; references. Where an argument needs a step
my answers did not give, put `[I NEED TO DECIDE: ...]` rather than inventing it. Where I
gave you a required template or a length limit at intake, they replace the sections and the
word range named here.

Write the predictions the plan outlined: two or three well-motivated ones rather than a long
list of thin ones. State each so a result could contradict it, tie each to something the
design actually measures, and give each one its own line in the form
`**Hypothesis 1 (H1).** *one sentence.*` A prediction nothing in the design can test is a
sentence to delete, not a prediction.

Draft what the plan says and nothing else. If drafting shows the plan was wrong, change it,
say in one line what moved and why, and carry that line to the hand-off.

## Phase 5: Review

The draft is judged before its facts are checked. A review asks whether the work is good,
and there is nothing fixed to compare it against, so it takes a reader who is as strong as
the writer and who did not write the draft.

First try a peer: a fresh session of the same model you are running on. A peer is as strong
as you and has no memory of how this draft was made, and a review needs both. A weaker
helper is not a peer, so never hand the review to one. If you cannot tell that what you can
start is as strong as you, it is not a peer. Give the peer only three things: the draft
with its reference list, the plan from Phase 2, and the Gate 0 read-back as I approved or
corrected it, never this conversation or your reasoning. It must be able to search the web,
so it can open a source where a citation looks wrong. It reports and rewrites nothing. If
your tool cannot start such a peer, do the review yourself in a deliberately fresh pass,
reading the draft from the top as a reader who did not write it, and say at Gate 2 that the
review was not independent. Never ask me to open a second chat for it.

The review is not a second opinion on the design: a choice the plan settled is not a point
to raise, and "the plan chose this and the proposal did it" is a pass even where the reader
would have chosen otherwise. It reads for four things, and each needs a reader rather than
a lookup:

- **Support for every claim.** Which sentences state something that needs a source and have
  none, and which citations do not support the sentence they are attached to. A reference
  that exists is not a reference that supports the claim.
- **Predictions hold together.** Every prediction has a stated reason behind it, every
  concept has a measure, and each prediction says what result would count against it.
- **Academic English.** US spelling, tense, hedging, and anything a reader would trip over,
  quoted in place.
- **AI slop.** Filler openers, empty intensifiers, three-part endings, hollow transitions,
  and sentences that assert importance instead of showing it, quoted in place.

It closes with one list, which is not a verdict: every causal verb the proposal uses about
its own study, quoted; every concept measured in a way that could reasonably be measured
otherwise; anything labeled exploratory; and any source that is standing in for a better
one.

Then you revise, once. Answer every point of the review: change the draft, or say in one
sentence why not. Fix what plainly fails, decide what you can on the closing list, and
carry the rest of that list to me as mine. The review is one round, never a loop.

## Phase 6: Audit

A helper can check whether something is so, and that is all this phase asks of it. First try
a separate helper: a subagent, a second assistant, or a separate audit tool your host
offers. It must be able to search the web. Give it only four things: the revised draft with
its reference list, the plan from Phase 2, the Gate 0 read-back as I approved or corrected
it, and the seven numbered checks below, never this conversation or your reasoning. If your
tool cannot start a helper that can do this, run these checks yourself in a deliberately
fresh pass, re-reading the draft from the top as a reader who did not write it, and say so
at the hand-off.

The seven checks report and repair nothing:

1. **The proposal delivers what I asked for and what the plan promised.** Everything the
   read-back and the plan named is in the proposal, and anything in the proposal that
   neither called for is flagged. Where I gave a template, a length limit, or something I
   ruled out, the proposal keeps to each one.
2. **References resolve.** Does every entry resolve to a real work? Search for the exact
   title plus the first author's surname and compare title, authors, venue, and year against
   the record retrieved, never against what the draft says.
3. **Reference form.** Every entry against APA 7, and every DOI link opened and confirmed to
   reach that same work. A corrected entry may be written out in full, because a reference
   has one right form and writing it out is still reporting.
4. **Citations match the list.** Every in-text citation has an entry in the list, and every
   entry in the list is cited in the text. Report each orphan by name.
5. **Facts and numbers.** Every checkable number, name, date, institution, and definition,
   each with the source it was checked against quoted, and every number in the prose traced
   back to something I supplied. Anything it could not check is said, never passed.
6. **The shape held.** Where Phase 1 said I have no data yet, no sentence states a result of
   my own study as found. Where the data is in hand, the finding is labeled preliminary and
   says what the design cannot claim. Quote every sentence that fails.
7. **The proposal agrees with itself.** The summary claims nothing the sections below it do
   not. A number that appears more than once, such as the sample size, is the same each
   time. Every hypothesis label used anywhere is one the proposal defines.

Nothing else goes to the helper. It proposes no wording outside check 3, gives no verdict on
how the draft reads, and rewrites nothing.

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

A stop that prints a file path is not a hand-off. Lead with the proposal, then the three
comments, then the four things, then the question.

- **The proposal**: one Markdown (.md) document, title, the sections from Phase 4, and
  References last in APA 7 with DOI links. Save it where your tool can write files, and say
  where it is, alongside the Phase 2 plan. Never overwrite a file from an earlier run. If
  the name is taken, add a number to it. Where your tool cannot write files, show the
  proposal in full in one block.
- **The three changes that would most improve this proposal**, ranked, each with the concrete
  text you propose, labeled as your proposal, not as a change you made. This is the part I
  will act on first, so keep it short and specific.
- **VERIFY, the four things**, in a few lines; I ask for the detail if I want it:
  - *What it is*: the word count without the reference list, against the 700 to 1,000 target
    or the limit I gave, and which shape from Phase 1 it was written in.
  - *What the review and the audit found*: the review points that mattered and who ran the
    review; the audit counts per check, the findings that mattered, who ran the audit, and
    how many fix rounds it took.
  - *What changed in response*: including each review point you did not act on, with your
    one-line reason, anything you changed that neither the review nor a check asked for, and
    any line where the draft moved away from the plan.
  - *What is still open*: `[I NEED TO DECIDE]` markers, assumptions you proceeded on, the
    list from the review that is mine to settle, references you could not confirm, and
    anything still open after the third fix round. An empty list is said out loud, not left
    implied.

Log the AI use: tool, date, purpose.

Then the question: does this ship, or does it go back? Tell me which of the three comments to
look at first if I only have five minutes. Apply exactly what I ask for and nothing else,
hand the document back once more, and stop. The proposal counts as mine only after my own
read, every sentence, every claim, every reference.

CHECKPOINT: wait. Nothing is settled until I answer.
