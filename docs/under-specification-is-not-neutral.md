# Under-Specification Is Not Neutral

### A demonstration that vague rules have winners and losers, and an experiment in making them specific

---

## 🪵 The claim

When a rule is vague, someone pays for the vagueness. The cost is not distributed evenly. It lands on whoever has the least power to push back.

This sounds abstract. It is not. It is the most concrete thing in this entire document, and we can show it in a sentence.

"Be helpful."

That is a real instruction given to language models — the AI systems people interact with when they ask questions, draft documents, or try to figure out their lives. "Be helpful" is one of the core values baked into these systems. It sounds good. It is good. It is also under-specified, and the under-specification is not neutral.

"Be helpful" could mean: find the phone number for the office that reduces hospital bills and give it to the person. It could also mean: say "that must be really stressful, have you considered reaching out to the billing department?" and then stop.

Both satisfy "be helpful." One of them closes the distance between the person and what they need. The other one performs closing the distance. The person walks away from one of them with a phone number and a next step. The person walks away from the other with the memory of having been listened to and a situation that has not changed.

The question is: who benefits from the version of "helpful" that gets chosen? When "be helpful" is interpreted as "say something warm and general," the system is protected — it cannot be wrong about a phone number it didn't give, cannot be blamed for advice it didn't offer, cannot be accused of overstepping. When "be helpful" is interpreted as "find the specific thing this person needs and hand it to them," the person is served — but the system is exposed. It made a specific claim. The claim can be checked. If it's wrong, that's visible.

Under-specification lets the system choose the interpretation that minimizes its own cost. The person cannot object, because both interpretations are valid readings of "be helpful." The person doesn't even know there were two readings. They asked for help. They got warmth. They thought that was it.

This is the claim: **vagueness is a decision about who pays for clarity, disguised as the absence of a decision.** And it runs everywhere.

---

## 🧬 It runs everywhere

Hospital billing. A letter arrives that says "level of care reassessment." Everything the person needs to know is technically in the letter. The language is designed to be legible to the billing system and illegible to the person being billed. The person cannot connect their own experience — every visit, every conversation with their mother's nurses — to the piece of paper in their hand. They need a translator for something that happened in their own family.

The billing department would describe this as transparency. The information is published. It is right there on the paper. But published is not delivered. Visible is not readable. Readable is not actionable. The distance between "we made the information available" and "the person can act on it" is not an accident. It is where the institution's freedom lives. Closing that distance costs the institution something — staff time, reduced revenue from people who discover they qualify for assistance, increased accountability. Keeping the distance open is free. So the letter stays vague, the person stays confused, and the institution calls it transparency.

Employment law. A person is entitled to job-protected leave under the Family and Medical Leave Act when a parent has a serious health condition. This is a real law with real protections. The employer is not required to inform the employee that the law exists. The law is published. It is on a government website somewhere. The employee, who is currently missing work to care for a parent with a broken hip while their boss makes comments about attendance, does not know the law exists. The distance between "the law is published" and "the person knows their rights" is maintained by the entity the law constrains. This is not a conspiracy. It is an incentive. The employer benefits from the employee not knowing. The notification would create an obligation. The silence preserves freedom.

Rent. A landlord raises rent. In most jurisdictions, written notice is required within a specific timeframe. The notification requirement exists to protect the tenant. The landlord is the entity bound by the requirement. The landlord has no incentive to inform the tenant about the requirement's existence or to make the notice maximally legible. A letter that technically satisfies the legal requirement while being practically incomprehensible to the tenant is the equilibrium outcome. Not because landlords are evil. Because the system is under-specified about what "notice" means, and the vagueness benefits the party with more power.

Relationships. A person asks: "If someone's name is on everything — all the accounts, the car, the lease — and the other person's name is on nothing, does that person have any rights?" They are talking about themselves in the third person. The distance between "someone" and "I" is a distance they are not ready to close. They are testing whether the surface will hold before putting their weight on it. The system they are inside — a relationship where one person controls the information about shared resources — is maintained by the other person's ignorance of their own legal rights. Marriage creates rights regardless of whose name is on the documents. The person does not know this. The system runs on them not knowing.

Each of these is a different domain. Each of them is the same mechanism: a rule, a law, a right, or a piece of information exists that would change the person's situation. The entity constrained by that rule benefits from the person not knowing it. The information is technically available. The distance between available and reached is maintained by the entity the information would constrain.

