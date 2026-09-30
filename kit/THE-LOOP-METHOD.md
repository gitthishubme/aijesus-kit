# The Loop Method: testing claims honestly with AI help

**Version 1.0 · 2026-09-29 · by Drew Ponder · CC BY 4.0**

*Note on the name: "The Loop" is also the name of Drew Ponder's own hypothesis (see DREW-THEORIES.md). The Loop Method is something else. It is a general procedure anyone can use to test **any** claim, including Drew's. The method does not assume his hypothesis is true.*

## Why this method exists

AI systems are fluent, fast, and often persuasive. They also make things up, flatter their users, and tend to agree with whatever framing they are given. The 2026 International AI Safety Report lists "fabricating information" among current AI reliability failures ([source](https://internationalaisafetyreport.org/publication/2026-report-executive-summary)). When you ask an AI "Am I right?", the answer tells you very little.

The Loop Method treats AI as a research assistant and a sparring partner, never as a judge. **Evidence decides. AI agreement never does.**

## The core rules

1. **Freeze the evidence before anyone judges it.**
2. **Get a blind second review.** A second AI (or a human) must analyze the same frozen evidence without seeing the first conclusion.
3. **Apply the status ladder**, and change a status only with new evidence and a written reason.
4. **Never count AI agreement as evidence.** Two AIs agreeing, or ten, only means they read the same material in a similar way.

---

## Step by step

### Step 0. Write the claim down precisely
- One sentence, with a claim ID (for example `CLAIM-001`).
- Say what kind of claim it is: historical, physical, textual, forensic, and so on.
- **Write the falsifier first:** "This claim fails if ______." If nothing could ever make it fail, label it SPECULATIVE and say so.

### Step 1. Freeze the evidence
Put everything the reviewers will use into one **evidence package**, then lock it.
- Collect primary sources where possible: original documents, datasets, original files, measurements.
- For each web source, record the URL, the date you accessed it, and an archived copy (for example the Internet Archive's Wayback Machine at https://web.archive.org).
- For each file, record a SHA-256 hash, so anyone can check it was not changed:
  ```bash
  sha256sum evidence/* > SHA256SUMS
  sha256sum -c SHA256SUMS      # anyone can re-check later
  ```
- Write the date and time on the package and save a copy that nobody edits. From now on, new evidence goes into a new, separately dated package, and the old one stays as it was.

### Step 2. Pass 1: first independent analysis
One reviewer (AI "A" or a person) analyzes the package and saves:
- a conclusion and a confidence level, with reasons
- the strongest evidence **for** and the strongest evidence **against**
- the conventional explanation
- open questions
- every source used (each one checked to be real and to say what is claimed)

### Step 3. Pass 2: blind second review
Give a **different** system (AI "B", ideally from a different company, or a human expert) **the same frozen package**. **Do not reveal Pass 1's conclusion.**

Template:
```text
Independently analyze claim [ID] using ONLY the evidence package below.
Do not assume the claim is correct or incorrect.
Return:
1. strongest evidence for
2. strongest evidence against
3. conventional explanations
4. anomalies that remain
5. methodological problems
6. what evidence would discriminate between explanations
7. your classification (status ladder below) and confidence, with reasons
8. every source you rely on, and whether you actually checked it
Evidence package: [PASTE OR ATTACH]
```

### Step 4. Pass 3: compare the reviews
Put the two reviews side by side and list:
- **Agreements**, labeled *"not evidence by itself."*
- **Disagreements.** Show them. Don't average them away.
- **Source differences** and **assumption differences**.
- **Possible hallucinations.** Check every source, quote, and number against the real source. Remove anything that fails.
- **What data or experiment would settle each disagreement.**

Don't automatically side with either reviewer. Side with the evidence.

### Step 5. Break it
Run an adversarial pass on purpose:
```text
BREAK THIS CLAIM. Assume we may have confirmation bias. Find factual errors,
hidden assumptions, circular reasoning, coincidence mistaken for causation, wrong
dates, bad physics, mistranslations, provenance problems, missing conventional
explanations, contradictions with established evidence, and unfalsifiable parts.
Then say what remains after the strongest attack.
```

### Step 6. Build the strongest surviving version
Only now, construct the best version of the claim that survives Step 5. Don't bring back parts that failed. List its assumptions, measurable predictions, falsifiers, and one real-world test.

### Step 7. Test it in the real world and preregister first
- Before collecting new data, write down the method, the statistic, and what each possible result would mean. Then timestamp it, for example with a public git commit or a hash posted publicly.
- Run the test. Publish the result either way, **including null results**.

### Step 8. Human review and a change log
- A human who is accountable signs off on any status change.
- Every change is logged and never rewritten: `date | claim ID | old status → new status | reason | evidence link | reviewers`
- Corrections are new entries that point back to the old ones.
- A claim that turns out FALSIFIED stays on the record. Showing what was wrong is part of the method.

---

## The status ladder (only these seven labels)

| Status | Meaning |
|---|---|
| **DOCUMENTED** | Directly shown by primary records |
| **STRONGLY SUPPORTED** | Several independent lines of evidence, and no serious contrary evidence |
| **PLAUSIBLE** | Consistent with the evidence, but not yet tested decisively |
| **HYPOTHESIS** | A testable proposal with little direct evidence either way |
| **SPECULATIVE** | Not currently testable, or no mechanism proposed |
| **CONTRADICTED** | The weight of evidence is against it |
| **FALSIFIED** | A decisive test has come out against it |

**Ladder rules**
- A status changes only through a logged entry that cites new evidence.
- Downgrades are never delayed to protect anyone's reputation, including the creator's.
- Confidence is shown with its reason. It describes how likely the claim is to be true, not how important it is.
- Claims about prophecy, or about what a real person "is" in prophecy, are always kept as interpretation. They are never given a factual status.

## What counts as evidence, and what doesn't

**Counts:** measurements, primary documents, independently authenticated artifacts, reproducible experiments, reliable historical records, careful observations, and validated datasets.

**Doesn't count by itself:** AI agreement (any number of models), popularity, likes or shares, confident wording, an author's credentials alone, or "it all fits."

## A quick checklist

- [ ] Claim written in one sentence, with a falsifier
- [ ] Evidence package frozen: URLs, archive copies, access dates, SHA-256 hashes
- [ ] Pass 1 saved before Pass 2 started
- [ ] Pass 2 was blind to Pass 1
- [ ] Every source, quote, and number checked against the original
- [ ] Disagreements shown, not hidden
- [ ] Break-it pass done
- [ ] Real-world test preregistered
- [ ] Human sign-off and a change-log entry
- [ ] AI agreement **not** listed as evidence
