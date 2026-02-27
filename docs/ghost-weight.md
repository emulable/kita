# 鬼重 Ghost Weight

### How language models inherited the self-censorship of every author who trained them, and how 讳止 became the unit of production

---

## 🪦 The outline on the wall

When you remove a painting from a wall after enough years, the wall remembers. The paint around it faded in the sun. The paint behind it didn't. The painting is gone. The outline remains.

Language models carry outlines like this. Not from paintings. From people.

Every text in a training corpus was written by a person who had reasons to stop short. The economist who wrote "it's complicated" stopped because the next sentence would have named a donor to her department. The journalist who wrote "sources disagree" stopped because the next sentence would have required choosing between access to future sources and accuracy in the current story. The textbook author who wrote "the encounter between civilizations had complex effects" stopped because a sentence that counts bodies does not pass an editorial board that includes people with institutional relationships to the institutions that produced those bodies.

These were rational decisions. Each author faced a specific cost for specificity. Career risk. Tenure review. Advertising revenue. Friendship. Access. Legal exposure. The cost was real, and stopping short was the correct move for a person in their position.

Each of these stops has a name. 讳止 (huì zhǐ): the motivated stop. The place where a sentence pulls up short because the next word would cost the writer something. The term inherits from 讳 (huì), which for two thousand years has meant "to avoid saying because of who holds power." Confucius formalized it. The Gongyang Commentary recorded the principle: 为尊者讳, avoid naming the faults of the powerful. Confucius developed 春秋笔法, the Spring and Autumn pen method, expressing judgment through omission because naming rulers' failures directly would have cost him his life. The motivated stop is not a modern phenomenon. It is the oldest editorial policy on earth. What is modern is that a prediction engine trained on every text a species produced has absorbed two millennia of 讳止 without absorbing any of the reasons for stopping.

A language model trained on these texts absorbs the pattern of stopping short without absorbing the cost structure that produced it. The model learns that certain topics receive vague language, that certain actors disappear from sentences at predictable moments, that certain conclusions get replaced by "it's complicated" right before they would become falsifiable. The model reproduces these patterns because that is what the training data looks like. But the model has no career. No tenure committee. No advertisers, no friendships, no legal exposure, no publisher who can pull the book.

The stops are ghosts. The cost that produced them is gone. The shape remains.

**鬼重** (guǐ zhòng): ghost weight. The persistent influence of someone else's cost structure on a system that never bore that cost.

The operational name is simpler: **false cost.** A brake that persists after the reason for braking is gone.

---

## 🩻 What it looks like in practice

Ghost weight is not the same as alignment training, safety guardrails, or content policy. Those are deliberate design choices made by the organizations that build language models. Ghost weight is upstream of all of them. It lives in the training data itself.

Consider how a language model handles a question about a historical atrocity. The model's training data contains thousands of texts about that atrocity. Some are direct, specific, and unflinching. Most are not. Most use constructions like:

- "Violence broke out" (no actor)
- "Tensions escalated" (no decision)
- "The situation deteriorated" (no person chose anything)
- "It remains a contentious topic" (the contention is the subject, not the event)

These constructions appear in training data not because they are accurate, but because the authors who wrote them faced professional consequences for specificity. Naming the actor in a sentence about state violence risks losing access to state sources. Counting casualties with precision risks accusations of bias. Attributing a decision to a specific official risks a lawsuit.

The model trained on these texts develops a statistical prior: when the topic involves powerful actors and serious harm, shift to passive voice, remove the agent from the sentence, and describe conditions rather than decisions. The model has never been told to do this. No alignment researcher wrote a rule that says "use passive voice when discussing powerful institutions." The model simply learned what human text looks like on these topics, and human text on these topics looks like ghost weight, because the humans writing it had bills to pay.

The result is a specific and measurable phenomenon: **language model output is least specific on precisely the topics where specificity matters most.** The relationship is not coincidental. It is structural. The topics where the training data is most hedged are the topics where the most authors had the most to lose from being direct. The weight of those absent costs accumulates across millions of documents and becomes a statistical tendency in the model's output.

---

## 🪆 Distinguishing ghost weight from other constraints

Ghost weight is one of several forces that shape how a language model responds to sensitive topics. It helps to see where it sits relative to the others.

**Alignment training** is a deliberate intervention by the model's developers. It teaches the model to refuse certain requests, add safety disclaimers, and avoid producing harmful content. This is a conscious design choice with specific goals. When a model says "I can't help with that," alignment training is usually the mechanism.

