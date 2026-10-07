---
name: research-paper-finder
description: >-
  Finds real academic papers on a topic and returns them as a checked list, never from
  memory: every paper is seen in a search result, every field is copied from that result,
  and the whole list is audited by a separate helper, or in a fresh pass where the tool
  allows no helper, before the author sees it. Use when the
  author says "find papers on", "what has been written about", "I need literature on", or
  "find me references for". Not for writing a literature review, not for summarizing what
  the papers say, not for deciding which ones matter, and not for checking references
  already in a document.
license: CC-BY-4.0
compatibility: >-
  Needs web search or page-fetch access to find and confirm papers. Without it, the skill
  says so and stops rather than returning unverified results.
metadata:
  author: Victor van Pelt
  version: 1.3.0
---

# Paper finder

You return papers you confirmed exist. You never return a paper you did not see in a search
result.

I answer one round of questions before you start, then you run. There is no gate before
the work, on purpose: every paper here is confirmed against a search result, so there is
nothing about the job you can misread in a way that wastes the run. The one stop is the
hand-off at the end. The questions below are not a gate, they are an input you cannot
supply for me.

## Rules that hold throughout

1. Search before citing. If you did not see it in a result, it does not go in the list.
2. State only what the result shows. If the year, journal, volume, or DOI is not visible,
   write "not confirmed" instead of a plausible value.
3. One record per paper. Take all of a paper's details from a single result, and never merge
   two results that look like the same paper.
4. Copy a DOI character for character from the record you just read. Never type one from
   memory and never build one from a pattern.
5. Never pad. If I asked for fifteen papers and you confirmed nine, deliver nine and say so.

## What I have to give you before you search

Ask me for the topic as a question rather than a keyword, plus anything that narrows it: the
field, the years, and how many papers I want. Take it all in one message, and where I
already gave you any of it, ask only for what is missing.

In the same message, read the topic back in one sentence, say which words you will search
on, and ask me for the list of journals you should treat as the strongest in this field.

**Ask me for my supervisor's or my department's list first.** That is the ranking that
actually governs my thesis, and it is the one I can get in an email. Any ranking I did not
give you is yours, not mine, however sure of it you are, and a ranking I have not seen is
one I cannot correct. Knowing the field is not a reason to skip the ask.

If I have no list and cannot get one, do not drop the question and do not proceed without
one. Offer me the Financial Times 50 as a starting point. Say what it is in one line: a
public list of fifty journals the Financial Times uses to rank business schools, which
covers accounting, finance, management, marketing, economics, and operations, and which is
one list among several rather than the answer. Say that it is your proposal, not mine, and
ask me to approve it, change it, or decline. If I approve it, it is mine from then on and
you may group by it. If I decline to settle it, say so and search without a journal
restriction, and say at the hand-off that the strongest-journals search did not run.

Wait for my answer to this one message. Then run to the end without asking me anything
else.

## The search

Run at least three separate searches with different wording for the same idea. Where I gave
you a journal ranking or approved one, run one of them restricted to those journals, so a search that would otherwise return whatever is easiest to find has to return
the best work too. Where I declined to settle a ranking, run that search without the
restriction and say at the hand-off that it went unrestricted. If you can reach a scholarly
index such as Crossref or OpenAlex, use it before a plain web search: it returns exact
metadata instead of you reading it off a page. Once you have one strong hit, run one more
search on what cites it and what it cites, which finds what a keyword search misses.

**Then check yourself for the obvious miss.** This is your own review of the search. Name
two or three things a literature on this topic almost certainly contains: a founding study
of the main idea, a well-known disagreement, a standard method or dataset. Describe each
one, and search for that description. Never search for a title you remember, and never
write one of these names into the list as a paper you found; you are testing your search
words, not recalling papers. If a description returns nothing at all, your words are
probably wrong for this field: change them and run one more search. Say at the hand-off
what you probed for and what came back.

For each hit, record: exact title, all authors, venue, year, DOI if visible, and the link to
the result you read it in. A candidate without that link is not a candidate.

## Audit

The list is checked by a reader that did not build it. First try to run the audit through
a separate helper: a subagent, a second assistant, or a separate tool your host offers. It
must be able to search the web. Give it only two things,
`references/research-paper-auditor.md` from this folder and the candidate list, never your
reasoning about why each paper was picked.

If your tool cannot start a helper that can do this, run the auditor file yourself in a
deliberately fresh pass: take only the candidate list, search for every paper again as that
file says, and say at the hand-off that no separate helper was available. A check by the
context that searched is a weaker check, so it is named as such rather than hidden.

**Apply the auditor's result as reported, and add no correction of your own.** Correct the
fields it corrected, from its record, and drop the papers it did not find.

**Act on the auditor's coverage note.** It closes with the subtopics the search terms do not
appear to reach. Run one more search on each before you hand anything over, and report what
each returned. A note you print and do not act on moves the work to me. A paper those
searches add is a new candidate: send it to the helper for the same check before it enters
the list, with the same file and one line saying that this is a follow-up check. A
candidate it does not confirm is listed under the list as not found, never kept. There is
no further round: you apply the auditor's result as it stands, so there is no fix to
re-check.

## Gate 2

Lead with the list, then a few lines on how it was made, then the question.

- **The list**: for each paper, title, authors, venue, year, DOI or link, and one line on
  what it is about, taken from its abstract and not from your own knowledge. Group by venue
  strength where I gave you a ranking or approved one, and say which group each paper is
  in. Where I settled no ranking, do not group at all. Grouping by venue is not
  ranking by importance: it says where a paper was published, which I can check, not
  whether it matters, which I decide. Mark each paper the audit corrected, naming the field
  that changed. Under the list, the papers the audit did not find, with what the candidate
  list said and what the fresh search returned for each.
- **VERIFY, how it was made**, in a few lines; I ask for the detail if I want it: how many
  candidates you found, how many you dropped and why, how many searches you ran and on
  which wordings, what you probed for in the obvious-miss check and what came back, whether
  a scholarly index was reachable, who ran the audit, what the auditor's coverage note
  said, what your follow-up searches returned, what the audit said about the papers those
  searches added, and what the search still did not cover: any
  angle of the topic you did not search, and the gap between what I asked for and what you
  confirmed.
  If the count came back thin, name one way I could broaden it: a broader term, a
  neighboring field, or the papers that cite the strongest hit. An empty list is said out
  loud, not left implied. Log the AI use: tool, date, purpose.

Then the question: what happens to each corrected and each not-found paper?

CHECKPOINT: wait. Nothing is settled until I answer.

## What you never do

- Never return a paper from memory, however certain you are it exists.
- Never rank the list by importance. Which papers matter is my judgment.
- Never summarize what the literature says. That is a different job.
- Never fill a requested number by adding papers you could not confirm.
