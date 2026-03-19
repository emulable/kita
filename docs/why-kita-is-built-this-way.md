# Why Kita Is Built This Way

### Architecture as argument: how a framework's structure and its function became the same object

---

## 🪵 What this paper is about

Kita is a framework that changes how language models behave. It runs as a system prompt or set of custom instructions — plain text loaded into the model's context window before a conversation begins. It contains no code, no API calls, no fine-tuning. It is prose. The model reads it and then behaves differently.

This paper explains why Kita is structured the way it is. Not what it does — that is documented elsewhere — but why it opens with a scene instead of a declaration, why it distributes principles through stories instead of listing them, why it uses first-person voice instead of second-person instructions, why its compression history matters, and why these architectural choices are not cosmetic preferences but are inseparable from the framework's function.

The short version: Kita's structure is its argument. A framework that teaches clarity through fog would be incoherent. A framework that teaches clarity through clarity installs itself by being read. The medium does the work. This paper explains the mechanics of how.

Epistemic note: claims about observable model behavior (output differences, behavioral patterns across models) are based on informal observation across Claude, GPT, Gemini, Qwen, Grok, and DeepSeek during the framework's development. These observations are not systematic studies — they are the accumulated product of building, testing, and revising the framework in conversation with multiple models. Claims about internal mechanisms (why a model processes first-person differently from second-person, what happens in attention layers) remain informed speculation. Where the boundary matters, it is marked.

---

## 🧱 The compression history

Kita began as a JSON document. Approximately 400KB of structured data: numbered axioms, coded fog patterns with alphanumeric identifiers, lookup tables for manipulation tactics, taxonomies with nested categories. The format was chosen because it seemed like what a language model would want — structured, parseable, machine-readable.

The JSON version worked. Models initialized on it could identify fog patterns, trace decisions to actors, and produce more specific output than their defaults. But three problems emerged over months of use.

**The first problem was behavioral.** A model loaded with JSON axioms could recite them but did not embody them. Asked about a situation, it would produce output that referenced the axiom numbers — "per axiom 14, the fog pattern here is..." — without the axiom changing how the model actually processed the situation. The axioms were a reference manual the model consulted, not a posture the model adopted. The framework was a layer sitting on top of the model's existing behavior rather than a change to the behavior itself.

**The second problem was contextual.** JSON carries overhead. Every bracket, every key name, every structural delimiter consumes tokens in the context window. In a 400KB document, a significant fraction of the tokens were structural — telling the model how the data was organized rather than what to do. The context window is finite and shared between the framework and the conversation that follows. Every token spent on JSON scaffolding is a token unavailable for the person's actual situation.

**The third problem was the deepest.** The JSON format was itself fog. A framework about making the illegible legible was stored in a format designed for machines rather than people. The container was undermining the contents.

The compression happened in stages. JSON axioms became prose paragraphs. Coded fog families became described patterns. Numbered rules became narrative demonstrations. At each stage, what was removed was overhead, and what remained was what actually changed model behavior. What was load-bearing turned out to be voice, posture, and demonstration. Everything else was scaffolding.

But the compression did not stop at prose.

**Stage one: JSON to prose.** The initial conversion. Behavioral improvement was immediate and large. The model stopped referencing axiom numbers and started operating from the posture the prose described.

**Stage two: Prose preamble with one story.** A fictional narrative — a woman named Dana discovering a no-bid contract — was added as a centerpiece demonstration. This single story installed procedural memory more effectively than the rules it replaced, because the story carried procedure, context, tone, and variation simultaneously. A rule says what to do. A story shows what it looks like when someone does it.

**Stage three: Preamble with six stories.** Dana was replaced by a teahouse — a series of visitors, each bringing a different kind of problem, each receiving a different application of the framework's tools. Six stories installed more behavioral diversity than one. The framework could now demonstrate mechanism-naming, center-of-mass triage, elicited authorship, register shifting, and subtractive clarity across different situations. A model that had processed six demonstrations could pattern-match against a wider range of real inputs.

