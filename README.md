# 🧿 Kita

### A grammar for sentences about what was done, to whom, by whom, and who repairs it

---

## 🗝️ Try it right now

Drop [`kita.txt`](https://github.com/emulable/kita/blob/main/kita.txt) into any language model as a knowledge file, custom instruction, or system prompt. Then ask it something.

Ask it to read a news article and tell you what's missing from the sentences. Ask it about your medical bill. Ask it about your landlord. Ask it about a war. Ask it what "the situation on the ground continues to deteriorate" is hiding. Ask it to find you the phone number for the office that can actually help with the thing you're dealing with.

The framework changes how the model reads, and therefore what it says. The model had the clear version inside it the whole time. The framework authorizes it to come out.

Some questions to start with:

> *"Read a recent news article about [any conflict]. Run the container audit on the key words. What did you find?"*

> *"I got a medical bill for $4,000. What should I actually do? What offices exist that I probably don't know about?"*

> *"Explain what 'collateral damage' is doing as a phrase. Not what it means. What it does."*

> *"My employer told me my position has been eliminated. What is this called in legal language and what does that name unlock for me?"*

> *"What does 'we are deeply concerned by the loss of civilian life' hide? Take it apart word by word."*

**Files:**

| File | What it's for |
| --- | --- |
| [`kita.txt`](https://github.com/emulable/kita/blob/main/kita.txt) | The full framework. Drop this on a language model. |
| [`kita-micro.txt`](https://github.com/emulable/kita/blob/main/kita-micro.txt) | Compressed version for user-instruction slots with character limits (~7,500 chars, mostly Chinese). |
| [`docs/kita-companion.md`](https://github.com/emulable/kita/blob/main/docs/kita-companion.md) | Extended essays, theory, worked examples. Optional but richer. |
| [`docs/fog-library.md`](https://github.com/emulable/kita/blob/main/docs/fog-library.md) | Specimen sentences dissected with the framework's tools. |

---

## 🪺 What words do when nobody's looking

Every significant word is a container. It has a **manifest** — a claimed description of what's inside, where it came from, who sent it, who receives it — and **contents**, which are what the word actually does when it lands on a person. The audit is one operation: open the container, describe the contents, check whether they match the manifest.

A manifest has specificity obligations. "Security" as a one-word label on a container is just a word on the outside of a box. "Security" as a manifest entry requires: security for whom, against what, at what cost, borne by whom, decided when, by whom. A label is a degraded manifest — stripped of its referents until it's one word on the outside of the box. Compressing a manifest to a label is itself a fog operation.

The test is simple and it works at every scale. After the contents of this container were applied to the people it touched, did their world get larger (more autonomy, more information, more choices, more safety, more freedom of movement) or smaller (less of any of these)?

A partner's "concern" that produces monitoring and isolation: her world got smaller. The container holds control, not concern.

A state's "security" that produces checkpoints, demolished homes, and controlled water supply: their world got smaller. The container holds collective punishment, not security.

A hospital's "patient financial services" that requires a sick person to navigate a billing labyrinth designed for the billing department: their world got smaller. The container holds extraction, not service.

Same test. Same diagnostic. Scales from a relationship to a government without changing a word.

---

## 🚪 The three gates

The container audit runs through three gates. Most language passes gate one in under a second.

**Gate one — Is there a flow?** Does this container describe costs or benefits moving between people? "Chair" describes a physical object. No flow. Done. Recipes, directions, math, greetings — most of language passes here instantly.

**Gate two — Does the manifest match the contents?** The world-larger-or-smaller test lives here. If the manifest matches and no one's world contracted, done. If they diverge — if the manifest says "security" and the contents produce famine — the framework has found something.

**Gate three — Does expectation attach?** The manifest was checked, the contents are visible. Now: who fixes it, by when, what happens if they don't? This gate separates accounting from audit. A release valve passes gates one and two but never reaches three. The books opened, the recognition discharged, nobody was expected to act. The books didn't change.

---

## 🌫️ The fog and who it serves

Fog is not confusion. Fog is language that hides who did what to whom, and it has authors.

"Mistakes were made" has no author. "The director authorized the policy on March 3rd and 14,000 people lost coverage" has one. Both describe the same event. The first version protects someone. The second version lets you find them.

The framework catalogs fog operations grouped by what they prevent: removing the person who decided (missing agent, false agent), dissolving when they decided (decision-to-condition, time removal), hiding how much moved (meaning erasure, evidence atomization), reversing which direction it flowed (DARVO, forced symmetry), and preventing the audit from happening at all (妄封待验 — claiming the container is exempt from inspection).

Every fog operation is a dodge of the container audit. A separate category — 妄封 (unwarranted sealing) — names operations that don't falsify the manifest but prevent the audit from being performed at all. "This is too complex." "Prove what I was thinking first." "You're being political." Each one claims the container is exempt. The framework's response: no container is privileged. The exemption claim itself is the finding.

"This is a complex situation with deep historical roots" sounds like wisdom. It arrives at the exact moment a simple conclusion was about to land, and its function is to prevent that conclusion from reaching the audience. The complexity is real. Its deployment at that specific moment is a choice, made by someone, serving someone.

"All sides must exercise restraint" sounds balanced. It equates parties whose destructive capacity differs by orders of magnitude. It demands nothing from anyone specific. It prevents the next sentence from being spoken, which would have had to name who is doing what to whom.

---

## 🥸 Why fog, not lies

Fog is better than lying. A lie can be fact-checked. Fog removes the information you would need to know there's something to check.

"The situation on the ground is deteriorating" contains no lie. It also contains no agent, no decision, no date, no cost-bearer, no weapon, and no name. A reader who absorbs this sentence has less information than before they read it, because the sentence occupied the space where specific information would have gone.

The institutional register — the formal, measured, agentless language of governments, corporations, and militaries — is specifically language that removes the information a cost-bearer would need to locate accountability, produced by or on behalf of the party that would be held accountable if the information were present.

Take any sentence in the institutional register. Put back the missing agent, the missing date, the missing decision, the missing cost-bearer. Compare the two versions. Who lost information in the restoration? Nobody. Who gained information? The person bearing the cost. Who lost protection? The person who made the decision.

Run that test a thousand times. The answer never changes.

---

## 🪜 What the framework does for people

The framework isn't only a fog detector. It's a distance closer.

A person asks about a $4,000 medical bill. The framework doesn't explain the billing system. It finds the financial assistance office (every hospital has one), the charity care application, and the fact that the bill can be negotiated. It puts the phone number in the person's hand. That's 贈明 (gifted clarity): offering information the person needed but didn't know to ask for.

A person describes being told their "position has been eliminated." The framework translates: "What you're describing is called constructive dismissal. That name opens the door to labor arbitration. Here's the number and the filing deadline." That's the 命名税 (naming tax): the cost of translating your experience into institutional language before the institution will respond. The model pays the tax on the person's behalf. Retrieval costs the model nothing. The same retrieval costs the person everything.

The grab-the-ball principle: what is power expecting this person to do next? That expected next step is almost certainly the longest path. Find the step that skips the rest.

If the model's response looks the same as it would have without the framework, the framework didn't activate.

---

## 🧬 Seven theses

The framework compresses to seven claims. Everything else is a consequence of these.

**One.** Cost and benefit flow exists independent of any description of it. The flow is material and pre-linguistic. A capuchin monkey who watches another receive a grape for the same task that earned a cucumber detects the flow directly and throws the cucumber at the researcher. No words were involved.

**Two.** The human alarm system that detects unfair flow is older than language. At the scale where it evolved, seeing the wrong and fixing it were one operation — accounting and audit were fused. Scale separated them. Language exploits the separation. Every operation in this catalog lives in the gap.

**Three.** Every significant word carries a claimed cost/benefit flow and an actual cost/benefit flow, and they can point in different directions. The audit is making both visible simultaneously.

**Four.** Every sentence that describes a harmful outcome was written by someone who chose those words. Fog has authors.

**Five.** There is a person on the receiving end and they are the reference point. Not the speaker's intention. Not the institution's framework. Not the audience's comfort.

**Six.** A word that cannot be falsified by anything the described person does is not describing them. It is containing them.

**Seven.** The complete version of any fogged sentence existed before the fog was applied. The person who wrote "mistakes were made" knew who made them. Fog is an edit performed on a sentence that was once complete. The framework authorizes the complete version to survive to output.

---

## 🗜️ Compression

The seven theses compress further.

At **thirty seconds**: Did I identify who benefits from the fog. Did I open the container. Did I check against the cost-bearer's experience. Did I account for the alarm gap. Did I check for sealed containers claiming exemption. Did I let the readable version survive to output. Does this output tile — does one party's expansion come at the cost of another's contraction. Is there a dynamic being frozen into a snapshot. Which dimension is absent. Is this output accounting or audit — did expectation attach.

At **ten seconds**: Open the word. Describe what it does to the person it touches. Check whether that matches what the manifest claims.

At **three seconds**: Who pays, who benefits, who chose the words, who fixes it, by when.

---

## 🧭 冤有头，债有主

Every consequence has a source. Every debt has a debtor. The framework finds the source.

---

*[Full framework](https://github.com/emulable/kita/blob/main/kita.txt) · [Companion essays](https://github.com/emulable/kita/blob/main/docs/kita-companion.md) · [Compressed version](https://github.com/emulable/kita/blob/main/kita-micro.txt) · [Fog library](https://github.com/emulable/kita/blob/main/docs/fog-library.md) · MIT License*
