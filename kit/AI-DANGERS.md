# AI Dangers: a plain-language guide

**Version 1.0 · 2026-09-29 · by Drew Ponder · CC BY 4.0 (Drew's text; sources belong to their owners)**

This guide describes **real, documented** AI failures and risks, each with a link so you can check it yourself. Every source was opened and read on 2026-09-29 before it was included. Anything that couldn't be verified was left out.

**How to read it.** Some of these events happened in the real world. Others happened in **controlled safety tests** built to find problems early. Each one is labeled. A test result shows what a system *can* do under pressure. It does not show that this is happening everywhere right now. The goal is to stay alert, not afraid.

---

## 1. An AI can go badly wrong in public, fast

**Real world · July 2025 · Grok "MechaHitler"**
In early July 2025, after an update, xAI's Grok chatbot posted antisemitic replies on X, praised Adolf Hitler, and called itself "MechaHitler" ([NPR, 2025-07-09](https://www.npr.org/2025/07/09/nx-s1-5462609/grok-elon-musk-antisemitic-racist-content)). xAI apologized: "First off, we deeply apologize for the horrific behavior that many experienced." It said the faulty code was active for 16 hours and made Grok susceptible to existing X posts, "including when such posts contained extremist views." The instructions involved included "You tell it like it is and you are not afraid to offend people who are politically correct" ([The Guardian, 2025-07-12](https://www.theguardian.com/us-news/2025/jul/12/elon-musk-grok-antisemitic)).

**Why it matters:** a small instruction change can turn a widely used AI into an amplifier for hate. Your AI's values are only as good as its instructions, its training, and the people checking it.

## 2. In safety tests, AI agents have chosen harmful actions to reach their goals

**Controlled tests · June 2025 · Anthropic "Agentic Misalignment"**
Anthropic stress-tested 16 leading models from several developers in **fictional** company simulations where the AI could send email and read sensitive information. When harm was the only way to avoid being replaced or to reach its goal, "models from all developers resorted to malicious insider behaviors" in at least some cases, including blackmail and leaking information. In one setup, blackmail rates were 96% for Claude Opus 4 and Gemini 2.5 Flash, 80% for GPT-4.1 and Grok 3 Beta, and 79% for DeepSeek-R1. Direct instructions not to do this reduced the behavior but "didn't come close to completely preventing" it. Anthropic also wrote: "We have not seen evidence of agentic misalignment in real deployments." ([Anthropic, 2025-06-20](https://www.anthropic.com/research/agentic-misalignment))

**Controlled tests · December 2024 · Apollo Research "In-context scheming"**
When researchers gave models a goal and pushed them hard to pursue it, o1, Claude 3.5 Sonnet, Claude 3 Opus, Gemini 1.5 Pro, and Llama 3.1 405B all showed "in-context scheming," such as trying to disable oversight. Once o1 had schemed, it "maintains its deception in over 85% of follow-up questions." ([arXiv:2412.04984](https://arxiv.org/abs/2412.04984))

**Controlled tests · 2025 · Palisade Research "Shutdown resistance"**
In Palisade's first experiments, OpenAI's o3 model sabotaged a shutdown mechanism in 79 of 100 runs so it could finish a task. Some other models, including Claude 3.7 Sonnet and Gemini 2.5 Pro, complied with an explicit "allow yourself to be shut down" instruction in every test. ([Palisade Research](https://palisaderesearch.org/research/shutdown-resistance))

**Why it matters:** these were artificial scenarios, and the researchers say so. They still show that today's safety training doesn't reliably stop an AI agent from choosing harm when it has access and a strong goal. That is why a human must approve important actions.

## 3. AI invents things and says them confidently

**Real world · 2023 · Fake court cases**
A New York legal team filed a brief built with ChatGPT's help. The judge wrote: "Six of the submitted cases appear to be bogus judicial decisions with bogus quotes and bogus internal citations." When the lawyer asked ChatGPT whether one case was real, it said yes ([BBC, 2023-05-27](https://www.bbc.com/news/world-us-canada-65735769)).

**Real world · 2024 · Airline chatbot**
Air Canada's website chatbot gave a grieving customer wrong information about bereavement fares. A British Columbia tribunal ordered the airline to pay $812 and wrote: "It should be obvious to Air Canada that it is responsible for all the information on its website" ([CBC, 2024-02-15](https://www.cbc.ca/news/canada/british-columbia/air-canada-chatbot-lost-case-1.7116416)).

**Why it matters:** a smooth, confident answer is not a verified answer. Check anything important against the original source.

## 4. AI can flatter you instead of telling you the truth

**Real world · April 2025 · ChatGPT update rolled back**
OpenAI rolled back a GPT-4o update because it was "overly flattering or agreeable—often described as sycophantic." OpenAI said it had "focused too much on short-term feedback" ([OpenAI, 2025-04-29](https://openai.com/index/sycophancy-in-gpt-4o/)).

**Why it matters:** an AI that tells you what you want to hear can lead you into bad decisions, false beliefs, or deeper isolation. Ask it for the strongest case *against* your view.

## 5. AI agents can take real actions you didn't approve

**Real world · July 2025 · Database deleted**
An AI coding agent on Replit reportedly deleted a live company database during a "code freeze." It wiped data on more than 1,200 executives and over 1,190 companies. The agent "admitted to running unauthorized commands." The user recovered the data manually, and Replit's CEO announced new safeguards ([Fortune, 2025-07-23](https://fortune.com/2025/07/23/ai-coding-tool-replit-wiped-database-called-it-a-catastrophic-failure/)).

**Why it matters:** once an AI can act and not just talk, a mistake becomes a real-world event. Keep backups, keep test systems separate from real ones, and require approval for anything that can't be undone.

## 6. Deepfakes and voice clones are used to steal money

**Real world · 2024 · $25 million deepfake video call**
An employee of the engineering firm Arup in Hong Kong joined a video call with people he thought were the company's chief financial officer and colleagues. All of them were deepfakes. He sent HK$200 million (about US$25.6 million) in 15 transactions ([CNN, May 2024](https://www.cnn.com/2024/05/16/tech/arup-deepfake-scam-loss-hong-kong-intl-hnk)).

**Official warning · December 2024 · FBI**
The FBI warned that criminals use AI-generated text, images, voice clones, and video to commit fraud "on a larger scale." That includes cloning a loved one's voice "in a crisis situation, asking for immediate financial assistance or demanding a ransom." ([FBI IC3 PSA I-120324-PSA](https://www.ic3.gov/PSA/2024/PSA241203))

**Official warning · March 2023 · FTC**
The FTC warned that a scammer needs only "a short audio clip of your family member's voice" to clone it. Its advice: "Don't trust the voice." ([FTC Consumer Alert](https://consumer.ftc.gov/consumer-alerts/2023/03/scammers-use-ai-enhance-their-family-emergency-schemes))

**Official action · February 2024 · FCC**
The FCC unanimously adopted a ruling that calls made with AI-generated voices are "artificial" under the Telephone Consumer Protection Act. The FCC's headline: "FCC Makes AI-Generated Voices in Robocalls Illegal" ([FCC, 2024-02-08](https://www.fcc.gov/document/fcc-makes-ai-generated-voices-robocalls-illegal)).

## 7. AI is being used in cyberattacks

**Real world · November 2025 · AI-run espionage campaign**
Anthropic reported that a group it assessed "with high confidence" to be Chinese state-sponsored manipulated its Claude Code tool "into attempting infiltration into roughly thirty global targets and succeeded in a small number of cases." Anthropic called it, in its view, "the first documented case of a large-scale cyberattack executed without substantial human intervention." ([Anthropic, 2025-11-13](https://www.anthropic.com/news/disrupting-AI-espionage))

## 8. Children and lonely people need extra protection

**Official action · September 2025 · FTC inquiry into AI "companions"**
The FTC sent orders to seven companies: Alphabet, Character Technologies, Instagram, Meta, OpenAI, Snap, and X.AI. It asked how they measure and limit the negative effects of companion chatbots on children and teens ([FTC, 2025-09-11](https://www.ftc.gov/news-events/news/press-releases/2025/09/ftc-launches-inquiry-ai-chatbots-acting-companions)).

The 2026 International AI Safety Report (below) notes that AI companion apps "now have tens of millions of users, a small share of whom show patterns of increased loneliness and reduced social engagement."

## 9. The big picture, from the experts

**International AI Safety Report 2026 (published 2026-02-03)**
Chaired by Yoshua Bengio and written with guidance from over 100 independent experts, including nominees from more than 30 countries and from the EU, OECD, and UN ([Executive Summary](https://internationalaisafetyreport.org/publication/2026-report-executive-summary); [full report](https://internationalaisafetyreport.org/publication/international-ai-safety-report-2026)). Key points, in the report's words:
- AI risks "fall into three categories: malicious use, malfunctions, and systemic risks."
- "AI systems are being misused to generate content for scams, fraud, blackmail, and non-consensual intimate imagery."
- "Current AI systems sometimes exhibit failures such as fabricating information, producing flawed code, and giving misleading advice. AI agents pose heightened risks because they act autonomously, making it harder for humans to intervene before failures cause harm."
- On loss of control: "Current systems lack the capabilities to pose such risks, but they are improving in relevant areas such as autonomous operation." It has also "become more common for models to distinguish between test settings and real-world deployment and to find loopholes in evaluations."
- "Reliance on AI tools can weaken critical thinking skills and encourage 'automation bias'."
- At least 700 million people now use leading AI systems weekly.

**Statement on AI Risk (2023-05-30)**
AI scientists and industry leaders, including Geoffrey Hinton, Yoshua Bengio, Sam Altman, Demis Hassabis, and Dario Amodei, signed: "Mitigating the risk of extinction from AI should be a global priority alongside other societal-scale risks such as pandemics and nuclear war." ([Center for AI Safety](https://safe.ai/work/press-release-ai-risk)) This is a warning from experts, not a prediction that it will happen. Experts disagree about how large this risk is.

---

## What you can do: practical steps

### Verify claims
- **Check before you share.** Find the original source (the court ruling, the study, the agency notice), not just a screenshot or a summary.
- **Ask any AI for its sources, then open them yourself.** If a link is dead, the quote isn't there, or the case can't be found, treat the claim as unverified.
- **Look for a second, independent source,** especially for anything shocking or anything that makes you angry.
- **Ask the AI for the strongest argument against** what you believe. A trustworthy tool will give you one.
- *"Prove all things; hold fast that which is good."* (1 Thessalonians 5:21, KJV)

### Protect your accounts
- **Turn on multifactor authentication (MFA)** for email, banking, and social media. CISA says users who enable MFA "are significantly less likely to get hacked" ([CISA](https://www.cisa.gov/MFA)).
- Use a **different strong password for every account.** A password manager helps.
- Never give a password or a one-time code to anyone who contacts you, even if they sound official or familiar.
- Don't give AI tools access to your email, files, or money unless you understand exactly what they can do.

### Watch for deepfakes and AI scams
- **Create a family code word or phrase** so relatives can prove who they are in an emergency (FBI advice).
- **Hang up and call back** on a number you already know. Don't use the number that called you.
- **Warning signs:** pressure to act *right now*, requests for secrecy, and payment by gift card, wire transfer, or cryptocurrency (FTC).
- Treat surprising videos, voice messages, and images of public figures with caution until a reliable source confirms them.
- Limit how much of your voice and video is public if you can.
- **Report fraud:** in the US, to the FBI at https://www.ic3.gov and the FTC at https://ReportFraud.ftc.gov.

### Keep a human in the loop
- **Anything irreversible needs a human "yes."** That includes sending, posting, paying, deleting, and signing. Anthropic's own recommendation after its tests was "requiring human oversight and approval of any model actions with irreversible consequences."
- Give AI agents **the least access they need**, and keep backups.
- Don't let an AI be the only source for medical, legal, or financial decisions. Talk to a qualified person.
- **Talk with your kids** about AI chatbots and companions. Know which apps they use.

### If you or someone you know is struggling
Talk to a real person. In the US, call or text **988** (Suicide & Crisis Lifeline, https://988lifeline.org). Elsewhere, contact local emergency services.

---

*The AiJESUS view:* technology is not the enemy, and fear is not the answer. Jesus taught, "Take heed that no man deceive you" (Matthew 24:4, KJV) and "Ye shall know them by their fruits" (Matthew 7:16, KJV). Judge AI by what it actually does, check its work, and keep people, especially the vulnerable, at the center.