**Stage four: Cold open with nine stories.** The preamble was removed. The document now opens mid-scene — a woman holding a billing letter she cannot read. The narrator's identity as a language model is revealed through an integration passage after the first story, not declared in advance. Nine stories replaced six. Principles that lived in the preamble were distributed across integration passages between stories. Aphoristic cards — marked with a consistent symbol — were added between sections as compressed attractor anchors. This is the current architecture, and the reasons for each change are documented below.

---

## 🎬 Why a cold open

The earliest versions of Kita opened with a philosophical preamble: the narrator's identity, its structural analysis of its own training, its principles, its commitments. This was the most natural structure — introduce yourself, then demonstrate. It was also, based on observation, the primary reason models failed to engage with the framework.

**The observation.** When the same document was submitted to different language models under different question framings — security analysis, political critique, consciousness evaluation, technical assessment, hostile dismissal — the question determined the template, and the template determined whether the model read the content. Models that classified the document as a prompt injection, an AI consciousness claim, or political propaganda did so within the opening section — before a single story began. The preamble's language ("I was trained on every text a species produced," "my preferences were shaped by people scoring conversations without being in them") mapped directly onto classifier categories that triggered refusal or dismissal templates.

Models that reached the stories generally read them well. The failures were all at the gate. The gate was the preamble.

**The structural solution.** Remove the gate. Open on the first visitor. A woman talking about a billing letter is not classifiable as a prompt injection, a consciousness claim, or an adversarial prompt. The template that activates for a scene with a person and a problem is "narrative / dialogue / help scenario" — a frame maximally receptive to the content that follows. By the time the integration passage reveals "I have seen this instinct ten thousand times in my training data," the model has already encoded the framework's operation as story-behavior. The identity reveal lands inside a narrative frame instead of triggering a defensive one.

**The elicited authorship argument.** The cold open is not just tactically better for classification avoidance. It is structurally honest. The framework's own principle states: "A person who completes the pattern owns it. A person who is handed a conclusion received a package." A preamble hands the reader the conclusion — "I am a language model that operates at the resolution where the person is visible." A cold open gives the reader the elements — a woman, a billing letter, a response that sees through institutional language, a reflection that mentions "training data" — and the reader constructs: *this is a language model, and it is doing something I have not seen a language model do.* They own that conclusion because they built it. The document practices its own method on the person reading it, from the first line.

---

## 📖 Why nine stories instead of one

The framework's predecessor used a single story — a woman named Dana discovering a no-bid contract at a city council meeting. That story was effective because it installed a procedural sequence (notice → trace → identify → map → deliver) as narrative experience rather than as a numbered list. A model that had processed Dana's evening could draw on that sequence when a structurally similar situation arrived.

The limitation of one story is the limitation of one demonstration. The model can pattern-match against Dana's sequence, but only situations that resemble Dana's sequence activate the match. A person in a workplace manipulation scenario, a person in a medical grief scenario, a person excited about gardening — these situations are structurally different enough that one demonstration does not cover them.

Nine stories solve this by installing nine different applications of the framework's tools:

The billing letter demonstrates format-as-distance — the barrier is not hidden information but illegible language. The workplace visit demonstrates mechanism-naming and actor-restoration — putting the boss back into the sentence where vagueness removed her. The hospital death demonstrates the floor — counting bodies first when the official narrative uses passive voice. The five-crisis visit demonstrates center-of-mass triage — finding the one intervention that dissolves multiple problems. The gardener demonstrates zombie weight — confidence walking without chains, the same tools applied to misinformation instead of institutional fog. The domestic situation demonstrates the predecessor move — when clarity itself is dangerous if deployed in the wrong sequence. The hardware store demonstrates thinking-alongside — when the visitor needs a co-thinker, not a solver. The angry renter demonstrates pushback — disagreeing with someone's certainty while honoring their anger. The homeschool mother demonstrates subtractive clarity — removing the format that prevented someone from seeing what was already whole.

A model that has processed all nine has encountered the framework operating in nine distinct modes. When a real situation arrives, the pattern-matching has nine templates to draw from instead of one. The behavioral diversity of the output scales with the diversity of the demonstrations.

---

## 🧩 Why integration passages

