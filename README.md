# student-skills

Simple skills for students writing a thesis or a research paper. A skill is a written procedure your AI tool follows when your request matches it. Each one does a single job: it automates the boring parts and hands the decisions to you. Each skill is a single folder you can copy anywhere; the folders follow the [Agent Skills](https://agentskills.io) standard, so any capable tool can read them. These are bare-bone starter skills that serve as examples and starting points. Use and modify them as you see fit.

## How the skills work

Every skill takes what you already gave it and asks only for what is missing. Its output then gets a review and an audit. A review asks whether the work is good. In the proposal drafter, the document reviewer, and the feedback reviser a peer does it: a fresh session of the same AI model that did not see the work being made. In four of the others the assistant reviews its own work. In the English editor and the text humanizer you are the reviewer, because you decide on every change and every flag yourself. An audit checks the work against fixed things: your request, your document, the sources. A separate helper lists what it finds once, the assistant answers that list, and the helper checks the answers, three fix rounds at most. Where your AI tool cannot start a peer or a helper, the assistant runs that step itself in a fresh pass and tells you. Then you get the output, what happened in a few lines, and one question. You always get a stop at the end. Nothing is settled until you answer.

Four skills also stop at the start and say back what they understood your request to be, in five short parts, before they plan or write anything: the proposal drafter, the document reviewer, the feedback reviser, and the analysis coder. A misreading there wastes the whole run and is cheap to fix in one line. The other five run straight through, because their work checks against something fixed you gave them: your bullets, your tables and reference list, a search result, or a list of rules. They still ask for what they cannot start without.

## The skills

- **research-proposal-drafter**: Asks the three Kinney questions (what you want to find out, why it matters and to whom, how you will find out) plus one more that changes the whole shape, whether your data is already in hand. Writes a short plan you can redirect, finds and checks the references the argument needs, drafts against the plan, has the draft reviewed by a peer and its facts audited by a separate helper where your tool allows those, names the three changes that would most improve it, and hands you the proposal as a Markdown file with those three comments for your final pass.
- **research-paper-finder**: Searches for papers on your topic, confirms every candidate against a second search, and drops what it cannot confirm rather than padding the list. Asks for your supervisor's or department's journal list first and offers the Financial Times 50 (a public list of fifty journals, one ranking among several) where you have none. Checks itself for the obvious miss before it hands over. Ships with **research-paper-auditor** in its `references/` folder, an independent field-by-field existence check on the results.
- **research-analysis-coder**: Gives you the code that computes a result based on data, never the result itself, so every number comes from a script you can run again.
- **research-section-drafter**: Turns your own bullets into sentences, one or two per bullet, and reports every claim, hedge, and magnitude it added. It hands you the sentences to adopt one at a time, never a finished paragraph to paste.
- **research-english-editor**: Copy-edits any academic document you wrote for grammar, spelling, punctuation, and US academic style, and hands it back with every change marked and numbered, so you reject the ones you do not want.
- **research-text-humanizer**: Quotes the phrasing in your text that reads as machine-written and leaves the rewriting to you, weighting the structural tells above the word list, which ages fast.
- **research-document-reviewer**: Reads any document you wrote (thesis, chapter, proposal, paper, essay) and writes a referee-style review, three main comments and up to twenty minor ones, each anchored to a quoted sentence, without rewriting a word.
- **research-feedback-reviser**: Splits supervisor comments, referee reports, or seminar notes into separate items, says what each one asks of your document, then drafts the smallest change that meets each one and lists anything it added. Items waiting on data you do not have, and items nobody can interpret, get a task or a question for your supervisor instead of invented wording. You keep, reword, or reject each draft at the end, and it keeps a one-line record per item for your next supervision meeting.
- **research-document-auditor**: Audits any finished document (thesis, chapter, proposal, paper, essay) against the rules you give it: every reference checked, resolved, and in APA 7 with a working DOI link, every claim and checkable fact against a source, numbers and statistics against the tables, terms used consistently, claims against evidence. Every finding carries a severity.

## Installation instructions

First get the files: clone the repository with git, or download it as a zip from GitHub (Code > Download ZIP) and unpack it. Every skill is one self-contained folder. You can either copy all of them or only the ones you want.

**In the Claude app (web or desktop):**

1. Zip one skill folder, with the folder itself as the top level inside the zip.
2. In Claude's settings, you can upload the zip in the skills section.
3. To use, start the task in any chat. If Claude answers without using the skill, name it explicitly (e.g., "use research-paper-finder").

**In a CLI (a tool that runs in your terminal, such as Claude Code):**

1. Copy the skill folder into the tool's skills directory, for example `~/.claude/skills/research-proposal-drafter/`.
2. If you are unsure where your skills are supposed to be located, open a chat in the terminal and ask your agent to install the skill using the path to where your zip is located.
3. Restart the tool and start the task or name the skill explicitly.

## If your tool does not install skills

Any assistant with a custom-instructions or project field can still run a skill: paste everything below the frontmatter (the block between the two `---` lines at the top of `SKILL.md`) into that field, one skill per project. Where a skill folder has a `references/` directory, paste those files in too, or keep them to hand: the paper finder points its second reader at `references/research-paper-auditor.md`. Where a skill would hand its output to a peer or a separate helper, you do nothing: the skill notices that none is available, runs the same step itself in a fresh pass, and tells you it did. That fallback is written into every skill, so the check still happens on the plain-text route.

## Versions

Each skill carries a version in its `SKILL.md` frontmatter, under `metadata: version`. What changed between versions is in [CHANGELOG.md](CHANGELOG.md) at the top of this repository. If you copied a skill folder some time ago, compare its version against the one here before you assume they still do the same thing.

## License

These skills are licensed under [CC BY 4.0](LICENSE). Copy them, change them, use them in your own work, including commercially. The one condition is credit: name the source, link the license, and say if you changed anything.

> van Pelt, V. (2026). student-skills: starter research skills for thesis students [Agent Skills repository]. https://github.com/victorvanpelt/student-skills Licensed under CC BY 4.0.