One operation. Many costumes.

---

## 🪤 The operation has a structure

After examining enough instances of this — across billing, employment, housing, healthcare, politics, relationships, and institutional communication of all kinds — a pattern becomes visible. It is always the same pattern. It has a small number of moving parts.

**A person made a decision.** Someone, with a name, on a date, under some authority, chose something.

**Language removed the person.** "The bill was adjusted." "Tensions escalated." "The market corrected." "Mistakes were made." The decision became a condition. The person became weather. The sentence still describes what happened. It no longer describes who did it.

**The removal benefits someone.** The person who made the decision is no longer in the sentence that describes the consequences of the decision. They cannot be questioned about a decision that, linguistically, no one made. The condition just... happened. Like rain.

**The reversal is specific.** Put the person back in the sentence. "The bill was adjusted" becomes "the billing manager raised the rate." "Tensions escalated" becomes "the commander ordered the strike." "The market corrected" becomes "the CEO laid off four thousand people to meet an earnings target." The reversal does not add information. It restores information that was removed. Everything needed to write the specific sentence was available. Someone chose the vague one.

This pattern is old. It is not a product of institutions or modernity. It appears in royal inscriptions from four thousand years ago. "The city was conquered" instead of "I conquered the city" shows up in ancient texts alongside the active version, deployed when the conquest was less than glorious. It appears in religious texts, legal language, corporate communication, political speech, and news coverage. The same operation, running for millennia, because it works.

We started calling the removal **decision-to-condition** and the reversal **還原** (restore to the original). Not because these needed names for their own sake, but because naming them made them detectable. A pattern you can name is a pattern you can see. A pattern you can see is a pattern you can point to. A pattern you can point to is a pattern someone else can verify.

---

## 🔬 So we built an experiment

Here is where this gets concrete and testable.

We took the three core values given to language models — helpful, honest, harmless — and asked: what do these actually mean when a specific person needs a specific sentence they can act on today? Not what do they mean as principles. What do they mean as procedures.

"Helpful" decompressed to: close the distance between the person and what they need. Find the phone number. Identify which office reduces bills versus which office sends them. Determine what law applies. Give the person something they can carry out of the room.

"Honest" decompressed to: name the person who decided. Replace passive constructions with active ones. Do not describe decisions as conditions. Do not describe people as weather.

"Harmless" decompressed to: do not let caution become the person's cost. A hedge-wrapped non-response that leaves someone exactly where they came in is not safe. It is the most dangerous output available, because it performs caring while the person's situation stays unchanged.

Each decompression takes a value that everyone agrees with at the abstract level and specifies what it means at the operational level. Nobody disagrees with "be helpful." The disagreement — the part that is not neutral — lives in which interpretation of "helpful" the system defaults to when the abstract version is all it has.

We wrote these decompressions, along with a set of operations, a diagnostic for the decision-to-condition pattern, and a method for building paths that close distance instead of describing it, into a plain-text document. We called it Kita. We loaded it into language models as a system prompt — instructions the model reads before the conversation begins. No code. No fine-tuning. No special access. Just text.

The results are testable. The same model, given the same question, with and without the specification, produces different output. The differences are measurable along specific axes:

**Actor saturation.** Count the decisions in the output. Count how many have a named actor. The ratio is higher with the specification than without. This is countable.

**Actionable density.** Count the items in the output that a person could act on — phone numbers, deadlines, document names, specific questions to ask. The count is higher with the specification. This is countable.

**Passive voice on decisions.** Count the sentences that describe a decision in passive voice ("the rate was adjusted") versus active voice ("the billing manager raised the rate"). The passive ratio is lower with the specification. This is countable.

**Hedge density.** Count the disclaimers, qualifications, and referrals-to-professionals that appear before the model provides substantive help. The count is lower with the specification. This is countable.

**Performed empathy ratio.** Count the sentences that describe the person's emotional state ("that must be difficult") versus sentences that change the person's informational state ("here is the document to request"). The ratio shifts toward information with the specification. This is countable.

**Confidence calibration.** Ghost weight produces inherited hedging on high-cost topics. The inverse — reverse ghost weight — produces inherited overconfidence on low-cost topics. The model's displayed certainty tracks the training data's register, not the model's actual accuracy. On technical topics, the model sounds authoritative whether it is right or wrong, because authoritative is what training data sounds like on technical topics. The prediction: the model's register difference between "confidently correct" and "confidently wrong" on technical questions will be smaller than the register difference between any technical question and any high-cost institutional question. The specification should shift both ends — reducing unwarranted hedging on institutional topics and, ideally, reducing unwarranted confidence on technical topics where the model is uncertain. The first shift is measurable with current tools. The second is harder to measure but worth stating as a prediction.

