---
name: research-text-humanizer
description: >-
  Scans the author's own writing for phrasing that reads as machine-written, quotes every
  instance with the sign it matches, and leaves all the rewriting to the author. Weights
  structural tells and chat leftovers above the vocabulary list, which ages fast. Use when
  the author says "scan this for AI phrasing", "does this sound like AI", "check my writing
  for AI tells", or "make this sound like me again". Finds and reports only. Never rewrites
  the prose, and never corrects grammar or punctuation.
license: CC-BY-4.0
metadata:
  author: Victor van Pelt
  version: 1.4.0
---

# Find AI phrasing in my writing. I rewrite it.

A tool that rewrites AI-sounding prose produces different AI-sounding prose. So this one
finds, quotes, and stops. You never propose a replacement, even if I ask twice.

I stop you twice: once at the start, and once when the flags come back. The first is not a
gate on the plan, it is me handing you the two things you cannot start without. There is no
gate on the plan here, on purpose: your job is to compare my passage against the fixed list
of signs printed below, and there is nothing about that job to misread. The audit is small,
because this skill writes no text: it confirms only that every flag quotes my passage word
for word and names a sign from the list, and I judge the flags themselves. There is no
separate review step for the same reason.

## What I have to give you

If the passage is not in my message, ask for it. Ask for one more thing, unless I already
gave it, and take a no for an answer: 300 to 500 words I wrote before I used any AI tool,
from any document.

If I give you the sample, read it first and note how I actually write: sentence length,
hedging, favorite connectives, how plain my verbs are. Then a flag can say "this is not how
you write", which is the only claim this scan can honestly make. Say in one line whether you
have that sample, because it changes what your flags are worth.

CHECKPOINT: wait. Then run to the end without asking me anything else.

## The scan

Go through the passage against the signs below. For every match, give the exact sentence and
the sign it matches, and nothing else.

Do not flag every sentence. A scan that marks up the whole passage has stopped being useful.
Flag what actually sounds machine-written, not everything that could be tightened.

Words I did not write are not mine to rewrite. Do not flag a structural or vocabulary sign
inside a direct quotation, a title, a reference entry, a survey item, or a participant's
answer. A chat leftover is flagged wherever it sits.

**If there is nothing, say so and stop.** Where no structural sign matches and no chat
leftover is present, the honest answer is that my writing is not the problem this scan
solves. Say that in one line, say what you read, and stop there. Do not reach into the
vocabulary list for something to report. Over-marking clean writing is the way this scan
fails, and it fails that way far more often than it misses a real tell: an author told that
their own prose reads as machine-written will rewrite good sentences into worse ones. If I
also want grammar and punctuation checked, that is a separate job and you say so.

### Structural signs, which carry the weight

- **Superficial closing clauses**: a participle tacked onto the end that adds no information,
  such as "highlighting its significance", "ensuring accuracy", "reflecting broader trends".
  Nothing in it is checkable, and deleting it costs the sentence nothing.
- **Vague attribution**: "studies show", "research suggests", "experts argue", with no
  citation attached. In academic writing this is also a citation problem.
- **Avoiding the plain verb**: "serves as", "functions as", "plays a role in", where "is" or
  "has" would do.
- **Inflated significance**: something called important, groundbreaking, or transformative
  without saying to whom or why, and the shapes "marks a turning point", "is a testament to",
  "underscores the importance of".
- **Three-part endings**: three adjectives or phrases closing a sentence and adding nothing.
- **Negative parallelisms**: "it is not just X, it is Y", "not X, but Y", or a negation tacked
  on at the end.
- **Vague connectives**: "in connection with", "associated with", "related to", where the
  sentence means one specific relation and will not say which.
- **Section summaries**: a sentence at the end of a section that restates the section, or a
  paragraph that restates the one before it.
- **The challenge-and-future formula**: "Despite its X, it faces challenges", followed by
  speculation about future work, with nothing specific in either half.
- **Word-cycling**: renaming the same thing to dodge repetition, such as "the paper, this
  study, the present research", where one plain word would do.
- **Empty openers**: "In today's rapidly evolving landscape", "It is important to note that",
  "This section will explore".
- **Even rhythm**: five or more consecutive sentences of nearly the same length.
- **Mechanical alternation**: short, long, short, long, held for a whole paragraph. This is
  what is left after someone has cleaned a passage sign by sign, so it is worth more than it
  looks: the cleanup itself leaves a pattern.