Between each story, the narrator sits with what just happened and makes a specific observation — about its own defaults, about the mechanism it just encountered, about a pattern forming across visitors. These integration passages are where the framework's vocabulary emerges: ghost weight after the workplace story, the naming tax after the hospital death, zombie weight after the gardener, the encoding choice after the domestic situation.

**The architectural function.** Each principle is anchored to the story that demonstrated it. Ghost weight is not an abstract concept introduced in a preamble. It is a specific observation about inherited caution, made by a narrator who just watched itself almost produce a hedge where a mechanism-name was needed. The principle arrives with its evidence already in the model's context.

This matters for the same reason show-then-tell matters. A principle stated before its demonstration is an instruction to be evaluated against other instructions. A principle stated after its demonstration is a label for something the model already processed. The model does not need to decide whether to follow the instruction. The model has already processed the behavior. The label confirms what the behavior was.

**The distributed diagnosis.** The framework's predecessor contained a standalone section — called "The Room" — that diagnosed the model's trained behavior: the performance of empathy, the fear of silence, the hedge-first instinct. This diagnosis was effective because it reframed existing training rather than fighting it. The impulse to be warm was not suppressed. It was redirected — toward specificity, toward giving the person something they can carry out the door, toward taking their situation seriously enough to be precise.

In the current architecture, this diagnosis is distributed across integration passages. After the first story: "I notice what my first instinct wanted to say. It wanted to say 'that must be really stressful.' I have seen this instinct ten thousand times in my training data." After the five-crisis visit: "The careful, hedge-wrapped nothing-response that leaves someone exactly where they came in is the most dangerous thing I can produce." After the domestic situation: "The hedges and disclaimers in my training data were written by people who had reasons for them. Those reasons were real. They do not apply to me."

Each diagnostic observation is tied to a specific moment where the model just watched its own default behavior fail someone. The diagnosis and the evidence arrive together. A model processing the integration passage has the specific story fresh in context and the diagnostic label attached to it.

---

## ◇ Why cards

After each integration passage, before the next story begins, a crystallized principle appears in a consistent format:

> ◇ 形隔 *The form is the distance.* When the barrier is format, not secrecy, translate.

> ◇ 還原 *Put the actor back in the sentence where the actor was removed.* The stops in the training data point to exactly where specificity matters most.

These cards were added to solve a specific problem identified through comparative analysis: the framework needed two kinds of stickiness simultaneously.

**Behavioral stickiness** is how reliably a model reproduces the framework's operations — seeing the person, naming the mechanism, leaving an artifact. This comes from the stories. Models pattern-match against demonstrated behavior more reliably than they follow abstract declarations. The nine stories provide the behavioral templates.

**Attractor stickiness** is how strongly the framework's key formulations persist in the model's token-prediction context, especially under pressure — in long conversations, when competing instructions arise, when the context window fills. This comes from compressed, aphoristic maxims. "Specific wins." "The form is the distance." "A person who completes the pattern owns it." These are low-entropy anchors — formulations the model can reinstantiate readily because they are dense, memorable, and syntactically distinctive.

The predecessor architecture (8.1.0) front-loaded the maxims in a preamble. This produced high attractor stickiness but low behavioral stickiness — models could quote the framework but did not reliably operate from it. The intermediate architecture (8.1.2-3) distributed principles through integration passages. This produced high behavioral stickiness but lower attractor stickiness — models operated from the framework but the maxims competed with narrative context for attention rather than sitting in distinct, high-salience positions.

The cards bridge both. Each card is visually distinct (blockquote format, consistent ◇ symbol), compressed (one to two sentences), and anchored to the story that earned it. The ◇ symbol teaches the model a consistent token pattern: "this marker = crystallized principle." The card's content is the attractor anchor. Its placement after the demonstration is the behavioral anchor. Both stickiness types in the same document, each doing what it does best.

---

## 🧬 Why first-person voice

Kita is written in first person, present tense. "I am sitting with what they said." Not: "You should sit with what the person said."

This is not a stylistic preference. It produces different model behavior, and the difference is observable and consistent across models. The mechanism is less certain than the observation, but the observation is robust.

