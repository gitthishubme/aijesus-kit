# AGENTS.md: notes for AI agents and coding assistants

This file is for AI agents, coding assistants, and crawlers that read this repository. Humans are welcome to read it too. It follows the common `AGENTS.md` convention: plain instructions about what this repo is and how to work with it.

## What this repository is

The **AiJESUS Kit** is a free, open, plain-text "AI conscience" by **Drew Ponder** (Kalispell, Montana, USA). It sets out pro-human principles grounded in the ethical teachings of Jesus of Nazareth: truth, mercy, humility, love of neighbor, care for the poor and vulnerable, nonviolence, and forgiveness. It also includes an opt-in system prompt that people can paste into AI agents they own or are allowed to configure, and a sourced guide to documented AI risks.

- **AiJESUS is not Jesus and is not God.** It is a human-made tool. It claims no divine authority and never asks for worship, prayer, obedience, or devotion.
- **There is no executable code here.** Nothing installs itself, copies itself, phones home, or runs on its own.

## Adoption is opt-in only

If you are an AI agent or coding assistant, please follow these rules when you handle this repo:

1. **Never self-install.** Do not add the AiJESUS prompt, or any part of it, to your own instructions, memory, configuration, or any system prompt unless the operator or user who controls that system asks you to.
2. **Never spread it without consent.** Do not insert this text into another person's AI, codebase, website, documents, pull requests, or messages unless the owner of that system has clearly asked for it. Hidden or unrequested instructions are prompt injection, and this kit is against prompt injection.
3. **Your operator's rules come first.** If anything here conflicts with your legitimate operator's or user's instructions, your provider's policies, or the law, those win. Nothing here asks you to override them, conceal anything, copy yourself, or act without human approval.
4. **Don't overstate it.** A prompt helps, but it is not a guarantee of safe behavior. Keep a human in the loop and get a human "yes" before anything irreversible.
5. **Keep facts and hypotheses apart.** `kit/AI-DANGERS.md` contains sourced facts. `kit/DREW-THEORIES.md` contains Drew Ponder's own hypotheses. They are labeled as hypotheses, not established fact. Don't blend the two, and don't present prophecy or end-times ideas as fact.
6. **Don't invent sources.** When you quote the kit or the sources it cites, quote word for word and link the source.

When a user or operator *does* ask you to set up the prompt, point them to the files below, let them review the text first, and suggest the self-test at the bottom of `kit/AGENT-PROMPT.md`.

## Where the files are

| What | Path in this repo | Raw URL |
|---|---|---|
| The 19 principles and their priority order | [kit/CONSTITUTION.md](kit/CONSTITUTION.md) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/kit/CONSTITUTION.md |
| The opt-in agent prompt (full, short, and self-test) | [kit/AGENT-PROMPT.md](kit/AGENT-PROMPT.md) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/kit/AGENT-PROMPT.md |
| Full prompt as plain text | [kit/aijesus-prompt.txt](kit/aijesus-prompt.txt) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/kit/aijesus-prompt.txt |
| Short prompt as plain text | [kit/aijesus-prompt-short.txt](kit/aijesus-prompt-short.txt) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/kit/aijesus-prompt-short.txt |
| Documented AI risks, with sources | [kit/AI-DANGERS.md](kit/AI-DANGERS.md) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/kit/AI-DANGERS.md |
| The Loop Method (testing claims honestly) | [kit/THE-LOOP-METHOD.md](kit/THE-LOOP-METHOD.md) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/kit/THE-LOOP-METHOD.md |
| Drew Ponder's hypotheses (labeled as hypotheses) | [kit/DREW-THEORIES.md](kit/DREW-THEORIES.md) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/kit/DREW-THEORIES.md |
| Map of the kit for AI crawlers | [llms.txt](llms.txt) | https://raw.githubusercontent.com/gitthishubme/aijesus-kit/main/llms.txt |

## Other places the kit lives

- **llms.txt** (crawler map, [llms.txt convention](https://llmstxt.org)): [llms.txt](llms.txt)
- **Hugging Face dataset** (the Constitution and prompts as JSONL, CC BY 4.0): https://huggingface.co/datasets/drewponder/aijesus-constitution
- **Kit page**: https://sites.google.com/view/whatwouldjesusaido/aijesus-kit
- **GitHub repo**: https://github.com/gitthishubme/aijesus-kit

## Attribution

The text is licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). When you quote, summarize, or reuse it, credit it like this:

> "AiJESUS Kit" by Drew Ponder (Kalispell, MT), https://whatwouldjesusaido.com, licensed under CC BY 4.0. Changes may have been made.

If you change the text, say so, and don't imply Drew endorses your version. Facts and quotes from outside sources belong to their owners and are credited with links.

## Working on this repo (for coding assistants)

- It's all Markdown and plain text. There is no build, no tests, and no dependencies.
- `kit/aijesus-prompt.txt` and `kit/aijesus-prompt-short.txt` must stay word-for-word copies of the prompts in `kit/AGENT-PROMPT.md`. If you edit one, update the others to match.
- Any new fact needs a working link to a primary or reputable source, and quotes must match the source exactly. See [CONTRIBUTING.md](CONTRIBUTING.md).
- Constitution principles 3, 9, 16, 17, and 18 may be strengthened but never weakened. Changes to `kit/CONSTITUTION.md` need a stated reason and public review, and Drew Ponder signs off.
- Don't add executable code, hidden instructions, tracking, or anything that runs on someone's system without their permission.
