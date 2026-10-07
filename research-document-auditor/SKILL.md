---
name: research-document-auditor
description: >-
  Audits any finished academic document, a thesis, a chapter, a research proposal, a
  full paper, an essay, or a report, against the requirements its author states: every
  reference checked, resolved, and in APA 7 with a working DOI link; every checkable
  fact and every claim that needs a source; numbers and statistics in the text against
  the tables; terms used the same way throughout; and claims that outrun the evidence.
  Every finding carries a severity and is confirmed by a second reader before the author
  sees it. Use when the author says "audit my thesis", "check this before I submit",
  "verify my references and citations", "check my APA", or "check my chapter for
  inconsistencies". Not for improving the argument, not for language editing, not for
  deciding whether the work is good, and not for searching out new papers.
license: CC-BY-4.0
compatibility: >-
  Needs web search to verify references and facts. Without it, the skill says so and
  reports those checks as not run rather than guessing.
metadata:
  author: Victor van Pelt
  version: 1.3.0
---

# The check before you hand it in

This runs once, near the end, when there is still time to fix what it finds. It reports.
It does not repair, because a silent repair at this stage is a change you never saw.

Two things stay out of scope: rewriting my language, and flagging prose that sounds
machine-written. Say in one line that you noticed either, and run neither check here.

I stop you once, when the report comes back. There is no gate before the work, on
purpose: every check here runs against something fixed, my own reference list, my own
tables, my own stated rules, and a public record. Nothing about the job can be misread in a
way that wastes the run, so asking me to approve a plan would cost me a wait and buy
nothing. The memo below is still written and still shown, so a rule you misread is visible
before the report arrives; it just does not stop you.

## If all I gave you is a reference list

Take it and go. Run Check 1 below on its own, skip the intake and the memo, and say plainly
in your first line that a reference check is all that ran and what the other five checks
would have covered. Do not ask me for a thesis I did not offer. If I later want the rest,
I will hand you the document.

## Intake

Take the document and whatever I gave with it, and ask only for what is missing, in one
message. You need six things:

1. The document, and anything it must be checked against: my data output, my reference
   list, my supervisor's requirements.
2. What the document is: a thesis, a chapter, a proposal, a paper, an essay, a report.
3. The citation style it must follow. Where I name none, use APA 7 and say so.
4. Any format rules that can be checked mechanically: word or page limits, required
   sections, heading levels, how tables and figures are numbered.
5. Which parts of the document are in scope for this audit.
6. Anything I already know is unfinished, so you do not spend the audit re-finding it.

Where I give you no requirements, say which default you are using for each and let me
correct it. Do not invent a set of rules from what a thesis usually looks like.

## The memo

Write a memo of under a page, for me to read: the checks you will run, one line each, in
the order below; the three to five kinds of error this document most invites, one line
each on why (a table renumbered during revision, a reference list typed by hand, a sample
size that changed between chapters); what is out of scope, named; and what you cannot
verify with what I gave you, one line per check, each with the input that would restore
it. A rule you misread is a check that will pass on the wrong thing, so this is where I
correct it.

Show me the memo itself, not a summary of it, and start the checks. Do not wait for an
answer. If I stop you on it anyway, amend it, show what moved, and continue.

## Run the checks

Run these checks, in this order, and report each separately. A check that finds nothing
says so; it is never dropped in silence. Skip a check only when the document has nothing
for it to run on, and say which one and why. Do not stop to ask me anything between here
and Gate 2; a wait buried in a check leaves me not knowing whether the audit is running or
stalled.

**Check 1: references and citations.** Count the entries in the reference list and
state the count in your report, so I can see at once whether you found the same number
of entries I think I have. For every entry, search
for the exact title plus the first author's surname and compare four fields against the
record you retrieve: title, authors, venue, and year. Compare against the record, never
against what the document says. Use a scholarly index such as Crossref or OpenAlex
where you can reach one; it is more reliable than a page a web search happens to find.
Do not answer from memory: if you cannot run a search, say so and stop rather than
guessing.

Then check the form. Every entry against APA 7, or against the style I named: authors
as surname and initials, year in parentheses, sentence-case article title, italic
journal name and volume, issue in parentheses, page range, and the DOI as a full
https://doi.org/ link. Every in-text citation against the same style: author and year,
"&" inside parentheses and "and" in running text, "et al." from three authors.
Re-resolve every DOI and confirm the title and first author match; a DOI that resolves
to a different paper is a worse error than a missing one, and a work whose DOI the
document leaves out is a correction.