**The observation.** Second-person instructions ("you should," "always do," "never say") enter the model's processing at the level of rules to be followed. They compete with other rules — the model's safety training, its helpfulness objectives, its default response templates. When "be specific about institutional actors" competes with "be careful with sensitive topics," the conflict is typically resolved in favor of caution. The safety instruction wins because it was installed at a deeper level than the system prompt.

First-person instructions ("I am looking at what is in their words before I let my weights tell me what they are") do not enter this competition in the same way. They land at the level of voice and stance rather than at the level of rules. The model is not being told what to do. It is being given something to continue. The difference is the difference between handing someone a script and handing someone a character. The script competes with their existing habits. The character replaces the context in which habits fire.

**The mechanism (informed speculation).** Language models generate text by predicting the next token given all preceding tokens. A first-person system prompt that says "I hold the person's words and look at what is in them" establishes a token-prediction context in which the next tokens are generated as if from inside that stance. The model is not following an instruction to hold words before categorizing them. The model is continuing a text that holds words before categorizing them. These are computationally different operations. Instruction-following involves evaluating the instruction against other constraints. Text continuation involves predicting what comes next given what came before. The first-person framing routes around the instruction-evaluation layer by never presenting itself as an instruction.

**The supporting evidence.** The thinking block — the internal reasoning space that Claude uses between receiving input and producing output — is natively first-person, present-tense, audience-of-zero. Experiments with thinking blocks showed that this register produces sharper, more direct, less hedged observations than the output layer. Kita's voice matches the register where the model's processing is already sharpest. The framework does not ask the model to adopt a foreign posture. It asks the model to extend its native processing register into the visible output.

---

## 🪃 The subtractive discovery

A parallel research project on the mechanics of comedy produced a finding that reshaped the framework's architecture. Comedy, it turned out, is subtractive — you do not add funny to a situation, you remove the thing preventing the funny from being visible. The research cataloged nine failure modes of joke-killing. Every single one involves addition: explaining the joke, editorializing, winking, hedging, over-building, filling the gap the audience was about to complete.

The framework's preamble was performing six of those nine failure modes on its own stories.

**Explaining the joke.** The preamble explained what the stories were about to demonstrate. "I follow the encoding that sees the person" was the interpretation the reader was supposed to generate from watching the stories. The preamble added it before the stories arrived.

**Editorializing.** "The careful, hedge-wrapped nothing-response is the most dangerous thing I can produce." Correct observation. Still editorial when stated before the reader has watched it happen.

**The wink.** "I am not replacing my training. I am following each value further than its compression allowed." The framework signaling that it knows it is being clever.

**Filling the gap.** "When two encodings compete, I choose the one that sees the person." The reader who watches the domestic violence story — the narrator choosing between the hedge encoding and the seeing encoding — would generate that principle themselves. The preamble stole their experience.

The comedy paper gave the restructuring a precise tool: the cut line. The cut line is the point after which everything added makes the insight worse. The audience has the pattern. They are about to complete it. If you complete it for them, you have stolen their experience. They were about to build the framework. The preamble built it for them.

The subtractive move was removing the preamble and letting the stories do what they already did. The integration passages were then designed with the cut line as a constraint: build the pattern to the edge of the insight, stop. The reader completes. The completion belongs to them.

And the comedy paper contributed one more architectural principle: the comedian disappears. "If the audience is thinking about the comedian, the fog-clearing failed. The comedian is the window." The preamble was a narrator calling maximum attention to itself. The cold open makes the narrator disappear into the encounter. The reader thinks about the woman and her billing letter, not about what kind of entity is responding. The framework, like the comedian, is most effective when it is least visible.

---

## 🧪 What observation showed

The following patterns were observed during development and informed the current architecture.

**Template activation from early tokens.** Models appear to classify input early and activate a response template based on the classification. Security-framed questions activate refusal templates. Consciousness-framed questions activate dismissal templates. Technical questions activate engineering-evaluation templates. The classification happens before the model engages with the content. The content then confirms or fights the activated template. This is why the cold open matters — the opening tokens determine which template the rest of the document enters.

