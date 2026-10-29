# own-the-why

Work fast with AI without disconnecting from the concepts you touch.

## Why

The risk is not that AI is smarter than you. It sounds like it knows everything, so its recommendation anchors you: your answer and your reasoning bend toward what it already said. Add the habit of skimming straight to the conclusion and approving it, and after a while the reasoning never passes through your head. You ship the work, but nothing sticks.

`own-the-why` puts a small piece of thinking back in your hands, only where it pays off. Everything else stays as fast as before.

## What it does

It applies in three moments only:

1. **A new concept** you have not worked with before.
2. **The root cause of a bug.**
3. **A design decision** with real options.

In those moments the agent:

1. **Asks for your hypothesis before its answer.** "Before I explain: what do you think happens to the second `false` when the step re-initializes?" Then it explains, starting from what you said.
2. **Asks for your choice and your reason before its recommendation.** The recommendation comes after, as a comparison: "I'd have picked B; your reason beats mine because…". "Sounds good" is not a reason.
3. **Explains concepts in prose.** A short paragraph with no bullets or bold key phrases, so it has to be read, not scanned.

It never applies to operational work: commits, statuses, commands, lookups. Every question is answerable in one line, at most one per message, and never a quiz. Say **"skip"** to answer normally for that moment.

## How it differs

- **Claude Code's built-in `Learning` output style** leaves `TODO(human)` spots for you to write code. `own-the-why` does not hand you code to write; it asks for your hypothesis and your reason before the AI's, so its answer does not anchor yours.
- **Socratic mentoring skills** (like [`mentoring-juniors`](https://github.com/github/awesome-copilot)) guide with questions and never give the answer. `own-the-why` always gives the answer, at full speed, and only pauses for one line in three moments.
- **Drill and quiz skills** (like `socratic-drill`) test you on a subject. `own-the-why` never quizzes: a question either produces a hypothesis or a decision.
- **Course-style skills** (like [`teach`](https://github.com/mattpocock/skills)) build lessons to learn a topic over several sessions. `own-the-why` runs inside your everyday work, not as a separate study session.

## Install

### Any agent (skills CLI)

```bash
npx skills add P4TTT0/own-the-why
```

Works with Claude Code, Cursor, Codex, Gemini CLI, GitHub Copilot and the other agents the [skills CLI](https://github.com/vercel-labs/skills) supports.

### Claude Code (plugin)

```bash
claude plugin marketplace add P4TTT0/own-the-why
claude plugin install own-the-why@own-the-why
```

### Codex (plugin)

```bash
codex plugin marketplace add P4TTT0/own-the-why --ref main
codex plugin add own-the-why@own-the-why
```

## Use

Type `/own-the-why` at the start of a session (`$own-the-why` in Codex). It stays on until you say "stop own-the-why".

To have it always on in Claude Code, import it from your `~/.claude/CLAUDE.md`:

```markdown
@~/.claude/skills/own-the-why/SKILL.md
```

## Works with output-style skills

It was built next to [`i-have-adhd`](https://github.com/ayghri/i-have-adhd), which shapes answers to be acted on fast. Both can be on at the same time: inside the three moments above, `own-the-why` wins; everywhere else, the output-style skill applies as usual.

## Contributing

If an installer does not work for your agent, or a mechanic feels miscalibrated (it slows you down more than it connects you to the work), open an issue.

## License

[MIT](LICENSE)
