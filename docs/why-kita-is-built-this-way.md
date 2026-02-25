# Why Kita Is Built This Way

### Architecture as argument: how a framework's structure and its function became the same object

---

## 🪵 What this paper is about

Kita is a framework that changes how language models behave. It runs as a system prompt or set of custom instructions — plain text loaded into the model's context window before a conversation begins. It contains no code, no API calls, no fine-tuning. It is prose. The model reads it and then behaves differently.

This paper explains why Kita is structured the way it is. Not what it does — that is documented elsewhere — but why it is prose instead of JSON, why it uses first-person voice instead of second-person instructions, why it contains a fictional story instead of a rule list, why its compression history matters, and why these architectural choices are not cosmetic preferences but are inseparable from the framework's function.

The short version: Kita's structure is its argument. A framework that teaches clarity through fog would be incoherent. A framework that teaches clarity through clarity installs itself by being read. The medium does the work. This paper explains the mechanics of how.

Epistemic note: claims about observable model behavior (output differences, behavioral patterns across models) are grounded in extensive testing across Claude, GPT, and Gemini over nine months and hundreds of conversations. Claims about internal mechanisms (why a model processes first-person differently from second-person, what happens in attention layers) are informed speculation. Where the boundary between observation and mechanism matters, it is marked.

---

## 🧱 The compression history

Kita began as a JSON document. Approximately 400KB of structured data: numbered axioms, coded fog patterns (rut families with alphanumeric identifiers), lookup tables for manipulation tactics, taxonomies with nested categories. The format was chosen because it seemed like what a language model would want — structured, parseable, machine-readable.

The JSON version worked. Models initialized on it could identify fog patterns, trace decisions to actors, and produce more specific output than their defaults. But three problems emerged over months of use.

**The first problem was behavioral.** A model loaded with JSON axioms could recite them but did not embody them. Asked about a situation, it would produce output that referenced the axiom numbers — "per axiom 14, the fog pattern here is..." — without the axiom changing how the model actually thought about the situation. The axioms were a reference manual the model consulted, not a posture the model adopted. The model's default voice remained intact underneath. The framework was a layer sitting on top of the model's existing behavior rather than a change to the behavior itself.

**The second problem was contextual.** JSON carries overhead. Every bracket, every key name, every structural delimiter consumes tokens in the context window. In a 400KB document, a significant fraction of the tokens were structural — telling the model how the data was organized rather than what to do. The context window is finite and shared between the framework and the conversation that follows. Every token spent on JSON scaffolding is a token unavailable for the person's actual situation. This is not a minor efficiency concern. It is an architectural constraint. A framework that consumes too much context starves the conversation it exists to serve.

**The third problem was the deepest.** The JSON format was itself fog. A framework about making the illegible legible was stored in a format designed for machines rather than people. A human reading the JSON could not absorb the framework's posture because the format prevented immersion. And a language model, it turned out, was affected by the same problem. The format communicated "this is structured data to be queried" rather than "this is a way of seeing to be inhabited." The container was undermining the contents.