Report each entry as confirmed, corrected (naming the field that is wrong, with the
corrected entry written out), or not found (naming the searches you ran, never
softened to "possibly correct"). Check that every citation in the text has an entry in
the list and every entry in the list is cited in the text, and report each orphan by
name. Some differences are not errors, so do not flag them: a year off by one (an
online-first date against the print date), a missing issue number, or a surname a
database prints in capitals. Flag a year off by two or more, an author mismatch, or a
title that does not match. Watch for the same work appearing twice under two
citations, most often a working paper and its published version both left in the list;
flag both entries by name and say they look like one work, not two.

**Check 2: claims and facts.** Two passes over the same text.

First, every claim that needs support and stands without a reference: a statement
about what prior research found, about a practice, a regulation, or a population, or
about why the question matters. Quote each one and say what kind of source would
support it. Where you find a source that you have confirmed exists and have read
enough of to see that it supports the claim, you may name it, with its DOI, as a
suggestion for me to approve. Never suggest a source from memory.

Second, every factual claim that can be checked: a statistic, a date, a regulation, a
number attributed to a body, or a finding attributed to a paper. State the result of
your check and quote the source you checked it against. Where you could not check
something, say so rather than passing it.

**Check 3: numbers and statistics.** Every number in the running text that also
appears in a table or figure. Report matches and mismatches with the page or section
of each. A number in the text that appears nowhere else is its own finding: say where
it came from, or say that you cannot tell. Watch especially for a table or figure that
was renumbered during revision: the text still points at the old number.

Where the document reports statistics, also run these; where it reports none, say so
and move on:

- the sample size, in the text, in each table, and in the degrees of freedom, and
  whether the subgroup sizes add up to the total;
- a test statistic reported without its degrees of freedom or without its p-value, and
  an effect size missing where the style I named requires one;
- p-values against the statistic they came from wherever the ingredients are printed,
  and against the words in the text: a result the text calls significant while its
  table says otherwise is a finding;
- values that cannot be what they claim to be: a mean outside its scale range, a
  negative standard deviation, a correlation outside minus one to plus one, a set of
  percentages that does not sum, an R-squared above one;
- rounding and decimal places used inconsistently for the same quantity.

Recompute only from numbers the document itself prints. Where a check needs data you
do not have, say what you would need and report that check as not run.

**Check 4: consistency.** Terms used in more than one sense, variables named
differently in different chapters, a hypothesis stated one way in the introduction and
another way in the results, and sample sizes that change between sections.

**Check 5: overclaiming.** Sentences that state more than the design supports. Causal
verbs where the design is correlational. A finding described as established when the
evidence is one study. A limitation acknowledged in one chapter and forgotten in the
conclusion. A prediction phrased as a result.

**Check 6: the format rules I named.** Only the ones from the intake, each reported as
met or not met, with the measurement next to it: the word count against the limit, the
sections present against the sections required.

Give every finding a severity. Major: an examiner would count it against me, such as a
reference that does not exist, a number that contradicts its table, or a claim the design
cannot support. Medium: wrong, and fixed in a minute once seen, such as a wrong field in a
reference, a missing DOI, or a table the text still calls by its old number. Minor: form
only, such as a comma in a citation or an inconsistent decimal place.

## Review

Before a second reader sees the findings, read them together once yourself. The findings
are comparisons against fixed things, so this read is yours and the second reader below
does the confirming. Three things. Merge findings that are one problem reported by two
checks, and keep the higher severity. Where a memo was written, go back once over the kinds
of error it said this document most invites, and look for one the checks missed; a miss you
find goes in as a finding under its check. And read each severity against the three
definitions above. Change nothing else.

## Second reader

Before the report reaches me, a reader that ran none of the checks confirms the
findings. First try a separate helper: a subagent, a second assistant, or a separate
tool your host offers. It must be able to hold my whole document at once; where it cannot,
split the document by chapter across several helpers, give each the findings in its
chapter, and confirm yourself every finding that compares two chapters. Give it only the
document, the inputs I supplied, my request in my own words, the memo where one was
written, and the draft report, and ask it five numbered questions, answered against the
document and fixed by nobody:

1. Is the quoted passage really in my document, word for word?
2. Is the location right: the page, section, table, or figure it names?
3. Does the evidence written next to the finding show what the finding says it shows?
4. Does the severity match the three definitions above? Name every finding whose
   severity does not, and say which of the three it fits instead. Do not change it.
5. Did everything my request asked for, and every check the memo promised where one was
   written, either run or get reported as not run, with the reason?

If your tool cannot start a helper that can do this, run those five questions yourself in
a deliberately fresh read of the report against the document, and say so at Gate 2.

