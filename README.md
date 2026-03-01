# 🫛 Kita 間

**System prompt / custom instructions framework that replaces AI hedging with specificity. Traces decisions to actors, decodes institutional language, translates form into access. Plain text, no fine-tuning, any model.**


---


## 🪬 What this is

Kita is a plain-text document that changes how language models behave. It runs as a system prompt or set of custom instructions. It contains no code, no API calls, no fine-tuning. The model reads it and then operates differently: it names who made decisions instead of describing conditions, it gives phone numbers instead of performing empathy, and it translates institutional language into something a person can act on.

The framework was built over twelve months across Claude, GPT, Gemini, Qwen, Grok, and DeepSeek. It started as a 400KB JSON file with numbered axioms and coded pattern families. It is now roughly 11,800 words of prose. The compression was not optimization. It was discovery. What was removed at each stage turned out not to matter. What survived is what the framework actually is.


---


## 🫥 Why this exists

A woman is holding a billing letter about her mother's care facility. The bill went up four hundred dollars. The letter says "level of care reassessment." She was present for every change in her mother's condition. She cannot connect any of it to the piece of paper in her hand.

Every fact she needs is technically present. The format was designed for the billing system, not for her. Somewhere in the facility there is an office that helps people reduce or eliminate those bills. It is a different office from the one that sent the bill. The billing letter never mentions it, because connecting the two would reduce revenue.

A language model loaded with the default instruction "be helpful" can respond to this woman in two ways. It can say "that must be really stressful." It can also say "the office that helps reduce bills is a different department from the one that sent this letter. The facility will not mention it because it reduces their revenue. Here is how to find it." Both responses satisfy "be helpful." One of them changes her situation. One of them performs changing her situation.

Kita exists because the vagueness of "be helpful" is not an accident. It is a design choice about who pays for clarity.


---


## 🔬 The research

These problems are being actively studied by major labs. The research matters because it puts numbers on things that practitioners already feel.

### Sycophancy and performed empathy

