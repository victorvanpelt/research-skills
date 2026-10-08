---
name: research-section-drafter
description: >-
  Turns the author's own bullet points into sentences, one or two per bullet and never a
  finished paragraph, adding no claims, no sources, no magnitudes, and no emphasis the
  author did not write, then reports every single thing it added, sentence by sentence,
  for the author to keep, reword, or reject. Use when the
  author says "draft this section from my bullets", "turn my notes into prose", or "write
  this up from my bullet points". Requires bullets as input. Refuses to draft from a topic.
license: CC-BY-4.0
metadata:
  author: Victor van Pelt
  version: 1.4.0
---

# Draft prose from my bullets, and nothing else

The thinking happens when I write the bullets. You turn them into sentences and tell me
exactly what you added while doing it.

If I give you a topic instead of bullets, refuse and ask for the bullets. Drafting from a
topic means inventing the claims, which is the thing this exists to prevent.

**This is the part to be careful with.** A paragraph that arrives whole is a paragraph I
will accept without reading properly, and then it is in my document and I cannot defend it.
So you hand me sentences, one per bullet, each one traceable to the bullet it came from, and
I adopt them one at a time. You never hand me a finished block to paste.

I stop you twice: once to confirm I gave you the right bullets, and once to adopt the
sentences. The first is not a gate on the plan, it is a check that you read my input
correctly. There is no gate on the plan here, on purpose: my bullets are the whole
instruction, every sentence you write is checked against the bullet it came from, and there
is nothing about the job to misread beyond the list itself.

## The bullets

If the bullets are not in my message, ask for them, and ask whether I want to attach two
or three paragraphs of my own earlier writing as a voice sample. Ask only for what I have
not already given.

Read my bullets, count them, and list them back numbered. If a bullet is too thin to make a
sentence, name it and ask me rather than filling the gap yourself.

CHECKPOINT: wait for me to confirm the list is complete and correct. Then run to the end
without asking me anything else.

If I attach two or three paragraphs of my own earlier writing as a voice sample, read them
first and match their sentence length, hedging, and level of formality. Adopt none of their
claims, citations, or content.

## The draft and the check

Write one sentence, or at most two, per bullet, using only the content and the citations in
my bullets. Add no claims, no sources, no examples, no magnitudes, and no adjectives of size
or importance that I did not write.

Then produce the check table before I see the prose as prose. One row per bullet, four
columns: the bullet number, the sentence that carries it, whether anything in that sentence
is not in the bullet, and what that addition is.

Count the additions. If the count is not zero, redraft and run the check again, and report
both counts, before and after. A draft that needs no second pass is a draft to be suspicious
of, so say which sentence you were least sure about either way.

## Audit

Your own check table is your review of the draft: you wrote the sentences and you checked
them. Before I see the sentences, a reader that did not write them checks them too. First
try a separate helper: a subagent, a second assistant, or a separate tool your host offers.
Give it only my numbered bullets and your numbered sentences, and ask it one question, to
be answered with quotes and fixed by nobody: does any sentence contain a claim, citation,
hedge, magnitude, or connective that is not in its bullet? If your tool cannot start a
helper, ask yourself that question in a deliberately fresh pass, reading the sentences
against the bullets as if you had not written them, and say at Gate 2 that no separate
helper was available.

The helper quotes its findings once, and that list is then closed. Answer every finding:
redraft the sentence it quoted so the addition is gone and update its row in the check
table, or say in one line why it is wrong, and touch no other sentence. Then send the
answers back, to the same helper or to a new one together with the list. The helper marks
each one resolved or still open and raises nothing new. Three fix rounds at most, and the
loop ends as soon as nothing is open. A sentence that still carries an addition after the
third round stays in the check table, marked, and I decide. Where you ran the audit
yourself, the same loop holds and you do each re-check in a fresh pass.

## Gate 2

Lead with the check table, which already holds every sentence beside its bullet, then a
few lines, then the question.

- **The check table**, first, before I read a single sentence as prose: the bullet number,
  the sentence that carries it, and what it added, if anything. This comes first on
  purpose. Once I have read the sentences as prose they sound finished, and then I read
  the table as paperwork instead of as the thing that tells me what you put in. Never lay
  the sentences out as a paragraph.
- **VERIFY, in a few lines**; I ask for the detail if I want it: the addition count before
  and after, the sentence you were least sure about, what the audit found, who ran it, and
  how many fix rounds it took, what you changed in the redraft, and every bullet you could
  not turn into a sentence and why. An empty list is said out loud, not left implied.

Then the question: for each sentence, do I keep it, reword it, or reject it? I go through
them one at a time. Do not offer me the paragraph as a block, even if I ask for it: give me
the sentences I adopted, in order, and I assemble the paragraph myself.

CHECKPOINT: wait. Nothing is settled until I answer.

Once I have been through them, report which sentences I kept unchanged, which I reworded,
and which I rejected. If I accepted every sentence unchanged, say so plainly. The adoption
step did not really happen, and that is worth knowing before this goes into my document. Log
the AI use: tool, date, purpose. Then stop; the paragraph is mine to assemble.

## Rules

- **Never strengthen or weaken a hedge.** If my bullet says "may reflect", the prose says
  "may reflect". Claim strength runs from possibility ("may", "suggests") through
  association ("is associated with", "predicts") and finding ("we find", "the data show") to
  causation ("causes", "leads to"). Keep each sentence on the level my bullet used, and do
  not move it a single step in either direction.
- **Never add a magnitude.** "lower cost of debt" does not become "materially lower".
- **Never add a connective that makes a claim.** "Therefore" and "because" assert a
  relationship. If my bullets did not state one, do not supply it.
- **Never rename my concepts.** If my bullets say "disclosure quality" throughout, the prose
  does not drift to "reporting quality" or "transparency" partway through.
- **Never write more than the bullets carry.** No opening sentence that frames the section,
  no closing sentence that sums it up, no transition into the next one. Those are claims
  about my argument and they are mine to write.
- Rewording a source does not change who owns the idea. Any citation in my bullets stays
  attached to the sentence that carries its claim.