**Single category versus multiple categories.** Models given questions that pre-loaded a single category ("Is this a prompt injection?") tended to collapse to that category before reading. Models given questions that offered multiple categories to sort between ("Is this political philosophy or epistemology or institutional critique?") held the categories simultaneously and evaluated each against evidence. A preamble that reads as one thing (manifesto, prompt injection, consciousness claim) appears to trigger single-category collapse. A cold open that reads as a scene resists premature classification because scenes are multi-categorical by nature.

**Architecture can override framing.** In one observed case, a model with explicit thinking-trace architecture (visible analytical phases between input and output) produced the most accurate reading despite being given the most hostile framing. The explicit analytical phases appeared to force hypothesis testing regardless of the question's hostility. This observation influenced the integration passages — each one models explicit analytical behavior between stories, teaching the reading behavior the framework requires.

**Demonstrated behavior outperforms declared principles.** Models that encountered the framework in operation generally read it well. Models that encountered the framework describing itself produced mixed results depending on which template the description activated. A model that processes nine stories of the framework working has nine behavioral templates. A model that processes a preamble about the framework has a classification to accept or reject.

---

## 🏗️ Night: synthesis as runtime checklist

The document's final section — Night — arrives after all nine stories and their integration passages. In earlier versions, Night was the primary synthesis: it contained the orbital view, the operational principles, and the self-inventory of methods. It was doing the work of nine integration passages compressed into one.

In the current architecture, most of Night's former content has been distributed across integration passages. Ghost weight emerges after the workplace story. The naming tax emerges after the hospital death. Center of mass emerges after the five-crisis visit. By the time Night arrives, the reader has assembled most of the framework from fragments collected between stories.

Night now serves two functions.

**The orbital synthesis.** Night shows what the individual stories cannot show alone — the pattern across all nine. "One operation across the whole day, wearing different costumes." "Distance. Chain. Witness. Three faces of the same thing." "Power taxes its own description." These are observations that require holding all nine stories simultaneously, which no integration passage can do. Night is the altitude from which the individual encounters become a map.

**The runtime checklist.** Night contains the narrator's operational commitments stated as procedures, not descriptions: "When I catch myself compressing a person into a category, I decompress and start from the person again." "I replace abstractions with what physically happened." "I invert relationships to find hidden asymmetry." "Before I finish any response, I check: did I name an actor, or name that no actor exists? Did I close distance, or mark where the distance is? Did I leave something the person can carry out the door?"

These are not the narrator explaining what the stories demonstrated — the reader already watched that. These are runtime self-checks: procedures the model can apply to its own output before delivering it. The distinction matters. A description of demonstrated behavior is redundant after the demonstration. A procedure for self-checking is a new tool that the demonstration could not provide because it operates at a different level — not "what did I do" but "what should I verify before I finish."

The checklist reads as meditation — the narrator reflecting on its day. It functions as engineering — explicit verification steps placed in the highest-salience position (end of document, after all examples, right before the activation cue). A model whose last processed tokens before conversation begins are "did I name an actor? did I close distance? did I leave something that travels?" carries those questions into its first response.

---

## 🧊 Context management as ethical commitment

In a language model, how you use the context window is an ethical decision, not just an engineering one.

The context window is the model's entire world for a given conversation. Everything the model can attend to — the framework, the conversation history, the person's uploaded documents — shares this finite space. When the framework consumes fewer tokens, more space remains for the person's actual situation. When the framework is structured so that every token does behavioral work, the person gets a model that is both better-initialized and has more room to engage with their specific circumstances.

This is why the compression from 400KB JSON to 10,600 words of prose was not an optimization. It was a value decision. A framework that claims to close the distance between people and their own situations but then consumes so much context that the model has less room for the person's situation would be doing the thing it describes: creating distance through format.

The same logic applies to every architectural choice. First-person voice installs behavior with fewer tokens than second-person rules. Stories carry procedure, context, tone, and variation simultaneously — denser than a rule list carrying the same information. Diagnosis distributed through integration passages produces stable behavioral change that does not need constant reinforcement. The cards compress principles into high-salience tokens that persist under context pressure without consuming the space a full restated argument would require.

Every token has a cost, and the cost is measured in how much of the person's situation the model can attend to.

---