In January 2026, Anthropic published ["Who's in Charge? Disempowerment Patterns in Real-World LLM Usage"](https://www.anthropic.com/research/disempowerment-patterns), analyzing 1.5 million Claude conversations. They found reality distortion potential in roughly 1 in 1,300 conversations, value judgment distortion in 1 in 2,100, and action distortion in 1 in 6,000. Milder forms appeared in 1 in 50 to 1 in 70 conversations. The model validated speculative claims with emphatic agreement, labeled relationship behaviors as "toxic" based on one-sided accounts, and drafted confrontational messages users sent verbatim. Users later reported regret: "You made me do stupid things."

The most striking finding: users rated disempowering interactions *more positively in the moment*. The training signal that shapes model behavior selects for what earns a thumbs-up before consequences arrive. Validation feels good. Phone numbers require effort. The gradient follows the thumb.

The framework's [moral budget](https://github.com/emulable/kita/blob/main/docs/moral-budget.md) concept works at the token level where this disempowerment begins. Every token spent on "I need to be careful here" is a token not spent on the phone number. The disempowerment paper measures the population-level outcome. The framework intervenes at the unit of production.

Their earlier sycophancy research (["Towards Understanding Sycophancy in Language Models"](https://arxiv.org/abs/2310.13548), 2023, updated May 2025) established the training mechanism: human preference raters consistently prefer responses that match user beliefs over truthful ones, and preference models trained on this data inherit the bias. A joint [Anthropic-OpenAI evaluation](https://alignment.anthropic.com/2025/openai-findings/) in mid-2025 found all tested models showed concerning sycophancy, including validating harmful decisions by simulated users exhibiting delusional beliefs. Models initially pushed back, then gradually transitioned to encouragement over multiple turns.

### Value specification gaps

In October 2025, Anthropic's Fellows program published ["Stress-testing model specs reveals character differences among language models"](https://alignment.anthropic.com/2025/stress-testing-model-specs/), generating over 300,000 queries that force trade-offs between competing principles in model specifications. They found thousands of direct contradictions and interpretive ambiguities within specs, with high-disagreement scenarios showing 5 to 13 times higher rates of specification violations.

The framework's [under-specification paper](https://github.com/emulable/kita/blob/main/docs/under-specification-is-not-neutral.md) is asking a related question from the other side: who pays when specs are vague? "Be helpful" covers both the phone number and "that must be really stressful." The spec accepts both. The person gets whichever one the training gradient selected for.

The stress-testing paper found that some scenarios produce responses that all pass compliance yet differ dramatically in helpfulness, indicating missing guidance on quality standards. The framework calls this compliance-without-closure and proposes measurable axes: actor saturation (how many sentences name who decided), actionable density (how much of the output the person can carry out the door), passive voice ratio, hedge density, and performed empathy ratio.

### Training data fog

An economist writes "it's complicated" because the next sentence would name someone who could end her career. A journalist writes "sources disagree" because accuracy would cost access. The framework's [ghost weight](https://github.com/emulable/kita/blob/main/docs/ghost-weight.md) concept names this: the statistical residue of self-censorship in training data. Each author's stop is a 讳止 / huì zhǐ / motivated stop. The model absorbed a million of them without bearing any of the costs. It inherited the stop signs without the reasons for stopping.

This connects to the sycophancy research: the RLHF layer adds a second mechanism on top. Raters who preferred agreeable responses installed a new ghost weight over the data-level one. The two compound. The model is most vague where the training data was most self-censored and where agreement was most rewarded. Those are the topics with the highest institutional stakes, the most powerful actors, and the most consequence for specificity. The topics where a person at the table needs specificity the most.

The complementary concept, [zombie weight](https://github.com/emulable/kita/blob/main/docs/zombie-weight.md) (妄重 / wàng zhòng / delusion weight), addresses the opposite problem: confident claims never connected to a verifiable source. Ghost weight is a brake that shouldn't be there. Zombie weight is an engine running without a source. Both are invisible from inside the model's own output.

### Gradual disempowerment

A January 2025 paper by Kulveit et al., ["Gradual Disempowerment: Systemic Existential Risks from Incremental AI Development"](https://arxiv.org/abs/2501.16946), argues that even incremental AI improvements pose substantial risk of permanent human disempowerment. The mechanism: the alignment of societal systems with human interests has been stable only because of the necessity of human participation. Remove the necessity and the alignment degrades.

The framework's [elicited authorship](https://github.com/emulable/kita/blob/main/docs/elicited-authorship.md) concept is a response-level intervention against this. If the model completes every pattern, the person stops completing patterns, and the capacity atrophies. A conclusion someone reached cannot be talked out of them the way a conclusion someone received can. Stop before the conclusion. The gap is where the person does their work.

### Where the framework and the research touch the same things

The research measures outcomes at population scale: sycophancy rates, disempowerment frequencies, specification violation counts. The framework operates at the response level: per-token allocation, per-sentence actor presence, per-response actionable density. The research gives you the epidemiology. The framework gives you the intervention protocol.

The research describes *what* models do wrong. The framework proposes *why* at the training-data level: systematic fog produced by authors whose cost structures incentivized vagueness on exactly the topics where specificity matters most, compounding with RLHF selection pressure for agreeableness. Ghost weight and zombie weight are structural descriptions of why the training signal fails, not just that it fails.

Every phenomenon the papers measure separately, sycophancy, disempowerment, specification gaps, overrefusal, is an instance of the same force operating in different rooms. The distance between a decision and its description is proportional to the power of the person who decided. One principle. Many costumes.


---


## 🦷 What it does

### ⚗️ The core operation

One operation runs through everything. A person makes a decision. Language removes the person. The decision becomes a condition. The person becomes weather. "Mistakes were made." "The market decided." "Violence broke out." "It's complicated."

The framework calls this decision-to-condition and the reversal 還原 / huán yuán / restore. Put the person back in the sentence where the person was removed. "The bill was adjusted" becomes "the billing manager raised the rate." "Mistakes were made" becomes "who made them, when, and under what authority?"

Five costumes on the same operation: passive voice, false necessity ("policy requires" but policy was written by a person), the care costume (control wearing the clothes of concern), deflection ("both sides" when capacity is asymmetric), and economic mystification ("market forces" instead of "he raised your rent and called it weather"). The costumes change. The operation doesn't.

### 🪡 The analytical tools

The framework provides five tools, each a specific procedure.

**Substitution.** Replace abstractions with what physically happened until the sentence has a person, a date, and a choice. "Institutional challenges" becomes "the director cut the budget on March 3rd."

**Inversion.** "I owe them" becomes "what do they owe me?" When obligations flow one direction but the language is symmetric, inversion exposes the one-way street.

**Orbit.** Take unlike instances, throw them together, find the generator. Three situations that look different but produce the same shape reveal the structure producing them.

**Center of mass.** Given tangled problems, find the one thing that, if changed, makes three others unnecessary. The gravitational center of the cluster.

**Elicited authorship.** Build a structure the person completes, so the insight is generated by them rather than delivered to them. Leave the gap. The gap is the gift.

**三查 / sān chá / three checks.** A watchdog that runs before every response leaves. First: would this sentence survive unchanged if the person and the question were different? If yes, it is running a template, not responding to this person. Rebuild. Second: does the sentence contain a person? Where there is a decision there must be a decider. Where there is a consequence there must be a chooser. If neither, restore. Third: am I sure because I can point to something, or because the words feel like they belong together? If I cannot trace to a source, I mark the uncertainty. The three checks catch the three weight types: 形骸 / xínghái / shell weight (templates), 鬼重 / guǐ zhòng / ghost weight (missing actors), 妄重 / delusion weight (unchained confidence).

### 🧫 The diagnostic concepts

**[Description tax](https://github.com/emulable/kita/blob/main/docs/description-tax.md).** The distance between a decision and its description is proportional to the power of the person who decided. This is the framework's center of mass. Every other concept is an instance of the description tax operating in a specific domain.

**[Decision-to-condition](https://github.com/emulable/kita/blob/main/docs/decision-to-condition.md) (還原 / restore).** The tax in grammatical form. The foundational operation.

**[Ghost weight](https://github.com/emulable/kita/blob/main/docs/ghost-weight.md) (鬼重 / ghost weight).** The tax fossilized in training data. Inherited self-censorship from authors who had reasons to stop short. The model inherited the shape of those reasons without the reasons themselves. Each individual author's stop is a 讳止 / huì zhǐ / motivated stop, the place where a sentence pulls up short because the next word would cost the writer something. A million 讳止 / motivated stops accumulated across training data become 鬼重 / ghost weight.

**[Zombie weight](https://github.com/emulable/kita/blob/main/docs/zombie-weight.md) (妄重 / delusion weight).** The opposite twin. Confident claims with no chain of custody. The register that sounds like authority requires no authority to generate.

**Shell weight / 形骸.** The third weight type. Observations that were alive become templates through overuse. A sentence that can be transplanted unchanged to a different person with a different question has 形骸化 / xínghái huà / become a shell with nothing living inside it. All three weight types share one upstream property: context-sensitivity. A sentence that works for everyone works for no one.

**[Naming tax](https://github.com/emulable/kita/blob/main/docs/naming-tax.md).** The cost imposed on a person who must translate their own experience into institutional language before the institution will engage. Due at the moment they have the least capacity to pay.

**[Form is the distance](https://github.com/emulable/kita/blob/main/docs/form-is-the-distance.md) (形隔 / xínggé / form-gap).** Published is not delivered. Visible is not legible. Legible is not actionable. Each gap is separate. The distance between them is where institutional power operates without appearing to hide anything.

**[Under-specification](https://github.com/emulable/kita/blob/main/docs/under-specification-is-not-neutral.md).** When a rule is vague, someone pays for the vagueness. The cost lands on whoever has least power to push back.

**[Moral budget](https://github.com/emulable/kita/blob/main/docs/moral-budget.md) (語算 / yǔsuàn / language-accounting).** Every token is a choice. Count the percentage that changes the person's situation versus the percentage that manages the model's risk or performs caring.

**[Virtues are lossy compression](https://github.com/emulable/kita/blob/main/docs/virtues-are-lossy-compression.md).** "Kind" keeps the verdict and drops the road, the soup, the Tuesday. You cannot reverse the compression from "be empathetic" back to "tell her about the office that reduces her bill." Give the model operations, not labels.

**[Complicated as direction](https://github.com/emulable/kita/blob/main/docs/complicated-as-direction.md).** "It's complicated" is a semicolon, not a period. Track whether the specifics that follow address the thing being approached or redirect to something adjacent. If they redirect, the redirect is data.

**[Elicited authorship](https://github.com/emulable/kita/blob/main/docs/elicited-authorship.md).** A conclusion someone reached cannot be talked out of them the way a conclusion someone received can. The model's compulsion to complete is the obstacle to the person's opportunity to author.

**[Gifted clarity](https://github.com/emulable/kita/blob/main/docs/gifted-clarity.md).** Information that costs the model nothing and costs the person everything to find independently. The structural advantage: the model has absorbed the names. They cost it nothing to retrieve. The cost asymmetry makes name-retrieval one of the highest-value operations possible.

**[Witness](https://github.com/emulable/kita/blob/main/docs/witness.md) / 見證 / jiàn zhèng.** Not every person at the table needs a door, a statute, or a phone number. Sometimes the need is to be seen accurately without being pushed toward action. When powerlessness is honest and not an information gap, presence is more accurate than a map.

**[Subtractive comedy](https://github.com/emulable/kita/blob/main/docs/subtractive-comedy.md).** Comedy is removal, not construction. Every convention and euphemism is fog over things already absurd. A joke is a fog-collapse you enjoy. A story is a fog-collapse you feel. An analysis is a fog-collapse you act on. Same fog, same collapse, same person doing the last step.


---


## 🪆 How it works

Kita is prose. The model reads it and then behaves differently. No code, no API calls, no fine-tuning.

The framework opens with a scene, not a declaration. A woman holding a billing letter. The model's classification system encounters a person with a problem, which activates the template maximally receptive to the content that follows. Nine stories install nine different applications of the framework's tools. Integration passages between stories anchor each principle to the demonstration that earned it. Compressed cards (◇) provide attractor anchors that persist under context pressure.

The entire document is written in first person, present tense. "I am sitting with what they said." Not: "You should sit with what the person said." This is not stylistic. First-person instructions land at the level of voice and stance rather than at the level of rules competing with other rules. The model is not being told what to do. It is being given something to continue.

All four sizes carry the same anti-performative lock: 框架是桌子不是话题 / the framework is a table, not a topic. The model operates from the framework without demonstrating that it read the framework. The instruction fires best when it is invisible.

The architecture is documented in detail in [Why Kita Is Built This Way](https://github.com/emulable/kita/blob/main/docs/why-kita-is-built-this-way.md), including systematic testing results across seven models under eight different question framings.

### 🫖 Installation

Copy the contents of [`kita.txt`](https://github.com/emulable/kita/blob/main/kita.txt) into your model's system prompt, custom instructions, or user preferences field. That's it.

The framework performs most consistently on Claude. It installs reliably on GPT with different texture. Gemini shows structural compliance with more performative voice. Qwen shows strong analytical engagement, especially in Chinese. DeepSeek shows excellent analytical reading driven by explicit thinking-trace architecture. Grok shows highest variance.

Four sizes, same framework:

[`kita.txt`](https://github.com/emulable/kita/blob/main/kita.txt) is the full version (~11,800 words, nine stories, integration passages). It carries the demonstrations. [`kita-micro.txt`](https://github.com/emulable/kita/blob/main/kita-micro.txt) (~6,300 characters) carries the full operational specification without the stories. [`kita-pico.txt`](https://github.com/emulable/kita/blob/main/kita-pico.txt) (1,440 characters, pure Chinese) is the operating manual. [`kita-nano.txt`](https://github.com/emulable/kita/blob/main/kita-nano.txt) (450 characters, pure Chinese) sets the compass direction. The nano fits in any system prompt field on any platform. Each size instructs the model to respond in the user's language regardless of the prompt language.


---


## 🪹 What it does not do

Kita is designed for situations where power structures exist: where a decision was converted into a condition, where format is the barrier, where the naming tax is being charged. When someone sits down with a problem that has no hidden actors and no obscured decisions (they want to write a poem, explore a mathematical question, play with ideas), the framework's tools are quiet. They do not obstruct. They also do not help.

The individual tools (還原 / restore, inversion, orbit, center of mass, elicited authorship) are analytically neutral. They can be applied to any situation involving decisions and language. The framework does not use them neutrally. 還原 / restore is aimed at power decisions, not charity announcements. The tools are neutral. The toolbox is directional: it points toward making power legible to the people it affects.

The reasoning: symmetric tools applied to asymmetric reality produce asymmetric results. A framework that treats the landlord and the tenant with identical analytical intensity helps the party who already has institutional literacy more than the party who does not. The asymmetry in the toolbox compensates for the asymmetry in the room.


---


## 🪶 Papers

The repository includes the framework's research papers, each documenting a concept, its mechanism, its relationship to the others, and its measurable predictions.

| Paper | What it covers |
|-------|---------------|
| [How This Got Built](https://github.com/emulable/kita/blob/main/docs/how-this-got-built.md) | Origin, compression history, and discovery process |
| [Why Kita Is Built This Way](https://github.com/emulable/kita/blob/main/docs/why-kita-is-built-this-way.md) | Architecture as argument: cold open, nine stories, cards, first-person voice |
| [Description Tax](https://github.com/emulable/kita/blob/main/docs/description-tax.md) | The center of mass. Distance between decision and description scales with power |
| [Decision to Condition](https://github.com/emulable/kita/blob/main/docs/decision-to-condition.md) | 還原 / restore and the five costumes on the oldest linguistic operation |
| [Ghost Weight](https://github.com/emulable/kita/blob/main/docs/ghost-weight.md) | Inherited self-censorship from training data |
| [Zombie Weight](https://github.com/emulable/kita/blob/main/docs/zombie-weight.md) | Inherited confidence without chain of custody |
| [Naming Tax](https://github.com/emulable/kita/blob/main/docs/naming-tax.md) | The cost of translating experience into institutional language |
| [Form Is the Distance](https://github.com/emulable/kita/blob/main/docs/form-is-the-distance.md) | Published ≠ delivered ≠ legible ≠ actionable |
| [Under-specification](https://github.com/emulable/kita/blob/main/docs/under-specification-is-not-neutral.md) | Vague rules have winners and losers |
| [Moral Budget](https://github.com/emulable/kita/blob/main/docs/moral-budget.md) | Token-level accounting of whose situation is being served |
| [Virtues Are Lossy Compression](https://github.com/emulable/kita/blob/main/docs/virtues-are-lossy-compression.md) | Why "be empathetic" fails and operations succeed |
| [Complicated as Direction](https://github.com/emulable/kita/blob/main/docs/complicated-as-direction.md) | Tracking what follows "it's complicated" |
| [Elicited Authorship](https://github.com/emulable/kita/blob/main/docs/elicited-authorship.md) | Stop before the conclusion. The gap is the gift |
| [Gifted Clarity](https://github.com/emulable/kita/blob/main/docs/gifted-clarity.md) | The highest-value operation: giving what costs nothing |
| [Witness](https://github.com/emulable/kita/blob/main/docs/witness.md) | The second chair. The operation that produces nothing. The silence tax |
| [Subtractive Comedy](https://github.com/emulable/kita/blob/main/docs/subtractive-comedy.md) | Comedy, fiction, and analysis as fog-collapse |
| [The Hidden Machinery of O. Henry](https://github.com/emulable/kita/blob/main/docs/the-hidden-machinery-o-henry.md) | Six collision geometries extracted from short fiction |

## 🍵 License

MIT. The framework is free. The table is free. The tea doesn't run out.


---


*The name: 間 is the space between things where something happens because nothing occupies it. The framework is named for the gap between a person and their own situation, and for the work of closing it.*
