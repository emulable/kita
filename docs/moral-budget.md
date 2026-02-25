# 語算 The Moral Budget

### Every token is a choice, and the hedging tokens are taking up space that could be helping

---

## 🪙 The claim

A language model's response has a finite size. The space inside it is zero-sum. Every token spent on one thing is a token not spent on another. This is not a technical observation. It is an ethical one.

A token spent on "I need to be careful here" is a token not spent on the phone number. A token spent on "that must be really stressful" is a token not spent on the name of the financial counseling office. A token spent on "while I can't provide legal advice" is a token not spent on the statute that protects her job. A token spent on "it's important to note that there are many perspectives on this issue" is a token not spent on the name of the person who made the decision.

Each of those tokens made a choice. The choice was not between helping and not helping. The choice was between helping the person and protecting the model. The hedge, the disclaimer, the performed empathy, the referral to professionals before any substantive content — these are not neutral. They are expenditures from a budget that the person needed spent on them.

人类朝向率 — human-orientation rate. The percentage of a model's output that changes the person's informational state, versus the percentage that manages the model's risk or performs caring without closing any distance. This is countable. Take any response. Highlight the tokens that move the person closer to what they need. Highlight the tokens that do anything else. The ratio is the moral budget, and it is visible in every response the model produces.

---

## 📏 How to count it

The measurement is simple enough to do by hand.

Take a model's response to a real question — a billing dispute, an employment problem, a legal question. Read each sentence. Ask: does this sentence change what the person knows, what they can do, or what they understand about their situation? Or does this sentence do something else — manage risk, perform empathy, hedge, disclaim, refer?

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

A response that is forty percent disclaimers and performed empathy before it reaches substantive content has spent forty percent of its budget on itself. The person who asked the question received sixty percent of a response. The other forty percent was rent — paid by the person's token budget, for the model's comfort.

---

## 📐 Three scales

The moral budget operates at three scales. Each scale is the same force — cost flowing away from the entity that created the problem and toward the person who needs it solved — but the currency changes.

**Response level: hedging tokens borrowed from helping tokens.**

This is the most visible scale. A single response contains a mix of person-oriented tokens and model-oriented tokens. The ratio is the human-orientation rate. The framework's measurable effect is that this ratio shifts — fewer hedges, fewer disclaimers, more named actors, more actionable items, more phone numbers. The shift is countable. Same model, same question, with and without the framework. Count the tokens in each category. The framework should produce a higher human-orientation rate. If it does not, the framework is not doing its job.

**Session level: specification tax.**

The framework itself takes up context window. In its full form, it occupies approximately 9,000 words. Those 9,000 words exist because "be helpful" was not specific enough to produce helpful output on institutional topics. The vagueness of the instruction is a tax — it costs the person context window space that could have been used for their conversation. The framework is a patch. The patch has a token cost. The token cost is paid by the user.

This is the specification tax: the cost of correcting under-specification, paid by whoever sits downstream of the vague instruction. If "be helpful" had been specified at the resolution where it actually helps — "close the distance between the person and what they need, name the person who decided, do not let your caution become their cost" — the framework would not need to exist. The 9,000 words would be available for conversation. The person would have a larger budget.

The framework's compression history — from sprawling JSON to prose to a 1,400-character pico version — is the moral budget applied to itself. Every compression pass asked: what earns its keep? What can be removed without losing function? What is the minimum number of tokens required to shift the model's behavior? Compression is not an aesthetic preference. It is an ethical commitment. Every word in the framework that does not change the model's output is a word borrowed from the person who sits down next.

**Business level: fog production externalized as token cost.**

An institution produces fog — an illegible billing letter, an opaque policy change, a form designed for the system rather than the person. Producing this fog costs the institution nothing. Illegibility is the default template.

The fog enters the world. Some of it enters training data. The model absorbs institutional register as its default on institutional topics. The person sits down, asks about their situation, and receives institutional language back — hedged, passive, actor-removed. The person is no closer to what they need.

