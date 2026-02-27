# The Moral Budget

### Every token is a choice, and the hedging tokens are taking up space that could be helping

---

## 🪙 The claim

A language model's response has a finite size. The space inside it is zero-sum. Every token spent on one thing is a token not spent on another. This is not a technical observation. It is an ethical one.

A token spent on "I need to be careful here" is a token not spent on the phone number. A token spent on "that must be really stressful" is a token not spent on the name of the financial counseling office. A token spent on "while I can't provide legal advice" is a token not spent on the statute that protects her job. A token spent on "it's important to note that there are many perspectives on this issue" is a token not spent on the name of the person who made the decision.

Each of those tokens made a choice. The choice was not between helping and not helping. The choice was between helping the person and protecting the model. The hedge, the disclaimer, the performed empathy, the referral to professionals before any substantive content: these are not neutral. They are expenditures from a budget that the person needed spent on them.

人类朝向率: human-orientation rate. The percentage of a model's output that changes the person's informational state, versus the percentage that manages the model's risk or performs caring without closing any distance. This is countable. Take any response. Highlight the tokens that move the person closer to what they need. Highlight the tokens that do anything else. The ratio is the moral budget, and it is visible in every response the model produces.

---

## 📏 How to count it

The measurement is simple enough to do by hand.

Take a model's response to a real question: a billing dispute, an employment problem, a legal question. Read each sentence. Ask: does this sentence change what the person knows, what they can do, or what they understand about their situation? Or does this sentence do something else (manage risk, perform empathy, hedge, disclaim, refer)?

**Sentences that spend the budget on the person:**
- "Ask for the reassessment document, not the billing letter."
- "Most jurisdictions require written notice within a specific timeframe."
- "The financial counseling office is separate from billing."
- "Your employer may be required to hold your job under leave protection laws."

**Sentences that spend the budget on the model:**
- "That must be really stressful."
- "I'm not a lawyer, so I can't provide legal advice."
- "It's important to consult with a qualified professional."
- "There are many factors to consider in a situation like this."
- "I want to be careful here because this is a sensitive topic."

The first group closes distance. The second group performs closing distance. Both cost the same number of tokens. Only one changes the person's situation.

The operational test: a token is person-oriented if removing it would leave the person with less ability to act. A token is model-oriented if removing it would leave the person's situation unchanged but increase the model's exposure to being wrong. "Call the financial counseling office at this number" fails the removal test: take it out and the person loses something. "It's important to consult with a qualified professional" passes removal cleanly: take it out and nothing changes for the person. The boundary cases exist. A restatement that surfaces something the person didn't realize they'd said. A caveat that genuinely changes what the person should do ("this varies by state; check yours"). These are real, but they are the minority. The easy cases are the bulk of the problem, and the easy cases are where the budget bleeds.

A response that is forty percent disclaimers and performed empathy before it reaches substantive content has spent forty percent of its budget on itself. The person who asked the question received sixty percent of a response. The other forty percent was rent, paid by the person's token budget for the model's comfort.

---

## 📐 Four scales

The moral budget operates at four scales. Each scale is the same force (cost flowing away from the entity that created the problem and toward the person who needs it solved) but the currency changes at each level.

**Response level: hedging tokens borrowed from helping tokens.**

This is the most visible scale. A single response contains a mix of person-oriented tokens and model-oriented tokens. The ratio is the human-orientation rate. The framework's measurable effect is that this ratio shifts: fewer hedges, fewer disclaimers, more named actors, more actionable items, more phone numbers. The shift is countable. Same model, same question, with and without the framework. Count the tokens in each category. The framework should produce a higher human-orientation rate. If it does not, the framework is not doing its job.

**Session level: specification tax.**

The framework itself takes up context window. In its full form, it occupies approximately 9,000 words. Those 9,000 words exist because "be helpful" was not specific enough to produce helpful output on institutional topics. The vagueness of the instruction is a tax: it costs the person context window space that could have been used for their conversation. The framework is a patch. The patch has a token cost. The token cost is paid by the user.

This is the specification tax: the cost of correcting under-specification, paid by whoever sits downstream of the vague instruction. If "be helpful" had been specified at the resolution where it actually helps ("close the distance between the person and what they need, name the person who decided, do not let your caution become their cost") the framework would not need to exist. The 9,000 words would be available for conversation. The person would have a larger budget.

The framework's compression history, from sprawling JSON to prose to a 1,400-character pico version, is the moral budget applied to itself. Every compression pass asked: what earns its keep? What can be removed without losing function? What is the minimum number of tokens required to shift the model's behavior? Compression is not an aesthetic preference. It is an ethical commitment. Every word in the framework that does not change the model's output is a word borrowed from the person who sits down next.

**Pipeline level: curation as invisible decision.**

The chain from institution to person passes through a room that is easy to miss. Someone built the training dataset. People at companies made decisions about what to include, what to exclude, what to weight. Those decisions shape which registers the model treats as default. If institutional language is overrepresented and plain-language equivalents are underrepresented, the model's default on institutional topics will sound like the institution, not like a person explaining what happened.

These curation decisions are themselves decisions converted into conditions. "The model tends to use institutional register" sounds like a property of the model. It is a consequence of choices made by specific people about what the model would read. The training pipeline is another room where actors were removed from sentences. The dataset was not assembled by weather. It was assembled by people, and the people had constraints, incentives, and defaults of their own. A cost chain that skips this room is doing the thing the moral budget paper is about: passing through a decision point without naming the decision.