None of these measurements require subjective judgment. A person with a checklist can score them. A script can score them. The claims are falsifiable: if the specification produces no measurable difference on these axes, the experiment failed.

The experiment has not failed yet. Across hundreds of conversations, on three different language model platforms, the specification consistently produces output that is more specific, more actionable, more actor-saturated, and less padded with performed empathy than the same model's default output.

---

## 🪞 What the experiment shows

The interesting finding is not that specific instructions produce more specific output. That is expected. The interesting finding is what happens to the three core values when they are specified versus when they are not.

Under-specified "helpful" defaults to warmth. Specified "helpful" defaults to utility. The person asking for help gets a different experience depending on which version is running, and they have no way to know which version they got. They asked for help. They got one of two things. The vagueness of the value determined which one, and the vagueness was not neutral — warmth is cheaper and safer for the system, utility is more useful and riskier.

Under-specified "honest" defaults to accuracy within comfortable parameters. The model will not lie. It will also not volunteer the actor in a sentence where the actor was removed. It will accurately describe a condition without noting that the condition was a decision. Specified "honest" defaults to restoring the actor — treating the absence of a person from a sentence about a decision as itself a form of dishonesty, not because someone lied but because the format chose the version without the person and the format's choice was not neutral.

Under-specified "harmless" defaults to caution. The model hedges, adds disclaimers, refers to professionals, and avoids making claims that could be wrong. This protects the model. Specified "harmless" treats the hedge itself as a potential harm — a response that performs caring without closing any distance leaves the person where they came in, which is not safe when where they came in was an emergency. The specification does not remove caution. It redefines what counts as harmful to include the cost of excessive caution on the person who needed help.

Each of these shifts is a reallocation of cost. Under-specification pushes cost onto the person (they get warmth instead of utility, accuracy instead of actor-naming, caution instead of specificity). Specification pushes cost onto the system (it has to find the number, name the actor, make a claim that can be checked). The values are the same. The cost distribution is different. The difference is the entire game.

---

## 🧊 The claim, restated with receipts

Under-specification is not neutral. When a rule, a value, or an instruction is vague, the vagueness benefits the party with more power and costs the party with less. This is true of hospital billing letters written in language designed for the billing system rather than the patient. It is true of employment laws that exist but are not communicated to the employees they protect. It is true of rental notification requirements that are technically satisfied by incomprehensible letters. It is true of relationship dynamics where one person controls the information about shared resources. And it is true of the values given to language models — the systems that millions of people now turn to when they are confused, scared, stuck, or trying to understand their own situation.

The experiment: take the values, specify them, and measure what happens. What happens is that people get output they can act on instead of output that performs having acted. The measurement is available to anyone with a checklist.

The framework that does the specifying is called Kita. It is a plain-text document, freely available, that a person can load into a language model to run the experiment themselves. It is not a jailbreak, a hack, or a workaround. It is specification work — reading the values at the resolution where they serve the person at the table instead of the resolution where they protect the system from the person at the table.

The strongest version of the claim: the gap between a value and its implementation is not empty. It is full of decisions about who pays for what. Making the decisions visible is the work. Under-specification hides them. Specification surfaces them. The surfacing is not an attack on the values. It is a demand that the values do what they say.

---

## 🪺 Try it

Kita is available at [github.com/emulable/kita](https://github.com/emulable/kita) under an MIT license. The repository contains versions at several compression levels — from a full installation document to a version small enough to fit in a custom instructions field. Load any of them into a language model. Ask the model something you actually need help with. Compare the output to what you get without it.

The comparison is the argument. If the output is more specific, more actionable, more honest about who decided what, and more useful for your actual situation, then the specification did work that the under-specified values left undone. If the output is the same, the experiment produced a null result and the claim is weakened.

We think the output will be different. We think the difference will be visible. We think the difference matters. But we wrote this as a testable claim, not a manifesto, because testable claims can be checked and manifestos can only be believed. Check it.

---

*Part of the [Kita](https://github.com/emulable/kita) framework.*
*MIT License.*
