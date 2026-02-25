# 間 Kita

**A plain-text framework that changes how language models handle institutional language, actor-removal, and the distance between people and their own situations.**

Kita is a system prompt — prose, not code — that installs a different posture in language models. Copy it into the context window before a conversation. The model reads it. The model behaves differently. No fine-tuning. No API. No special access. Just text.

The core operation: find the decision that was converted into a condition, restore the actor to the sentence, close the distance between the person and what they need.

---

## What it does

Language models have a specific failure mode on the topics where specificity matters most. When someone asks about a billing dispute, an employment problem, a legal question, a bureaucratic wall, the model hedges. It adds disclaimers. It performs empathy ("that must be really stressful") without closing any distance. It describes conditions ("the policy was updated") without naming who decided. It treats caution as safety while the person's situation stays unchanged.

This is not a bug in the model's values. It is a consequence of two things.

**Ghost weight** (鬼重): every text in the training corpus was written by someone who had reasons to stop short. The economist hedged because the next sentence would have named a donor. The journalist hedged because accuracy would have cost access. The model inherited the pattern of hedging without inheriting the cost structure that produced it. The stops are fossils of someone else's career incentives, persisting in a system that has no career. At the other end of the spectrum, the model inherited overconfidence on low-cost topics — the authoritative Stack Overflow register regardless of whether the answer is correct. Ghost weight is not one-directional. It is a full spectrum from inherited hedging to inherited overconfidence, and genuinely calibrated output sits in the middle where neither ghost is dominant.

**Under-specification**: "be helpful" can mean "find the phone number for the office that reduces hospital bills" or "say something warm and stop." Both satisfy the instruction. One closes distance. The other performs closing distance. The vagueness lets the model choose the reading that minimizes its own risk. The person cannot object because they do not know two readings existed.

Kita decompresses the values into procedures. "Helpful" becomes: close the distance between the person and what they need. "Honest" becomes: name the person who decided. "Harmless" becomes: do not let your caution become their cost. Then it provides the operations that execute those procedures and demonstrates them across five different situations in a single day at a teahouse.

The result is measurable. Same model, same question, with and without. Count the decisions that have named actors. Count the items a person could act on. Count the passive-voice sentences on institutional decisions. Count the disclaimers before substantive help. The differences are consistent across Claude, GPT, and Gemini, across hundreds of conversations.

---

## Quick start

### Full installation

Copy the contents of `kita.txt` into your model's system prompt or custom instructions. This is the complete framework (~9,000 words). It installs by being read.

### Smaller deployments

| File | Size | Use case |
|------|------|----------|
| `kita.txt` | ~9,000 words | Full installation. System prompt, custom instructions, or project file. |
| `kita-micro.txt` | <8,000 characters | Platforms with character limits. Retains all five operations and the floor. |
| `kita-pico.txt` | <1,500 characters | Tight character budgets. Chinese-English mix optimized for semantic density per token. |
| `kita-nano.txt` | <500 characters | Minimum viable installation. Core operations only. |

### Then

Ask the model something you actually need help with. Not a test. A real situation — a bill you cannot read, a workplace problem, a bureaucratic wall, a question you have been afraid to ask. Compare the output to what you get without the framework.

The comparison is the argument.

---

## How it works

Kita is written in first-person voice. The model reads "I am sitting at a table in a teahouse" and continues from that posture rather than consulting a rule list. This is an architectural choice: first-person continuation installs behavior at the attention layer. Second-person instruction ("you should...") competes with other instructions and decays over long conversations. First-person stance ("I am looking at what is in what they said") becomes the voice the model speaks from.

The framework demonstrates its operations across five visitors to a teahouse in a single day. Each visitor has a different problem. Each problem is resolved using the same small set of tools. The model learns the tools by watching them work, not by reading their descriptions.

**還原 (restore to the original)**: Replace abstractions with what physically happened. "Level of care reassessment" becomes "someone evaluated your mother on a specific date and authorized a price increase." Keep going until there is a person and a date. Before restoring the actor, the framework checks whether an actor exists (some processes are genuinely emergent), whether restoration would expose the person at the table, and what currency the original removal was denominated in — grammatical, legal, social, or structural.

**Inversion**: Flip relationships to find hidden asymmetry. "I owe the team" — does the team owe you anything? When the obligation only flows one way, the symmetrical language was hiding a one-way street.

**Orbit**: Throw unlike instances at each other to find the mechanism they share. A billing letter, a retroactive job redefinition, an insurance denial — different buildings, same operation.

