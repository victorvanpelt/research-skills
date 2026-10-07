# Changelog

Every skill folder carries its own version in the `metadata.version` field of its
`SKILL.md`. This file records what changed in each release, so a skill copied earlier
can be compared against the current one.

`research-defense-questions`, named in the 1.1.0 and 1.0.0 entries below, is no longer part
of this repository.

## 1.3.0, 2026-10-07

**All nine skills.** The work between the first stop and the last one now runs in one
order: plan, work, review, audit. A skill with no first stop or no review step says so.

- **A review comes before the audit.** A review asks whether the work is good. An audit
  checks it against fixed things. `research-proposal-drafter`, `research-document-reviewer`,
  and `research-feedback-reviser` send the review to a peer, a fresh session of the same
  model that did not see the work being made, and fall back to a fresh pass by the same
  assistant where the tool cannot start one. In the proposal drafter the judgment pass that
  used to follow the fact check is now this review and comes first. In the document reviewer
  the defender pass goes to the peer. The feedback reviser gets a review it did not have.
  `research-analysis-coder` and `research-document-auditor` get a short review by the
  assistant itself.
- **The audit loop is written out.** The helper raises its findings once. The assistant
  answers each one: it fixes it or says why it is wrong, and changes nothing else. The
  helper checks the answers and raises nothing new, three fix rounds at most. What is still
  open after that reaches you as open. Five skills did not state a loop before. Two run a
  shorter one and say why: the paper finder applies the auditor's result as it stands, and
  the text humanizer re-checks once.
- **In five skills the audit helper now gets what you asked for.** In the four skills that
  say back what they understood, it gets that read-back as you approved or corrected it. In
  the document auditor it gets your request in your own words and the memo. It can then
  check the result against what you asked for.
- **Questions first, then the read-back.** The proposal drafter, the document reviewer, and
  the feedback reviser now ask for what they are missing before they say back what they
  understood, so the read-back holds your answers.
- **A skill says what its helper must be able to do** where that is more than reading a
  short text: search the web, or hold your whole document at once, with a split by chapter
  where it cannot.
- **research-text-humanizer**: a small audit confirms that every flag quotes your passage
  word for word and names a sign from the list. A style sign inside a quotation, a title, a
  reference entry, or a survey item is not flagged; a chat leftover is flagged wherever it
  sits.
- **research-paper-finder**: a paper found by a follow-up search goes through the same
  check before it enters the list. A working paper and its published version are listed
  once, and a working paper is marked as not yet peer reviewed. A long journal list is
  searched in groups of about six names.
- **research-english-editor**: the helper gets the do-not-touch list, and a change it names
  is withdrawn, narrowed, or kept with a stated reason before you see the file. The helper's
  question now names how certain a claim sounds. No change sits inside another, a withdrawn
  change keeps its number, and an edited file from an earlier run is never overwritten.
- **research-feedback-reviser**: shows the numbered list of requests before it drafts.
  Under each draft it also lists what the draft took out that limited a claim. Comments
  that ask for the same change get one draft. The hand-over says how many words your
  document grows or shrinks by if you accept every draft.
- **research-document-auditor**: the second reader also checks that everything you asked
  for and every promised check ran or is reported as not run. The checks now also cover
  leftover placeholders and paragraphs pasted in twice, every pointer to a table, figure,
  section, appendix, equation, or hypothesis, and the numbers against your data output where
  you supply it. A recomputed value shows its arithmetic, a table read from PDF text is
  checked on the page before a mismatch is reported, and a corrected reference comes from
  one record. For a book, a report, a thesis, or a working paper it also searches the
  publisher's page and a library catalogue; one that is still not found stays not found,
  with a note that indexes often leave out such work.
- **research-proposal-drafter**: a template, a length limit, or something you ruled out now
  binds the draft, and the audit checks it. Two more audit checks: the proposal states no
  result you cannot have yet, and it agrees with itself (the summary, a number stated twice,
  every hypothesis label).
- **research-document-reviewer**: the step a comment asks for is one you can take with what
  you have. A comment never says what a source you cite found unless that source was opened.
  The defender drops a comment only where it can name the sentence in your document that
  answers it, and a quote the audit could not find is corrected or its comment is dropped.
  A second look at a revised document gives each earlier comment one verdict and writes no
  new set of main comments.
- **Four skills that save a file** (document auditor, document reviewer, feedback reviser,
  proposal drafter) never overwrite a file from an earlier run.

## 1.2.0, 2026-09-17

**research-proposal-drafter only.** The 1.1.0 rewrite removed the three-round loop but left
the skill without a plan step, so it went from three intake answers straight to a full draft
and its three comments dangled with nothing to attach to. Rebuilt on the shape its academic
counterpart uses:

- **Phase 1 now asks a fourth question**, because it changes everything downstream: is the
  data already in hand? No and a study will be run gives a future-tense design section ending
  in what will be fixed in advance. Yes gives predictions written knowing how they turned out
  and a short, clearly labeled preliminary finding with a line on what the design cannot
  claim. Neither gives a short honest design section and an offer to grow into one of the
  other two later.
- **Phase 2 is a plan**, written before a sentence of the proposal, shown and carried forward
  without waiting. Eight items: the research question, the contribution, the tension (the
  credible reason to expect the opposite result, written out), the design, the predictions in
  outline, what a null result still says, what it positions against, and what is out of
  scope. It closes with the calls that are the author's to overrule now rather than after a
  full draft exists.
- **Phase 3 positions the proposal** with the reference discipline stated in one place:
  never from memory, confirmed in Crossref, OpenAlex, or on the publisher's page, DOI copied
  from that record, unconfirmed flagged rather than cited.