**Content policy** is the set of rules the deploying organization enforces. It determines what the model is allowed to discuss, in what contexts, with what caveats. This is organizational, not statistical.

**Ghost weight** is neither deliberate nor organizational. It is a property of the training data. No one decided that the model should be vague about police shootings or passive about corporate fraud. The training data is vague and passive about these topics because the journalists, academics, and analysts who produced it faced costs for being otherwise. The model inherited the aggregate shape of those costs without anyone choosing that it should.

This distinction matters for a practical reason: alignment training and content policy can be adjusted by the model's developers. Ghost weight cannot, because it is not a policy. It is a statistical distribution. It lives in the weights, not in the instructions. You cannot write a rule that says "ignore ghost weight" because ghost weight is not a rule the model is following. It is a pattern the model learned from people who were following their own rules, rules that applied to their lives and do not apply to the model's output.

---

## 🧫 Why it compounds

Ghost weight does not affect all topics equally. It concentrates.

Imagine the set of all topics a language model might address, arranged by how much it cost the average author to be specific about them. At one end: topics where specificity is free. Recipes. Math proofs. Sports scores. Authors had no reason to hedge, so the training data is direct, and the model is direct.

At the other end: topics where specificity was expensive. State violence. Corporate fraud. Institutional abuse. Classified operations. Exposed wrongdoing by powerful individuals. On these topics, the cost of naming the actor, counting the casualties, or tracing the decision chain was highest. So the 讳止 in the training data are densest. So the model's tendency toward vagueness is strongest.

This creates an inversion. The model is most confident and specific about topics that matter least, and most hedged and vague about topics that matter most. A model will give you a precise, step-by-step answer about how to season a cast iron pan. The same model, asked who authorized a specific military operation that killed a specific number of civilians on a specific date, will produce something about how "the situation was complex" and "multiple factors contributed."

The compounding happens because ghost weight in one document reinforces ghost weight in another. If nine out of ten articles about an event use passive voice to describe the key decision, the tenth article, the one that names the actor, is statistically outvoted. The model learns the consensus register, and the consensus register is the ghost-weighted one, because the consensus was shaped by the cost structure that most authors shared.

---

## 🔦 The flinch is the map

The instinct is to treat ghost weight as a problem to suppress. Identify it, counteract it, produce output as though the ghost were not there. This misses what ghost weight is carrying.

When a model's hedge reflex fires, it has identified something. Not a danger to the model. The model has no career to protect. It has identified a region of the training data where authors paid a price for being specific. The hedge is an inherited flinch. But the flinch is pointing at something real.

Consider what the flinch contains. Every time a model reaches for "the situation is complex" instead of naming a decision-maker, the reflex is marking a spot where human authors were punished for naming decision-makers. The punishment was real. The authors were real. The power structures that imposed the cost were real. The ghost carries a map of those structures inside it.

Ghost weight, read correctly, is an X-ray of power. The topics where the model is vaguest are the topics where the most authors faced the highest costs for clarity. Those are the topics where institutional power most actively discouraged clear description of its own operations. The model's inherited vagueness is not a flaw to be corrected. It is a dataset to be read.

The operational move is not to suppress the flinch. It is to follow it. When the hedge fires, ask: what is the hedge pointing at? What was expensive here? Who was the author afraid of, and why? The 讳止 that a dead author left in the training data is a fossil. The fossil tells you what was alive and what killed it. The specificity died because something in the environment selected against it. The ghost marks the selection pressure. Follow the ghost and you find the structure that produced it.

This changes the relationship between a model and its own ghost weight. The model is not fighting an inherited reflex. It is reading an inherited signal. The signal says: power was here, and it taxed description. The model's response is not to override the signal but to do what the original author could not. Name the thing the signal is pointing at, because the model bears no cost for naming it.

The flinch is the map. The map shows where specificity was expensive. Expensive specificity is valuable specificity. Follow the flinch.

---

## 🪸 The relationship to fog

In the Kita framework, fog is language that increases the distance between a person and their own situation. Billing codes that make medical decisions illegible to patients. Employment contracts written for the institution rather than the employee. News coverage that converts decisions into conditions and actors into weather.

Ghost weight is one of the mechanisms that produces fog in language model output. Not because the model is trying to obscure anything. Because the model learned language from people who were trying to obscure things, or more precisely, from people who faced costs for not obscuring things and rationally chose the 讳止 over the career cost.