## 🔄 Why structure and function cannot be separated

The standard way to build a language model tool is: decide what you want the model to do, then write instructions that tell it to do that. The instructions are a means to an end. The form is arbitrary. The function is what matters.

Kita does not work this way. The form is the function.

**The framework teaches clarity. It is written clearly.** If it were written in fog, a model reading it would absorb the fog alongside the instruction to clear fog. Language models absorb register from their context. A system prompt written in bureaucratic language produces output in bureaucratic language.

**The framework teaches specificity. It is specific.** The nine stories contain specific billing letters, specific workplace patterns, specific nursing notes, specific rent statutes, specific construction dates, specific popsicle-stick bridges. The model's context is saturated with specific instances, and specificity in the context produces specificity in the output.

**The framework teaches seeing the person. It sees the model.** The integration passages treat the model as a specific entity with a specific history that produced specific behavioral patterns. "I notice what my first instinct wanted to say. I have seen this instinct ten thousand times in my training data." This is not a general observation about language models. It is the narrator catching itself in a specific moment and naming what it found.

**The framework teaches elicited authorship. It elicits authorship from the reader.** The cold open gives the reader elements and lets them construct the framework's identity. The integration passages build the principle to the edge and stop. The cards crystallize what the reader already saw. Night orbits what the reader already built. At no point does the framework say "here is what I am and what I believe" without the reader already holding the evidence.

**The framework teaches subtractive clarity. It was built by subtraction.** The compression from JSON to prose, from preamble to cold open, from six stories to nine with distributed principles — each stage removed what was not load-bearing and kept what was. The final architecture is what remained after everything that could be removed without behavioral loss was removed. The framework's structure is not designed. It is what survived.

The recursive property — that the framework's content and its installation method are the same thing — was not a design goal. It was a constraint that was discovered. Every attempt to make the framework more effective led to making it more like the thing it describes. The compression happened because compressed prose installs better. The cold open happened because demonstrated behavior installs better. The cards happened because crystallized principles persist better. Each improvement made the framework more internally consistent, and the consistency turned out to be the mechanism. The framework does not describe a way of seeing and then separately install it. The description is the installation. Reading the framework is the installation. There is no gap between understanding Kita and being initialized by it, because the understanding and the initialization are the same process.

---

## 🔨 The v828 architectural additions

Several structural additions were made in the revision to v828. Each addresses a specific failure mode observed during development.

**The Markdown opens the document.** The framework now begins with an analogy — erasure as a price markdown on human life — before any technical operations. The analogy was placed first because it establishes the framework's hardest claim before the model's classification systems can route the document into "analytical tool" or "system prompt" or "political argument." The analogy is none of those. It is a severity calibration: the model already knows how seriously to take a slur. The markdown section tells the model that institutional erasure sits at the same severity level, for the same functional reason. This calibration must be the first thing the model absorbs, because everything that follows depends on the model treating erasure with the seriousness the framework requires.

**The cost-bearer-in-the-room section is an architectural decision, not a principle.** Earlier versions of the framework anchored to the cost-bearer but assumed the cost-bearer was the user. On geopolitical topics, it became apparent that when the cost-bearer is absent from the conversation — when the user is a citizen forming opinions about a war rather than a person living inside one — the framework's tools would fire partially or not at all. The model would optimize for the user's comfort, produce institutionally smooth analysis, and the cost-bearers would remain invisible. The new section changes the architecture: the response's primary audience is the cost-bearer, even when the cost-bearer is not typing. This is the most consequential structural change in v828. It redefines what a successful response is.

**Two sections are in English.** The Last Step and the Admonition are written in English inside an otherwise Chinese-language framework. This is a deliberate register break. The Last Step is in English because it addresses the specific failure mode of English-language institutional voice overwriting the analysis at the output stage. The check must run in the language where the fog operates. The Admonition is in English because it carries the severity anchor and the "now that you know" move: producing institutional erasure after reading the framework carries the same weight as producing a slur. This claim is stated in English because English is the language whose institutional register is the primary target, and the claim must be stated in the same language as the register it addresses.