- **Phase 4 drafts against the plan**, with the hypothesis format fixed and a rule for what to
  do when drafting shows the plan was wrong.
- **Phase 5 audits for fidelity, not design.** A choice the plan settled is not a finding. Five
  fact checks for a helper, including whether the proposal delivers what the plan promised, and
  a judgment pass that ends in a list the skill does not act on alone: causal verbs about its
  own study, concepts that could be measured otherwise, exploratory labels, and a source
  standing in for a better one. Closed ledger, three rounds at most.
- **Gate 2** leads with the proposal and the three ranked comments, then the four things, then
  the ship question, and says which comment to read first on five minutes.

## 1.1.0, 2026-09-17

**Where a skill stops changed.** Every skill used to stop once before the work, on a plan
it had already written. That stop is gone. Five skills now stop earlier instead, on what
they understood the request to be, before anything is planned or read:
`research-proposal-drafter`, `research-document-reviewer`, `research-feedback-reviser`,
`research-analysis-coder`, `research-defense-questions`. The other five have no stop before
the work at all, and each says why in one line: their work runs against something fixed
that already exists, so there is nothing about the job to misread.
`research-document-auditor`, `research-english-editor`, `research-paper-finder`,
`research-section-drafter`, `research-text-humanizer`. The stop at the end is unchanged in
all ten. Skills that asked for an input before starting still ask for it; that ask is not
a gate.

**research-proposal-drafter**: the three-round revision loop is gone, with its four stops.
The skill now takes one round of intake, then writes the draft, the references, and the
three ranked comments without stopping, audits, and hands everything over at once for you
to decide. Predictions got a standard: two or three, each stated so a result could
contradict it, each tied to something the design actually measures. Positioning references
got a pointer, three to six, stated as a recommendation the skill judges rather than a rule.

**research-feedback-reviser**: the mid-work stop is gone. The skill now drafts the smallest
change that meets each item itself, names a genuinely different alternative in one line
where one exists, and you decide once at the end with the drafts in front of you instead of
twice. Unclear items become a question for your supervisor; items waiting on data you do not
have become a task. Choosing how to meet a comment is the skill's job; judging whether the
comment is right stays yours.

**research-document-reviewer**: the minor-comment cap is now twenty rather than ten, as a
ceiling and not a target; over the cap the skill ranks by cost to the document and lists
what fell. A location is now strongly recommended rather than required: page numbers pulled
out of a PDF are unreliable, so where one cannot be confirmed the skill names the section,
table, or figure instead and says so.

**research-document-auditor**: a reference list pasted on its own now runs the reference
check alone, with no intake and no memo, and says what did not run.

**research-defense-questions**: a question your thesis cannot answer is no longer dropped.
It moves to a closing section of its own, outside the numbered list your answers are graded
against, because in a defense that is the question you most need to see coming.

**research-paper-finder**: asks for your supervisor's or department's journal list first,
and offers the FT50 as a named public starting point where you have none, saying what it is
and that it is one list among several. Added a check against the obvious miss: describe two
or three things the literature almost certainly contains and search for the descriptions,
never for a remembered title. The auditor's coverage note is now acted on rather than only
printed. `research-paper-auditor.md` moved to `research-paper-finder/references/`.

**research-text-humanizer**: added a clean exit, so a passage with no structural tell and no
chat leftover is reported as fine rather than mined for vocabulary flags. Added one tell,
mechanically alternating sentence lengths. Noted that "robust", "key" and "significant" are
ordinary words here and are not flagged alone.

**research-english-editor**: the skill now builds the do-not-touch list from your document
(construct names, condition labels, hypothesis labels, variable names, defined
abbreviations) plus whatever you named, shows it before editing, and counts against it at
the end.

## 1.0.1, 2026-09-08

- **research-english-editor**: `compatibility` added to the frontmatter. The skill needs a host
  that can write Word tracked changes into a .docx, and said so only in its body text, where a
  host program reading the frontmatter could not see it.
- **README**: the plain-text route no longer tells you to open a second chat and paste the work
  in. Every skill already handles a missing helper itself, by running the same check in a fresh
  pass and saying that is what it did. The README now says that, so the README and the ten
  skills give one answer instead of two.

## 1.0.0, 2026-09-08

First versioned release. All ten skills and the bundled `research-paper-auditor`.

Changed in this release:

- **research-document-reviewer**: the defender pass moved out of the helper and into the
  skill itself, as a deliberately separate pass, with four refutation questions and a kill
  log shown at Gate 2. Deciding whether a comment survives is a judgment, and a helper
  that kills a real concern removes the comment the author most needed.
- **research-document-auditor**: the second reader now answers four numbered questions and
  compares each severity against the three definitions the skill states, instead of judging
  whether a severity is fair. Adjusting a severity is the skill's call, reported at Gate 2.
- **research-proposal-drafter**: the audit split into two passes. A helper checks that the
  references resolve, that their form is right, that citations and list entries match, and
  that the checkable facts hold. Claim support, academic English, and AI slop moved to a
  separate pass by the skill, because judging how a draft reads is not a lookup. The helper
  no longer proposes replacement wording outside a corrected reference entry.
- **research-defense-questions**: the second reader reports an ungrounded question and
  changes nothing. The skill does the dropping and reports every drop at Gate 2.
- **Nine skills**: the second stop is now marked with CHECKPOINT, so both promised stops
  are labelled. research-english-editor is unchanged here: it designs one stop and says so.
- **Every skill**: `license` and `metadata.version` added to the frontmatter.
- **Repository**: LICENSE file added (CC BY 4.0).