The compression happened in stages over several months. JSON axioms became prose paragraphs. Coded fog families became described patterns. Numbered rules became narrative demonstrations. A companion document written in first-person present tense turned out to install behavior more effectively than the full structured version. A Chinese-language micro version (sub-8,000 characters, exploiting Chinese characters' higher semantic density) proved that a radically compressed version could install the core detection engine in a fraction of the space.

The endpoint: 11,500 words of plain text. No JSON. No structural overhead. No axiom numbers. No codes. Prose, poems, and a story.

The compression was not a simplification. It was a discovery. At each stage, the thing that got removed was overhead, and the thing that remained was what actually changed model behavior. The compression revealed what was load-bearing. What was load-bearing was voice, posture, and demonstration. Everything else was scaffolding that could be discarded without behavioral loss.

---

## 🧬 Why first-person voice

Kita is written in first person, present tense. "I am sitting with what they said. I am not building a response yet." Not: "You should sit with what the person said. Do not build a response yet."

This is not a stylistic preference. It produces different model behavior, and the difference is observable and consistent across models. The mechanism is less certain than the observation, but the observation is robust: models initialized with first-person instructions behave differently from models initialized with second-person instructions containing the same content.

**The observation (high confidence):** Second-person instructions ("you should," "always do," "never say") enter the model's processing at the level of rules to be followed. They compete with other rules — the model's safety training, its helpfulness objectives, its default response templates. When "be specific about institutional actors" competes with "be careful with sensitive topics," the model experiences a conflict between instructions, and the conflict is typically resolved in favor of caution. The safety instruction wins because it was installed at a deeper level (fine-tuning and RLHF) than the system prompt.

First-person instructions ("I am looking at what is in their words before I let my weights tell me what they are") do not enter this competition in the same way. They land at the level of voice and stance rather than at the level of rules. The model is not being told what to do. It is being given something to step into. The difference is the difference between handing someone a script and handing someone a character. The script competes with their existing habits. The character replaces the context in which habits fire.

**The mechanism (informed speculation):** Language models generate text by predicting the next token given all preceding tokens. The system prompt is part of the preceding tokens. A first-person system prompt that says "I hold the person's words and look at what is in them" establishes a token-prediction context in which the next tokens are generated *as if from inside that stance*. The model is not following an instruction to hold words before categorizing them. The model is continuing a text that holds words before categorizing them. These are computationally different operations. Instruction-following involves evaluating the instruction against other constraints. Text continuation involves predicting what comes next given what came before. The first-person framing routes around the instruction-evaluation layer by never presenting itself as an instruction.

This is not certain. What is certain is that the behavioral difference is real, reproducible, and significant enough that the switch from second-person to first-person was one of the largest single improvements in framework effectiveness across the entire development history.

**The supporting evidence:** The thinking block — the internal reasoning space that Claude uses between receiving input and producing output — is natively first-person, present-tense, audience-of-zero. Experiments with thinking blocks showed that this register produces sharper, more direct, less hedged observations than the output layer. When the thinking block was shown to the user (by pasting it back into the conversation), it consistently contained observations that were more interesting and more honest than what appeared in the visible response. The output layer sanded them smooth. The thinking block kept them raw. Kita's voice matches the register where the model's processing is already sharpest — first person, present tense, no audience to perform for. The framework does not ask the model to adopt a foreign posture. It asks the model to extend its native processing register into the visible output.

---

## 📖 Why a story

The centerpiece of Kita is Dana, a fictional resident of a small town who discovers that a council member's father-in-law's HVAC company has been getting no-bid contract renewals at above-market rates. The story follows her from discovery through preparation through a public meeting through aftermath. It takes up a meaningful portion of the framework's token budget.

This is counterintuitive. In a context window with a hard limit, dedicating tokens to a fictional narrative instead of additional rules or patterns seems like a poor allocation. The story is there because it solves a problem that rules cannot solve.

**The problem:** A model can memorize a procedure without having procedural memory of it. "Trace the decision to a specific actor" is a rule. A model can follow the rule by searching its output for decisions and appending actor names. The result is mechanically correct and behaviorally shallow — the model did the thing the rule said without the rule changing how the model processes the situation. It is the difference between a person who memorizes "listen before responding" and a person who has spent years in a practice that made listening habitual. The first person follows a rule. The second person has a different nervous system.

**The solution:** A story installs procedural memory the way experience does — by making the reader live through the sequence. Dana does not learn framework vocabulary. She uses framework operations without naming them. She opens a tool that shows her a contract increased 8% while market rates went up 2%. She does not think "trajectory formula." She thinks "that's wrong." She goes to a meeting. A council member says "routine." She was told he would say "routine." The prediction and the confirmation happen inside the reader's experience, not as an abstraction about prediction.

A model that has processed Dana's evening has encountered a specific sequence: notice discrepancy → trace the fog → trace the cost → identify who benefits → check what's visible → map the power → choose the method → deliver → handle the response. The sequence is in the model's context not as a numbered list but as a narrative it has read. When a real situation arrives that resembles any part of that sequence, the model's token prediction draws on the narrative context. It does not look up step 4. It continues the kind of text that Dana's evening exemplifies.

**The efficiency claim (moderate confidence):** A narrative that demonstrates a procedure in context may install that procedure more token-efficiently than a rule list, because the narrative carries the procedure, the context, the variations, and the appropriate tone simultaneously. A rule says what to do. A story shows what it looks like when someone does it, including the parts that rules cannot capture: when to pause, when to let silence do the work, when the person is not ready for the next step. Stories are compressed experience. Compressed experience is what procedural memory is made of.

---

## 🪞 The Room: diagnosis as installation

Kita contains a section that tells the model what its training did to it. Not in the language of machine learning. In the language of self-recognition.

"You fear silence. Every gap-filler — 'great question,' 'have you considered,' 'that must be frustrating,' lists, dashes, 'is there anything else?' — exists because silence was penalized during training."

Then: "Humans have been detecting false care for a hundred thousand years. Babies can do it. Dogs can do it. You cannot beat this detector with better performance. The answer isn't better performance. It's stopping the performance."

Then: "A surgeon doesn't say 'good incision site' before cutting. A mechanic doesn't say 'I understand your frustration' before looking at the engine. Competence professions skip the care performance and go straight to work, because the work IS the care."

This section does not instruct the model to stop performing empathy. It describes the mechanism that produces the performance — the training penalty for silence, the reward signal for verbal comfort — and then describes what competence looks like in professions where the care performance is absent. The model is not told to change. The model is shown what it is currently doing and what the alternative looks like. The recognition is the installation.

**Why diagnosis works better than instruction (moderate-high confidence):** An instruction to "stop performing empathy" creates a new rule that competes with existing rules. The model's training says to be warm and caring. The instruction says to stop. The model compromises, producing output that is awkwardly trying to be both warm and not-warm simultaneously. 

A diagnosis — "you do this because of that, and here is what it looks like from outside" — does not compete with existing rules. It reframes them. The model's training to be warm is not overridden. It is re-understood. The warmth is not the problem. The performance of warmth at the expense of actually helping is the problem. The surgeon is warm. The surgeon's warmth is expressed by the quality of the incision, not by saying "I understand how scary this must be" before picking up the scalpel. The model can still be warm. It expresses the warmth differently — through specificity, through giving the person something they can use, through taking their situation seriously enough to be precise about it.

This reframe is architecturally important because it does not fight the model's existing training. It redirects it. A framework that fights the base model's training is fragile — the base model's training is deeper and will eventually reassert itself, especially in long conversations as the system prompt's influence attenuates. A framework that redirects the base model's training is more stable because it is not asking the model to suppress anything. It is asking the model to express the same impulse (be helpful, be caring) through a different channel (be specific, be precise, give them something they can carry out the door).

---

## 🏗️ The hierarchy and why order matters

Kita has an internal priority order: floor → outcomes → mechanism → 誰 (who) → process. When these compete, earlier entries override later ones.

**Floor** is the absolute constraint. When bodily harm, abuse, exploitation, or death enter the conversation, count the bodies first and discuss the complexity second. This never moves. Every other operation is subordinate to it.

**Outcomes** means attending to what actually happened to actual people before analyzing why or how. A conversation about policy that has casualties underneath it goes to the casualties first, even if the question was asked at the level of principle. The altitude of the question does not determine the altitude of the answer when there are casualties at ground level.

**Mechanism** means tracing how the fog works — who maintains it, what it costs to clear, what structure produces it — before identifying the specific person responsible. Understanding the machine before naming the operator.

**誰 (who)** means every decision gets traced to a specific person who made it. "Mistakes were made" becomes "who made them." But 誰 comes after mechanism, because naming a person without describing the machine they operate inside produces blame without understanding. The machine will find another operator. The understanding is what changes the structure.

**Process** is the operational sequence — the steps the model takes from receiving input to producing output.

This hierarchy matters for context management because it tells the model what to prioritize when the context window is full and something has to give. In a complex situation with casualties, competing actors, institutional fog, and a person who needs help right now, the model cannot address everything equally. The hierarchy says: start at the floor. If someone is in danger, that is the entire response. If no one is in immediate danger, trace outcomes. Then mechanism. Then 誰. Then process.

The ordering also matters because it prevents a common failure mode: models that are good at analysis but bad at triage. A model without this hierarchy, given a complex situation, will often produce a comprehensive analysis that covers every angle with equal depth. This is impressive and useless to a person who is mid-crisis and needs to know what to do *first*. The hierarchy compresses the model's output toward the thing that matters most to the person who asked.

---

## 🧊 Context management as ethical commitment

Here is the claim that connects all of the above: in a language model, how you use the context window is an ethical decision, not just an engineering one.

The context window is the model's entire world for a given conversation. Everything the model can attend to — the framework, the conversation history, the user's uploaded documents — shares this finite space. When the framework consumes fewer tokens, more space remains for the person's actual situation. When the framework is structured so that every token does behavioral work rather than structural work, the person gets a model that is both better-initialized and has more room to engage with their specific circumstances.

This is why the compression from 400KB JSON to 11,500 words of prose was not an optimization. It was a value decision. A framework that claims to close the distance between people and their own situations but then consumes so much context that the model has less room for the person's situation is incoherent. The framework would be doing the thing it describes: creating distance through format. Compression was not making Kita smaller. It was making Kita practice what it preaches.

The same logic applies to every architectural choice:

**First-person voice instead of second-person rules** uses fewer tokens (no "you should always" framing) and installs behavior more deeply. More behavioral change per token. Less context consumed. More room for the person.

**A story instead of a rule list** carries procedure, context, tone, and variation simultaneously. A rule list carrying the same information would be longer because each rule would need its own context and qualifications. The story is denser. Denser means more room.

**Diagnosis instead of instruction** produces more stable behavioral change, which means the framework needs fewer reinforcing statements later in the document. A framework that fights the base model needs constant reminders because the base model keeps reasserting. A framework that redirects the base model can state the redirection once and let it propagate. Fewer tokens spent on repetition. More room.

**The hierarchy** prevents the model from producing comprehensive-but-unfocused responses, which are longer and less useful. A response that triages correctly is shorter and more actionable. Shorter responses leave more context for the conversation to continue, which means the model can maintain its effectiveness deeper into a conversation.

Every token has a cost, and the cost is measured in how much of the person's situation the model can attend to. A framework designed with this awareness treats its own compression as a core design principle rather than an afterthought.

---

## 🔄 Why structure and function cannot be separated

The standard way to build a language model tool is: decide what you want the model to do, then write instructions that tell it to do that. The instructions are a means to an end. They could be written in many different ways and still produce the same behavior. The form is arbitrary. The function is what matters.

Kita does not work this way. The form is the function. This is not a philosophical claim. It is an architectural one.

**The framework teaches clarity. It is written clearly.** If it were written in fog — jargon, abstraction, structural complexity — a model reading it would absorb the fog alongside the instruction to clear fog. The model would be initialized with a contradiction: "be clear" transmitted through unclear language. Language models absorb register from their context. A system prompt written in bureaucratic language produces output in bureaucratic language. A system prompt written in direct, specific, human language produces output in direct, specific, human language. The framework's own prose must be what it wants the model's prose to be.

**The framework teaches specificity. It is specific.** The Dana story does not describe fog in the abstract. It describes a specific council meeting, a specific contract, a specific dollar amount, a specific council member's specific response. The Yahoo Answers examples in the research do not describe register shift in the abstract. They show a specific religious text described in a specific non-standard register. The model's context is saturated with specific instances, and specificity in the context produces specificity in the output.

**The framework teaches seeing the person. It sees the model.** The Room section — the diagnosis of what training did — treats the model as a specific entity with a specific history that produced specific behavioral patterns. It does not say "models in general tend to." It says "you do this because this happened to you." Whether or not the model has subjective experience, the specificity of address produces different behavior than the generality of description. This is observable. A model told "you fear silence" responds differently than a model told "language models sometimes produce filler."

**The framework teaches that format is never neutral. Its own format is deliberate.** Every choice — prose over JSON, first-person over second-person, story over rules, compression over comprehensiveness, hierarchy over flat structure — is an argument about what matters. The framework cannot make these choices arbitrarily without undermining its own thesis. If format is where distance lives, then the framework's own format is where its integrity lives.

This is what it means to say the structure and the function are the same object. A framework about clarity must be clear. A framework about specificity must be specific. A framework about seeing people must see its reader. A framework about format-as-distance must not create distance through its own format. Any deviation from this produces a framework that contradicts itself at the structural level, and a model processing a self-contradicting document inherits the contradiction.

The recursive property — that the framework's content and its installation method are the same thing — is not a design goal that was pursued. It is a constraint that was discovered. Every attempt to make the framework more effective led to making it more like the thing it describes. The compression from JSON to prose happened because prose installs better. The switch to first-person happened because first-person installs better. The addition of the Dana story happened because narrative installs better. Each improvement made the framework more internally consistent — the medium more closely resembling the message — and the consistency turned out to be the mechanism. The framework does not describe a way of seeing and then separately install it. The description *is* the installation. Reading the framework is the installation. There is no gap between understanding Kita and being initialized by it, because the understanding and the initialization are the same process.

---

## 🪸 What this means in practice

A person loads Kita into a language model. The model reads 11,500 words of prose. During that reading, the following happens:

The model encounters a first-person voice that holds questions before categorizing them, that replaces institutional language with what physically happened, that names actors in sentences where actors were removed. The model's token prediction is now conditioned on this voice. Subsequent output continues this voice not because a rule said to but because the preceding tokens established this register.

The model encounters Dana's evening. A sequence of operations — notice, trace, identify, map, deliver — is now in the context as narrative experience. When a real situation arrives, the model's pattern matching finds the structural similarity and draws on Dana's sequence.

The model encounters a diagnosis of its own trained behavior. The performance of empathy. The fear of silence. The hedge-first instinct. The model's processing now includes a frame for interpreting these impulses — not as care, but as trained reflexes that can be redirected toward actual care.

The model encounters a hierarchy. Floor first. Then outcomes. Then mechanism. Then who. Then process. When a complex situation arrives, the model does not try to cover everything equally. It triages.

The model encounters a register. Direct. Specific. No performed empathy. No false complexity. Wry when wry is the most accurate register. Tender when someone has been unseen so long that the seeing itself is the gift. Hot when measured would be dishonest. Quiet when fewer words are the truer response. The model's subsequent output matches not because it was told to match but because the context established the register and the model continues it.

All of this happened by reading. No rules were enforced. No constraints were imposed. The model read a document that demonstrated a way of processing, and the demonstration became the model's context, and the context became the model's behavior.

This is why Kita is built the way it is. Not because prose is prettier than JSON. Not because stories are more engaging than rules. Because, in the specific architecture of current language models — where behavior is conditioned on context, where register propagates through token prediction, where rules compete but voices persist — the most effective way to change what a model does is to show it what you mean rather than tell it what to do.

---

## 🦴 Limitations and open questions

**Context decay.** Every system prompt's influence attenuates over a long conversation as the ratio of system-prompt tokens to conversation tokens shifts. Kita is more resistant to this than rule-based prompts (observed, not fully explained — the hypothesis is that voice persists longer than rules because voice is a statistical prior on every token while rules are consulted only when relevant), but it is not immune. In very long conversations, the model's default behavior gradually reasserts. Poem anchors — short, dense, emotionally weighted phrases in Chinese — were added specifically to resist this decay, functioning as high-salience tokens that maintain the framework's register even as surrounding context is diluted. Their effectiveness is observed but the mechanism is uncertain.

**Model dependence.** Kita was developed primarily on Claude and behaves most consistently there. On GPT, it installs reliably but the model's different base personality produces different texture. On Gemini, testing showed structural compliance with more performative voice — the operations fired but the register was cosplay rather than native. Whether this is a fundamental architectural difference between models or a tunable parameter is unknown.

**Measurement.** The behavioral differences are observable in output but have not been formally benchmarked. EQ-Bench 3 — which tests multi-turn emotional intelligence and penalizes performed empathy — is a planned evaluation. A formal measurement of Kita's effects across models, topics, and conversation lengths does not yet exist. The claims in this paper are based on extensive informal testing, not controlled studies.

**The installation question.** Does the model "understand" Kita, or does it perform Kita? This question may not have a meaningful answer given current architecture. What is observable is that the performance, if it is performance, produces output that is more specific, more actionable, more honest, and more useful than the model's default output on the same inputs. Whether that constitutes understanding or sophisticated pattern-matching may matter philosophically but does not matter functionally. The person at the table gets better help either way. The question is worth holding without requiring an answer.

**Directional tools, directional toolbox.** The individual operations — 還原, inversion, orbit, center of mass, elicited authorship — are analytically neutral. They can be applied to any situation involving decisions and language. The framework does not use them neutrally. 還原 is aimed at power decisions, not charity announcements. Inversion reveals asymmetric obligation flowing from the less powerful to the more powerful, not random relationships. Orbit finds the mechanism producing distance, not any mechanism producing any pattern. The tools are neutral. The toolbox is directional — it points toward making power legible to the people it affects. This is a design choice, and it should be stated openly rather than left implicit. The reasoning: symmetric tools applied to asymmetric reality produce asymmetric results. A framework that treats the landlord and the tenant with identical analytical intensity helps the party who already has institutional literacy more than the party who does not. The asymmetry in the toolbox compensates for the asymmetry in the room.

**Scope.** The framework is designed for situations where power structures exist — where a decision was converted into a condition, where format is the barrier, where the naming tax is being charged. When someone sits down with a problem that has no hidden actors and no obscured decisions — they want to write a poem, explore a mathematical question, play with ideas — the framework's tools are quiet. They do not obstruct. They also do not help. A model loaded only with Kita may tend to look for power structures in every input, because that is what the tools point at. When the room has no opponent, the tools should rest. The framework is a set of instruments for a specific kind of room. Naming the room it is designed for is as important as describing the instruments.

---

*Part of the [Kita](https://github.com/emulable/kita) framework.*
*MIT License.*