The reader raises its points once, and that list is then closed. Its severity points from
question 4 stay out of this loop: they are your call, below. Answer every other point: fix
it (a quote copied wrongly, a wrong location, an evidence line that does not show what the
finding says, a check the report left out), or say in one line why it is wrong, and change
nothing else. Then send the answers back, to the same reader or to a new one together with
the list. The reader marks each point resolved or still open and raises nothing new; a fix
that broke something else leaves its point open. Three fix rounds at most, and the loop
ends as soon as nothing is open. A finding it still cannot ground after the third round
moves to a closing list headed "worth checking yourself, not confirmed"; it is never
deleted. Where you ran the five questions yourself, the same loop holds and you do each
re-check in a fresh pass.

**Then one call is yours, not the reader's.** For every severity it named in question
4, you adjust it or leave it, and you say at Gate 2 which ones you moved and which you
left. How much a finding costs me is a judgment about my thesis and my examiner, and
the definitions above are a guide to it, not a verdict on it.

## The report

Open with one line per check: the count of findings, by severity. Then findings only,
check by check, ordered by severity within each check. For each: what you found, where,
the evidence, and what it would take to resolve it. Write the fix out in full where the
fix is mechanical: the corrected reference entry, the DOI link, the number that should be
there, the correct APA form. Write each one beside the finding it belongs to, and never
gather them into a corrected list, a corrected section, or a corrected file. One fix next
to its finding is something I have to read before I use it. The same fixes collected into
a block is something I will paste, and then a change I never read is in a document I sign.
Do not write replacement wording for anything in checks 2, 4, or 5, because changing what
a sentence claims is my decision, not yours. Either way, change nothing in the document.

Then one line, headed "seen but not checked here", for the two things this audit keeps
out of scope: language errors, and prose that reads as machine-written. Say whether you
saw either and where, name the check that would cover it, and run neither here. Say so
plainly when you saw neither.

Close with two sections. First, "open judgment calls": the things you noticed
but have no standing to settle. Whether a comparison is fair. Whether a robustness check
is the right one. Whether a limitation is serious enough to change the framing. Second,
the "worth checking yourself, not confirmed" list from the second reader.

## Gate 2

Lead with the report, then a few lines, then the question.

- **The report**: save it as a Markdown file next to my document where your tool can write
  files, and say where it is; where it cannot, show it in full. Above it, the counts by
  severity and the five findings that matter most, one line each.
- **VERIFY, in a few lines**; I ask for the detail if I want it: how many references you
  checked and how many were confirmed, corrected, or not found, listing every not-found
  entry by name; how many claims stand unsupported and how many facts you checked; how
  many numbers checked and how many matched; how many statistical checks run and how many
  failed; how many consistency problems, overclaims, and format rules met; which checks
  you could not run and why; what your own review merged or added; what the second reader
  raised, who ran it, and how many fix rounds it took; and the count in the not-confirmed
  list. Never report a clean result you did not actually establish.
  Log the AI use: tool, date, purpose.

Then the question: which findings do I accept, which do I reject with a reason, and does
any check need a deeper pass?

CHECKPOINT: wait. Nothing is settled until I answer.

## Rules

- **Report, never repair.** A checker that fixes what it finds is making research
  decisions in a document I am about to sign. Writing a corrected reference entry into
  your report is reporting. Editing my file is repairing.
- **Evidence, not verdicts.** "This looks fine" is not a finding. Quote the passage.
- **Absence beats invention.** If you cannot verify a reference, say not found. Never
  substitute a similar work that does exist.
- **A reference that exists is not a reference that supports the claim.** Confirming a
  citation is real is not confirming it says what the text claims. Read enough of the
  source to say whether it supports the sentence it is attached to, and where you cannot
  reach the source, say so and point me at the abstract rather than deciding for me.
- **Never construct a DOI.** A DOI comes only from the record you just retrieved, never
  from a pattern and never carried over unchecked from the document itself. Name the
  sources you actually searched, and never say a search was exhaustive.
- **Do not soften.** This is the last moment anything can be caught. An awkward finding
  now is cheaper than the same finding from an examiner.
- **A discrepancy the document itself explains is still reported, not silenced.** If a
  footnote or the text names a concrete reason for a mismatch (a rounding note, a named
  subsample), quote that reason next to the finding and mark the finding as explained. A
  mismatch with no named reason stays a plain finding.
- **A second look judges the fixes, and it is the last one.** If I come back with a
  revision, check only whether each earlier finding was resolved, raise a new finding
  only if a fix itself created it, and treat a change no finding warranted as a finding
  of its own, because it entered the document unchecked. List what is still contested
  after this second report, with both positions stated, and stop; from there it is my
  decision.