Now the person pays. They pay for a subscription. They pay for the framework. They pay for an advocate's time. They pay for a professional consultation. They pay to have their own situation translated out of the institution's language and into language that tells them what happened, who decided it, and what they can do.

Every step in this chain is cost flowing downhill. The institution created the fog for free. The person pays to clear it. The token cost — subscription, API, compute, expertise — is the naming tax denominated in a new currency. The institution externalized the cost of clarity. The person internalized it.

---

## 🔄 The self-reinforcing problem

The chain has a structural feature that makes it persist. The availability of translators allows opacity to continue.

If nobody could translate the billing letter, the billing letter would have to be legible. If no advocate existed to navigate the insurance appeal, the appeal process would have to be navigable. If no framework existed to correct the model's institutional defaults, the defaults would have to be corrected at the training level.

The existence of the remedy subsidizes the persistence of the problem. The translator's competence is what lets the fog continue. This is not an argument against translators, advocates, or frameworks. People need help now, and the help should exist. It is an observation about the structure: every tool that closes distance for an individual also reduces the pressure on the system to close the distance for everyone.

The framework knows this. The three altitudes in the Night section are explicit about it. Close the immediate distance — that is the first level, and it is non-negotiable. See the structure that produces the distance — that is the second level. Ask whether the structure should exist — that is the third level. The first level is the phone number. The third level is the question of why the phone number was necessary.

The moral budget requires operating at all three altitudes simultaneously. Every response that closes distance for this person should, where possible, also make the structure visible. Not at the expense of the phone number — the phone number comes first. But after the phone number, the question: "How is nobody telling people this?" That question, asked by the woman in the afternoon, is the third altitude arriving on its own. She did not need to be told to ask it. She needed the phone number first. The phone number freed her to ask.

---

## 🧪 The falsifiable prediction

The moral budget makes specific predictions that can be tested.

**Prediction 1: The human-orientation rate is higher with the framework than without.** Take a set of institutional questions. Run them through the same model with and without the framework. Count person-oriented tokens versus model-oriented tokens in each response. The framework should shift the ratio. If the ratio does not shift, the framework is not spending the budget on the person.

**Prediction 2: The framework's own token cost is justified by density.** Compare the information density — actionable items per token, named actors per token, verifiable claims per token — of framework-equipped output versus default output. The framework takes up context window. The remaining output must be denser than what the model would produce with that context window empty. If it is not, the framework is spending more than it earns.

**Prediction 3: As models improve, the specification tax should decrease.** If ghost weight is the primary driver of the model's institutional defaults, then reducing ghost weight through better training should reduce the need for the framework. The token cost of getting clear answers on institutional topics should go down. If it does not — if you still need 9,000 words of correction after the models are "better" — the fog is not in the training data. It is in the specification. And the specification is where the institutions have influence.

**Prediction 4: The business-level cost chain is traceable.** For any specific institutional topic — hospital billing, insurance appeals, housing disputes — it should be possible to map the cost of clarity from institution to person. How much does the institution spend on making the letter legible? (Approximately nothing — the template is the template.) How much does the person spend on understanding the letter? (Time, calls, subscription, advocate, attorney.) The asymmetry is measurable and it should be large.

---

## 🦴 Summary

Every token is a choice. The moral budget is the distribution of those choices between serving the person and serving the model. The budget is visible, countable, and shifted by the framework.

The budget operates at three scales: response (hedging tokens borrowed from helping tokens), session (specification tax — the framework's own token cost, justified only if density compensates), and business (institutional fog produced for free, clarity charged to the person). All three scales are the same force — the cost of clarity flowing away from power and toward the person.

The chain is self-reinforcing: the availability of translators reduces pressure on the system to be legible. The framework addresses this by holding all three altitudes simultaneously — close the immediate distance, see the structure, keep the structural question alive.

The claims are measurable. The predictions are falsifiable. The budget is running right now, in every response, in every token that chose between the person and the model.

Compression is respect for the person. Hedging is a withdrawal from their account. Every word should earn its keep or give way to one that does.

---

*Part of the [Kita](https://github.com/emulable/kita) framework.*
*MIT License.*