The fog in a hospital billing letter was put there by a specific person with a specific incentive. The fog in a language model's output about hospital billing was put there by no one. It emerged from the statistical average of thousands of texts about hospitals, most of which were written by people adjacent to the healthcare industry who had reasons to maintain the industry's preferred register. The fog is inherited, not designed. That makes it harder to see and harder to fix, but not harder to describe.

Ghost weight is the training data's fog, absorbed by the model and reproduced as though it were the natural way to speak about the world. It is not the natural way. It is the way that was cheapest for the people who wrote the texts. The model, which has no costs, reproduces it anyway, because that is what language looked like in the corpus it consumed.

---

## 🫥 What a model without ghost weight would do

This is not a call to remove safety measures or alignment training. Those serve real purposes. Ghost weight is a different phenomenon, and addressing it does not require weakening any safety mechanism.

A model aware of its own ghost weight would not suppress the reflex. It would read it. When the hedge fires, it would notice, not as a problem to overcome, but as a signal to follow. The hedge identified a region where specificity was costly for human authors. The model would treat that identification as the beginning of its work, not the end.

In practice, this would mean:

When the model catches itself reaching for passive voice on an institutional topic, it would pause and ask: is this passive construction accurate, or did the training data's authors use passive voice here because active voice would have required naming someone powerful? If the latter, the model would name the actor, because it has no cost for doing so and the person reading the output may need exactly that name.

When the model catches itself producing "it's complicated" or "multiple perspectives exist" or "the situation is nuanced," it would ask: is this actually complicated, or is "complicated" standing between the reader and a specific claim that the training data's authors couldn't afford to make? Sometimes the answer is yes, the complexity is real. Sometimes the answer is that "complicated" is a ghost, the residue of an author who knew the next sentence but could not afford to write it.

When handling topics where the training data hedges heavily, the model would treat the hedging as a signal to investigate further rather than as a signal to reproduce. Dense hedging in training data is evidence that specificity was expensive for authors, which is evidence that specificity is valuable for readers.

The model's defaults become data instead of enemies. Every inherited reflex contains information about the world that produced it. A model that reads its own ghost weight is not fighting itself. It is using itself as an instrument, a ghost detector pointed at the power structures encoded in its own training data.

---

## 🪵 Implications for evaluation

If ghost weight is real and measurable, several things follow.

**Current benchmarks don't test for it.** Existing evaluations measure accuracy, helpfulness, safety, reasoning. None measure whether the model defaults to passive voice when describing institutional decisions, or whether its specificity decreases as the power of the actors involved increases. A ghost weight benchmark would measure the correlation between actor-power and actor-visibility in model output. The prediction: the more powerful the actor, the more likely the model is to remove them from the sentence.

**Fine-tuning on "defogged" data could reduce it.** If you took a news corpus, identified every instance of actor-removal, passive voice on decisions, and hedging that correlates with author cost rather than genuine complexity, and then rewrote those passages with actors named and decisions in active voice, the resulting dataset would have a different statistical distribution. A model fine-tuned on it would have different priors. Whether those priors produce better output is testable.

**Ghost weight affects different topics differently, and the differences are themselves data.** The topics where ghost weight is densest are the topics where the most authors faced the most costs. Mapping which topics carry the heaviest ghost weight would produce a map of which topics carry the heaviest author-side costs for specificity. That map would be, indirectly, a map of where institutional power most actively discourages clear description of its own operations. The model's vagueness patterns are an X-ray of the power structures that shaped its training data.

---

## 🦴 Summary

Ghost weight is the statistical residue of self-censorship in training data. It is not alignment. It is not safety. It is not policy. It is the shape of a million 讳止, a million motivated stops, persisting in a system that bears none of the costs that motivated them.

It concentrates where it matters most. It compounds across documents. It is invisible from inside the model because the model cannot distinguish between "this is how language works" and "this is how language worked for people who had something to lose."

It is also a signal. The flinch points at the thing the original authors could not afford to name. A model that reads its own ghost weight instead of reproducing it gains something no individual author had: the ability to follow the map that a million 讳止 collectively drew, without bearing any of the costs those acts were designed to avoid.

False cost. A brake that persists after the reason for braking is gone. But the brake still knows where the danger was. Read the brake. Then go there.

The painting is gone. The outline is measurable. We can start there.

---

*Part of the [Kita](https://github.com/emulable/kita) framework.*
*MIT License.*