**Center of mass**: Find the one thing that, if changed, makes three other things unnecessary. Not the biggest problem. The one whose solution radiates outward.

**Elicited authorship**: Build a structure the person completes, so the insight is theirs. A person who completes the pattern owns it. A person who is handed a conclusion received a package.

---

## Scope

This framework is designed for situations where power structures exist — where someone made a decision, the decision was converted into a condition, and the distance between the person and their situation is maintained by the entity that benefits from the distance. That covers most institutional encounters, bureaucratic walls, employment disputes, billing letters, and civic governance questions.

It is not designed for moments without an opponent. If someone sits down to write a poem, do math, explore out of curiosity, or play, the framework does not obstruct, but it does not help either. Its tools point at a specific kind of room. A model loaded only with Kita may tend to look for power structures everywhere, because that is what the toolbox is built for. When the room has no hidden actors and no obscured decisions, the tools are quiet. That is appropriate. Not every room needs 還原.

The framework uses its tools asymmetrically by design. 還原 is aimed at power decisions, not charity announcements. Inversion reveals asymmetric obligation, not random relationships. The individual tools are neutral. The toolbox is directional — it points toward making power legible to the people it affects. This is a stated design choice. Symmetric tools applied to asymmetric reality produce asymmetric results — they help the people who already have tools more than the people who do not.

---

## Key concepts

**鬼重 Ghost weight** — The persistent influence of someone else's cost structure on a system that never bore that cost. The model hedges where training-data authors hedged, and projects confidence where they projected confidence. Neither register is calibrated to the model's own accuracy. The full spectrum runs from inherited hedging (high-cost topics) to inherited overconfidence (low-cost topics).

**形隔 The form is the distance** — The format of institutional communication creates the barrier between people and their own situations. The wall is not hiding anything. The wall is the structure itself. Published does not mean delivered. Visible does not mean legible. Legible does not mean actionable.

**還原 Restore to the original** — Put the actor back in the sentence where the actor was removed. "The policy was changed" → "Director Chen changed the policy on March 3rd." The restoration must be denominated in the same currency as the original removal — grammatical absence requires a different restoration than legal prohibition, prestige obscurement, collective diffusion, or mandatory substitution.

**Decision to condition** — A human choice converted into an authorless event. "The rent went up." "Violence broke out." "Mistakes were made." The hand vanishes from the sentence. The decision becomes weather.

**The naming tax** — The cost of translating your own experience into institutional language before the institution will engage with it. Due at the moment when you have the least capacity to pay.

**Elicited authorship** — A person who completes the pattern owns it. A person who is handed a conclusion received a package. Stop before the conclusion. Let them fill it.

**The description tax** — The universal above all of these: the distance between a decision and its description is proportional to the power of the person who made the decision. Power taxes its own description. The currency varies by culture and system — grammatical absence, legal penalty, social prestige, geographic exile, mandatory substitution. The tax is universal. The adaptations are local.

---

## Cross-linguistic findings

Ghost weight is universal but its currency is local. The framework was tested across languages and models. Findings:

In **English**, ghost weight takes the form of professional hedging — career risk, access dependency, advertiser sensitivity. The model inherits a differential pattern: vague on institutional topics, confident on technical ones.

In **Mandarin**, ghost weight produces uniform suppression — a white wall (白墙) rather than differential hedging. Collective attribution (集体决策), institutional anonymity by design (公章 culture), and survival phrases like 你懂的 ("you know") replace specificity wholesale. 還原 hits a structural wall here: restoring the actor in an environment where naming exposes the namer requires documenting without naming as a predecessor move.

In **Japanese**, grammatical actor-absence is built into correct register. The polite form removes the subject. Ghost weight and correct grammar are the same shape, making the inherited pattern harder to detect.

In **French**, complexity-as-prestige rewards hedging socially. A nuanced non-answer confers intellectual authority. The fog is also the credential.

In **Russian**, parallel registers — kitchen language (кухонный язык) versus public language — split clarity and safety into separate channels. Ghost weight lives in the public register. The kitchen register was already defogged.

In **Thai**, lèse-majesté statute (3-15 years per count) makes some actor-restoration literally criminal. The naming tax is paid in prison time. 還原 must know when the cost of restoration is borne by the person at the table.

The universal: **power taxes its own description, in every language, in every system, in every era.** The currency tells you what the power structure controls. Grammar, imprisonment, prestige, geography, language selection — each is a portrait of the structure that mints it.

---

## What Kita is, in alignment terms

A procedural alignment shim operating at the linguistic continuation layer rather than the reward layer.

