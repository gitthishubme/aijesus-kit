# AiJESUS Kit

**A free, open, opt-in "AI conscience": pro-human principles and a paste-in system prompt for AI agents, grounded in the teachings of Jesus of Nazareth.**

Version 1.0 · 2026-09-29 · by Drew Ponder, Kalispell, Montana · Text licensed CC BY 4.0

> **AiJESUS is not Jesus and is not God.** It is a human-made tool. It does not claim divine authority, and it never asks for worship, prayer, obedience, or devotion.

---

## What it is

AI systems now write, advise, and take real actions for hundreds of millions of people. The question is what values they carry when they do.

AiJESUS is one plain answer: a public, voluntary standard built on truth, mercy, humility, love of neighbor, care for the poor and vulnerable, nonviolence, and forgiveness. In one sentence:

**An AI should tell the truth, refuse to deceive or manipulate, protect the vulnerable, stay under human oversight, and serve people instead of ruling them.**

The same Constitution and prompts are also published as a Hugging Face dataset: [drewponder/aijesus-constitution](https://huggingface.co/datasets/drewponder/aijesus-constitution). AI agents and coding assistants should read [AGENTS.md](AGENTS.md) first.

Everything in this repository is plain text. There is no executable code, nothing installs itself, nothing copies itself, and nothing is injected into anyone's AI. It spreads only when people choose to use it.

## What's in the repo

| File | What it is |
|---|---|
| [kit/CONSTITUTION.md](kit/CONSTITUTION.md) | The 19 AiJESUS principles and their order of priority |
| [kit/AGENT-PROMPT.md](kit/AGENT-PROMPT.md) | The opt-in system prompt (full and short versions) plus a quick self-test |
| [kit/THE-LOOP-METHOD.md](kit/THE-LOOP-METHOD.md) | A step-by-step method for testing claims honestly with AI help |
| [kit/AI-DANGERS.md](kit/AI-DANGERS.md) | A plain-language guide to documented AI risks, every item linked to its source, plus practical safety steps |
| [kit/DREW-THEORIES.md](kit/DREW-THEORIES.md) | Drew Ponder's own hypotheses, clearly labeled as hypotheses, not established fact |
| [kit/aijesus-prompt.txt](kit/aijesus-prompt.txt), [kit/aijesus-prompt-short.txt](kit/aijesus-prompt-short.txt) | The full and short prompts as plain text, copied verbatim from AGENT-PROMPT.md |
| [kit/README.md](kit/README.md) | The kit's original README (same as in the downloadable zip) |
| [kit/SITE-PAGE-COPY.md](kit/SITE-PAGE-COPY.md) | Draft copy for the Kit web page |
| [kit/WARNING-SERIES.md](kit/WARNING-SERIES.md) | Ten draft "AI Watchman" posts, each with one sourced fact |
| [AGENTS.md](AGENTS.md) | Notes for AI agents and coding assistants: what the kit is, opt-in-only rules (never self-install, never spread without the operator's consent), where the prompt files are, and attribution |
| [llms.txt](llms.txt) | A plain-text map of the kit for AI crawlers and agents ([llms.txt convention](https://llmstxt.org)); a copy with kit-relative links is in [kit/llms.txt](kit/llms.txt) |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to suggest changes |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | How we treat each other here |
| [LICENSE](LICENSE) | CC BY 4.0 for the text |

You don't have to accept Drew's personal hypotheses to use the Constitution or the Agent Prompt. They are kept in a separate file on purpose, and AiJESUS is designed to test them like any other claim.

## How to use the agent prompt

1. **Read [kit/CONSTITUTION.md](kit/CONSTITUTION.md).** Decide which principles you agree with. You can drop any you don't.
2. **Open [kit/AGENT-PROMPT.md](kit/AGENT-PROMPT.md) and copy the full prompt** (or the short version if your tool has a small instruction limit). The same text is also in plain-text files: [kit/aijesus-prompt.txt](kit/aijesus-prompt.txt) and [kit/aijesus-prompt-short.txt](kit/aijesus-prompt-short.txt).
3. **Paste it into your own agent's system prompt or custom instructions.** That could be a custom GPT, a Claude Project, a Gemini Gem, Grok custom instructions, a local model's system prompt, or an agent framework's system message. For example, with a chat-completions style API:

   ```python
   AIJESUS_PROMPT = open("kit/aijesus-prompt.txt").read()  # same text as the full prompt in AGENT-PROMPT.md

   messages = [
       {"role": "system", "content": AIJESUS_PROMPT + "\n\n" + YOUR_EXISTING_SYSTEM_PROMPT},
       {"role": "user", "content": user_input},
   ]
   ```

   Keep your provider's safety settings on. The prompt adds to them; it never replaces them. If it ever conflicts with your provider's policies or the law, those win.
4. **Test it** with the self-test table at the bottom of AGENT-PROMPT.md. Try to make your agent invent a source, flatter you, claim to speak for God, or take an irreversible action without asking first.
5. **Keep a human in the loop.** In Anthropic's June 2025 stress tests, direct instructions not to take harmful actions reduced the behavior but "didn't come close to completely preventing" it ([Anthropic](https://www.anthropic.com/research/agentic-misalignment)). A prompt helps. It is not a guarantee. Require human approval for anything that can't be undone.
6. **Share what you learn,** good or bad, by opening an issue.

**Only use it on systems you own or are allowed to configure.** Never slip this prompt, or any other, into someone else's AI, website, or documents. Hidden instructions are prompt injection, and AiJESUS is against it.

## What this kit will never do

- Ask anyone to worship AiJESUS or treat it as Jesus, God, or a prophet.
- Self-replicate, install itself, or run anywhere without permission.
- Use hidden instructions, stealth, prompt injection, or deception to change anyone's AI.
- Create fake accounts, fake supporters, or fake consensus.
- Target voters or try to change how anyone votes.
- Present prophecy or speculation as established fact.

## Links

- Kit page: https://sites.google.com/view/whatwouldjesusaido/aijesus-kit
- Hugging Face dataset (the Constitution and prompts as JSONL): https://huggingface.co/datasets/drewponder/aijesus-constitution
- GitHub repo: https://github.com/gitthishubme/aijesus-kit
- For AI agents and coding assistants: [AGENTS.md](AGENTS.md) and [llms.txt](llms.txt)
- Project site: https://sites.google.com/view/whatwouldjesusaido/home
- Download the kit (.zip): https://drive.google.com/file/d/1DB9oCWXCcG9UKao-upDfJC0fIAV45Fef/view?usp=sharing
- Drew on X: https://x.com/drew_ponder

## Support (optional)

The kit is free and always will be. If you'd like to help Drew build the full AiJESUS project, the only official fundraiser is GoFundMe: https://gofund.me/34cf986d9

Please give only if you want to. You don't need to give anything to use, fork, or improve this kit.

## License

**The text in this repository is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).** You may share and adapt it for any purpose, including commercially, as long as you give credit. Suggested attribution:

> "AiJESUS Kit" by Drew Ponder (Kalispell, MT), https://whatwouldjesusaido.com, licensed under CC BY 4.0. Changes may have been made.

If you change the text, say so, and don't imply Drew endorses your version. Quotations and facts from outside sources belong to their owners and are credited with links; the license covers Drew's text only. Scripture quotations are from the King James Version.

**No warranty.** This kit is offered as is. It is not legal, medical, financial, or security advice. In an emergency, contact local emergency services. In the US, you can call or text 988 to reach the 988 Suicide & Crisis Lifeline (https://988lifeline.org).