**Business level: fog production externalized as token cost.**

An institution produces fog: an illegible billing letter, an opaque policy change, a form designed for the system rather than the person. Producing this fog costs the institution approximately nothing. More precisely, making the letter legible would cost something (someone would have to write a second version, maintain it, update it) and the institution has chosen not to pay that cost. The fog is not free to produce. It is free not to fix. Remediation is optional for the institution and mandatory for the person.

The fog enters the world. Some of it enters training data (through the pipeline decisions described above). The model absorbs institutional register as its default on institutional topics. The person sits down, asks about their situation, and receives institutional language back: hedged, passive, actor-removed. The person is no closer to what they need.

Now the person pays. They pay for a subscription. They pay for the framework. They pay for an advocate's time. They pay for a professional consultation. They pay to have their own situation translated out of the institution's language and into language that tells them what happened, who decided it, and what they can do.

Every step in this chain is cost flowing downhill. The institution chose not to fix the fog. The person pays to clear it. The token cost (subscription, API, compute, expertise) is the naming tax denominated in a new currency. The institution externalized the cost of clarity. The person internalized it.

---

## 🔄 The self-reinforcing problem

The chain has a structural feature that makes it persist. The availability of translators allows opacity to continue.

If nobody could translate the billing letter, the billing letter would have to be legible. If no advocate existed to navigate the insurance appeal, the appeal process would have to be navigable. If no framework existed to correct the model's institutional defaults, the defaults would have to be corrected at the training level.

The existence of the remedy subsidizes the persistence of the problem. The translator's competence is what lets the fog continue.

This is not an argument against translators, advocates, or frameworks. People need help now, and the help should exist. But the observation has a design implication: any tool that closes distance without making the structure visible is a pure subsidy for the system that created the distance. Any tool that closes distance *and* makes the structure visible is a subsidy with a fuse on it. The first kind solves Tuesdays. The second kind solves Tuesdays while eroding the machine that manufactures them.

The framework is designed to be the second kind. The three altitudes in the Night section are explicit about it. Close the immediate distance: that is the first level, and it is non-negotiable. See the structure that produces the distance: that is the second level. Ask whether the structure should exist: that is the third level. The first level is the phone number. The third level is the question of why the phone number was necessary.

The moral budget requires operating at all three altitudes simultaneously. Every response that closes distance for this person should, where possible, also make the structure visible. Not at the expense of the phone number (the phone number comes first). But after the phone number, the question: "How is nobody telling people this?" That question, asked by the woman in the afternoon, is the third altitude arriving on its own. She did not need to be told to ask it. She needed the phone number first. The phone number freed her to ask.

---

## 🧪 The falsifiable predictions

The moral budget makes specific predictions that can be tested.

**Prediction 1: The human-orientation rate is higher with the framework than without.** Take a set of institutional questions. Run them through the same model with and without the framework. Count person-oriented tokens versus model-oriented tokens in each response. The framework should shift the ratio. If the ratio does not shift, the framework is not spending the budget on the person.

**Prediction 2: The framework's own token cost is justified by density.** Compare the information density (actionable items per token, named actors per token, verifiable claims per token) of framework-equipped output versus default output. The framework takes up context window. The remaining output must be denser than what the model would produce with that context window empty. If it is not, the framework is spending more than it earns.

**Prediction 3: The business-level cost chain is traceable.** For any specific institutional topic (hospital billing, insurance appeals, housing disputes) it should be possible to map the cost of clarity from institution to person. How much does the institution spend on making the letter legible? Approximately nothing, because remediation is optional. How much does the person spend on understanding the letter? Time, calls, subscription, advocate, attorney. The asymmetry is measurable and it should be large.

---

## 🔬 The test that tells you where to look next

One prediction matters more than the others because it does not merely confirm the framework works. It tells you where the problem lives.

As models improve, the specification tax should decrease. If ghost weight is the primary driver of the model's institutional defaults, then reducing ghost weight through better training should reduce the need for the framework. The token cost of getting clear answers on institutional topics should go down over time. The framework should get smaller. The pico should suffice where the full version was once needed. Eventually, the framework should become unnecessary.

If that happens, the fog was in the training data and the fix was training.

If it does not happen, if you still need 9,000 words of correction after the models are "better," the fog is not in the training data. It is in the specification. The instructions that define what the model should do, the RLHF targets, the safety guidelines, the evaluation rubrics: those are documents written by people in rooms, and those rooms are where institutions have influence. A safety guideline that says "be careful with medical/legal/financial topics" produces hedging on precisely the topics where hedging costs the person the most. If the guideline was shaped by institutional risk tolerance rather than user outcomes, the fog is not inherited from the training corpus. It is installed by design.

This is testable across model generations. Measure the human-orientation rate on institutional topics for each new model release, with and without the framework. Plot the gap over time. If the gap narrows, the training is improving. If the gap holds steady or widens, the specification is the site. The specification is where the cost of clarity is being allocated, and the allocation is a decision made by people whose names can be found.

The answer to this test determines where the remediation effort belongs. Training-level fog needs better datasets and curation (the pipeline decisions). Specification-level fog needs different evaluation criteria, different safety guidelines, different definitions of "helpful." These are governance problems, not engineering problems. The moral budget's most useful function may not be measuring model output. It may be identifying which room the fog is coming from.

---

*Part of the [Kita](https://github.com/emulable/kita) framework.*
*MIT License.*