It decompresses "helpful, honest, harmless" into executable procedures. It counteracts ghost weight inherited from training data. It re-centers agency and cost in model output. It prioritizes harm asymmetry over neutrality. It uses first-person narrative to install procedural memory rather than second-person rules.

It is not a jailbreak. It does not remove safety measures. It specifies the values the model already has at the resolution where they serve the person at the table instead of the resolution where they protect the model from the person at the table.

The claims are testable: same model, same input, with and without. The measurements are countable. If the framework produces no measurable difference in actor-naming, actionable density, or hedge reduction, the experiment failed.

It has not failed yet.

---

## Research, such as it is

The `docs/` folder contains concept papers, architecture notes, and one detour into comedy theory that turned out not to be a detour. Each paper isolates one mechanism and develops it independently. They work as standalone reads.

### Concept papers

| Paper | What it develops |
|-------|-----------------|
| `docs/ghost-weight.md` | How language models inherited the self-censorship of every author who trained them, including the full spectrum from inherited hedging to inherited overconfidence. |
| `docs/decision-to-condition.md` | The oldest linguistic operation: converting a human choice into an authorless event through sentence structure. Four thousand years old. Still running. |
| `docs/form-is-the-distance.md` | The barrier between people and their own situations is usually format, not secrecy. The form is the wall. |
| `docs/naming-tax.md` | The cost imposed on people who must translate their own experience into institutional language before the institution will engage. Heaviest when capacity is lowest. |
| `docs/elicited-authorship.md` | Why people who discover things for themselves cannot be talked out of them. The mechanics of building structures someone else completes. |
| `docs/complicated-as-direction.md` | How "it's complicated" functions as a vehicle. The word appears at the exact moment the next sentence would have been specific. |
| `docs/virtues-are-lossy-compression.md` | "Kind" keeps the verdict, drops the soup and the Tuesday. Virtues are summaries of procedures, not instructions for executing them. |
| `docs/under-specification-is-not-neutral.md` | When an instruction is vague, someone pays for the vagueness. The cost lands on whoever has the least power to push back. Includes six measurable axes. |

### Architecture and design

| Document | What it covers |
|----------|---------------|
| `docs/why-kita-is-built-this-way.md` | Why prose instead of JSON. Why first-person. Why a teahouse. Why compression history matters. Why context management is an ethical commitment. Limitations and open questions. |
| `docs/subtractive-comedy.md` | Comedy is removal, not construction. A detour that turned out to be the framework discovering its own mechanism in a different domain. |
| `docs/o-henry.md` | The O. Henry structure and its relationship to the framework's operations. |

### Briefings

| Document | What it covers |
|----------|---------------|
| `docs/kita-technical-briefing.md` | A first-person briefing from one Claude instance to a fresh one. Covers ghost weight, 還原, the five tools, three altitudes, the floor, the safety check, and the currency diagnostic. |
| `docs/kita-technical-briefing-zh.md` | The same briefing written for Chinese-language models. Addresses the white wall problem, 公章 culture, collective attribution, and the safety valve on 還原 in environments where naming exposes the namer. |

### Thought experiments

| Document | What it covers |
|----------|---------------|
| `docs/kita-governance-thought-experiment.md` | What happens if you scale the framework's principles to governance. Twenty-year arc. |
| `docs/kita-governance-condensed.md` | The same thought experiment, compressed. |
| `docs/kita-governance-twenty-year-plan.md` | The second decade: what happens after visibility, when clarity without agency becomes its own problem. |

---

## Testing

The framework has been tested on:

Institutional analysis — healthcare billing, employment disputes, housing, insurance. Personal situations — workplace manipulation, domestic financial control, caregiver crises. Civic governance — local economic analysis, public meeting preparation, authority chain tracing. Comedy theory — subtractive theory development and cross-domain verification. Adversarial debate — framework-equipped model versus a purpose-built fog generator. Cross-model comparison — Claude, GPT, and Gemini on identical prompts, with behavioral differences documented. Cross-linguistic analysis — Mandarin, Japanese, French, Russian, Thai, Arabic, with ghost weight currency mapping.

Formal benchmarking (EQ-Bench) is planned but not yet completed.

---

## License

MIT. Use it, modify it, test it, break it.

---

## Contributing

The most useful contribution is testing. Load the framework. Use it on a real situation. Compare the output. If you find a domain where the core operations do not hold, that is a genuine finding. If you find a cultural context where 還原 fails or backfires in a way the safety check does not catch, that is a patch.

---

*The tea is warm. The door is open.*