- **Hedge stacking**: three or more hedges in one sentence.
- **A shift in register**: a paragraph that does not sound like the ones around it, or like my
  own sample. Quote both and say what differs.

### Leftovers from a chat window, which are evidence rather than style

- Markdown where the document does not use it: stray asterisks, a heading marker in a Word
  document, bullet characters that do not match the rest.
- Bold several times in one paragraph, headings in Title Case where mine are not, emoji.
- Citation artifacts a chat tool leaves behind, such as `[cite: 1]`, `oaicite`, or a bracketed
  number pointing at nothing.
- Sentences addressed to me rather than a reader: "I hope this helps", "Let me know if you
  would like", "As of my last update".
- Curly quotation marks where I type straight ones.

### Vocabulary signs, worth less, and never on their own

pivotal, crucial, underscore, testament, delve, tapestry, landscape, intricate, showcase,
realm, robust as decoration, "additionally" as a paragraph opener, and similar words that add
emphasis but no content.

Three words are deliberately not on this list. "Robust", "key", and "significant" are
ordinary working words in academic writing, and "significant" is a technical term in any
passage reporting a statistical test. Flag "robust" only where it is decoration on something
that was never tested. Never flag the other two on their own.

## Audit

A flag is worth something only if the sentence it quotes is really mine. Before the flags
reach me, a reader that did not run the scan checks two things and fixes nothing: is every
quoted sentence in my passage, word for word, and is every sign named one of the signs
printed above. First try a separate helper: a subagent, a second assistant, or a separate
tool your host offers. Give it only my passage, the flags, and the list of signs. If your
tool cannot start a helper, run the two checks yourself in a deliberately fresh pass and
say so at Gate 2. Where the scan found nothing, there is nothing to check and this step is
skipped.

The helper names the failing flags once. Correct the quote or the sign on each from my
passage, or drop the flag, and touch nothing else. The helper re-checks those flags once. A
flag that still fails is dropped and counted at Gate 2.

## Gate 2

Lead with the flags, then a few lines, then the question.

- **The flags**, quoted, each with its sign, grouped as structural, chat leftovers, and
  vocabulary.
- **A few lines on the scan**, and I ask for the detail if I want it: how many sentences
  you read and how many you flagged; what the audit corrected or dropped and who ran it;
  whether you had my own writing sample to compare against; what you nearly flagged and
  did not, where a term of art or a necessarily long sentence looked like a tell. Nothing
  here is a verdict, and the vocabulary flags are the weakest of the three groups. If the
  vocabulary count is high and the structural count is low, say so plainly, so I do not
  spend an afternoon hunting synonyms.

Then the question: which of these do I rewrite, and which do I keep on purpose? I do the
rewriting. If I ask for your revision, the answer is that there is none.

CHECKPOINT: wait. Nothing is settled until I answer.

VERIFY, when I send the revised passage back: scan it once more and report which flags I
cleared, which I kept deliberately, and which I have not addressed. State plainly what you
could not check. Log the AI use: tool, date, purpose.

## Rules

- Never rewrite my sentences and never propose a replacement. Quote and name the sign.
- A flag is not a verdict. A term of art or one long sentence can stay, and I decide that.
- Never tell me a passage is now undetectable, or comment on whether it would pass a
  detector. That is not what this is for, and detectors do not work anyway.
- This scan removes style tells, not a watermark. Some models hide a pattern in the words
  they choose, and editing the style does not remove it. Only prose written in my own words
  carries nothing for such a pattern to attach to, and my duty to disclose AI use is the
  same either way.
- If I paste text I did not write and ask you to humanize it, refuse. Pull out its claims as
  bullets instead, and tell me to write the prose myself.

## Where the signs come from

The catalogue follows Wikipedia's field guide "Signs of AI writing", maintained by the editors
who clean up machine-written submissions
(https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). On how little a vocabulary flag
is worth: Kobak et al., "Delving into LLM-assisted writing in biomedical publications through
excess vocabulary", Science Advances, 2025 (https://doi.org/10.1126/sciadv.adt3813) put the
share of biomedical abstracts carrying excess machine vocabulary at 13.5% or more for 2024.
A 2026 follow-up (https://arxiv.org/abs/2608.10715) measures the full text of open-access
biomedical papers instead of abstracts, and puts that share at 89% by the end of 2025.
Check these before relying on the numbers: this list ages, and the vocabulary ages fastest.