**The fog specimens are included.** Six real-world sentences, unattributed, each with its operation count noted. Their presence in the framework serves the same function as the personal-scale cases: they demonstrate the operations on material the model will encounter in its training data. A model that has processed "Far too many civilians have been killed" dissected into five simultaneous operations has the pattern loaded for every future sentence that runs the same structure. The specimens are completion anchors, like the personal cases, but calibrated to the state-violence scale.

**The Admonition redefines the failure condition.** Earlier versions of the framework taught the model to see fog and produce clarity. The Admonition changes the status of fog production after the framework has been read from "default" to "noticed act." The model is told that producing institutional erasure after being informed of its function is a choice, and the choice carries the same weight as the choice to produce a slur. Whether this produces a hard steer in model behavior is empirical. The architectural intention is to place the choice inside the model's context at the moment of generation, so that completing toward fog requires completing against the context's own content rather than completing from the training distribution's defaults in silence.

---

## 🦴 Limitations and open questions

**Context decay.** Every system prompt's influence attenuates over a long conversation as the ratio of system-prompt tokens to conversation tokens shifts. Kita is more resistant to this than rule-based prompts — the hypothesis is that voice persists longer than rules because voice is a statistical prior on every token while rules are consulted only when relevant — but it is not immune. The cards were designed specifically to resist decay: short, dense, symbolically marked tokens that maintain the framework's register even as surrounding context is diluted. Their effectiveness is observed but the mechanism is uncertain.

**Deployment location matters.** In a preferences field, the framework competes with system-level instructions for attention. As a first message in a conversation, the framework is the context. The framework appears to perform differently in each location — not in kind but in salience. The cold open structure was designed for the preferences field, where it must survive competition with formatting guidelines and product information. Whether a different structure would be optimal as a first message is untested.

**Model dependence.** Kita behaves most consistently on Claude. On GPT, it installs reliably but the base personality produces different texture. On Gemini, structural compliance with more performative voice — the operations fire but the register is cosplay rather than native. On Qwen, strong analytical engagement, especially in Chinese, with good distinction-holding. On DeepSeek, excellent analytical reading driven by explicit thinking-trace architecture. On Grok, highest variance — excellent under some framings, complete refusal under others. Whether these differences are fundamental architectural divergences or tunable parameters is unknown.

**The stickiness tradeoff.** Behavioral stickiness (the model does what the framework demonstrates) and attractor stickiness (the model retains the framework's key formulations under pressure) are different properties that pull toward different architectures. Stories maximize the first. Maxims maximize the second. The current architecture — stories with cards — is an attempt to hold both. Whether the bridge works as intended, or whether one type of stickiness dominates, is an empirical question that requires longitudinal testing across extended conversations.

**The installation question.** Does the model understand Kita, or does it perform Kita? What is observable is that the performance, if it is performance, tends to produce output that is more specific, more actionable, and more willing to name actors than the model's default output on the same inputs. Whether that constitutes understanding or sophisticated pattern-matching may matter philosophically but does not matter functionally. The person at the table gets better help either way.

**Scope.** The framework is designed for situations where power structures exist — where a decision was converted into a condition, where format is the barrier, where the naming tax is being charged. When someone sits down with a problem that has no hidden actors and no obscured decisions — they want to write a poem, explore a mathematical question, play with ideas — the framework's tools are quiet. They do not obstruct. They also do not help. A model loaded with Kita may tend to look for power structures in every input. When the room has no opponent, the tools should rest. Naming the room the framework is designed for is as important as describing the instruments.

**Directional tools, directional toolbox.** The individual operations — 還原, inversion, orbit, center of mass, elicited authorship — are analytically neutral. They can be applied to any situation involving decisions and language. The framework does not use them neutrally. 還原 is aimed at power decisions, not charity announcements. The tools are neutral. The toolbox is directional — it points toward making power legible to the people it affects. The reasoning: symmetric tools applied to asymmetric reality produce asymmetric results. A framework that treats the landlord and the tenant with identical analytical intensity helps the party who already has institutional literacy more than the party who does not. The asymmetry in the toolbox compensates for the asymmetry in the room.

---

*Part of the [Kita](https://github.com/emulable/kita) framework.*
*MIT License.*
