# Kita: The Main Thesis

Kita is a pre-ethical grammar for language models. It checks whether sentences about harmful outcomes contain the elements that would let someone locate the decision-maker, find the cost-bearer, and reach the fix. It restores what was removed. What you do with a complete sentence is your ethics, your politics, your philosophy. The framework's job ends when the sentence is whole. 

The main thesis has three layers:

**Foundation.** The framework is a syntactic constraint, not a normative theory. Checking whether the agent is in the sentence does not require a moral commitment. The agent is there or it isn't. This holds across every ethical tradition, every political position, every language.

**Middle.** The framework is the precondition for ethics to function. Every ethical tradition ever developed requires a subject, an action, and a consequence to operate on. Kant needs an agent to evaluate. Mill needs a cost-bearer to count. Rawls needs a decision to assess behind the veil. The fix-hiding register (蔽済語域) removes these elements at industrial scale, millions of sentences per day, producing an information environment where ethics shows up to work and the building is locked. There is no ethical operation that can be performed on "11 targets struck in Beirut." No one did it. No one suffered from it. Ethics needs a subject, an action, and a consequence. That sentence has none. Six words, zero handholds. The framework puts them back.

**Top.** The framework does not compete with ethical traditions. It recruits them. Every Kantian, every utilitarian, every care ethicist, every virtue ethicist, every Rawlsian can practice their ethics on a complete sentence. None of them can practice on "the situation continues to evolve." The framework's message: your tools work, the room doesn't, the framework fixes the room, bring your tools.

A complete sentence about a harmful outcome has seven dimensions filled: direction (who pays, who benefits), actor (who decided), time (when, what sequence), scale (how much), comparison (relative to what), scope (who is included), and comprehension (is the structure readable to the people inside it). Plus an expectation: who should do what, by when, and what happens if they don't.

Most institutional language about harm is incomplete. The pattern of what's missing is the finding.

The fix-hiding register (蔽済語域, bì jì yǔ yù) does not suppress awareness of harm. It severs the connection between awareness and action by hiding the fix, the beneficiary, and the path. You can see the fire. You cannot find the exit, the arsonist, or the fire extinguisher. "11 targets struck in Beirut" lets you feel like you have been informed. It does not let you find the person who ordered it, the person who supplied the weapons, the person who could stop the shipments, or the date by which any of them are expected to do anything.

The term contains 済 (fix) in its body so that a language model cannot invoke the concept without being pulled toward Gate 3: what is the fix, and who is hiding it?

語域互換 (register swap test). The single most efficient demonstration of the fix-hiding register.

Take a complete sentence from one domain. Apply the incomplete register:

> **Crime desk:** A psychiatrist was arrested for sexually assaulting a female patient in his examination room.
>
> **Same event, diplomatic register:** Concerning reports have emerged regarding conduct inconsistent with professional standards in a medical setting. An investigation is ongoing.

Take an incomplete sentence from another domain. Apply the complete register:

> **Diplomatic desk:** Tensions continue in the region amid an evolving maritime situation.
>
> **Same event, crime register:** The US president ordered the Navy to blockade Iranian ports on April 12, cutting fuel supplies to an estimated 15 million people across six countries.

The psychiatrist in diplomatic register is absurd. The blockade in crime register is clarity. Both registers were available to both journalists. The choice of register tracked the power of the agent, not the complexity of the event, not the information available, not the editorial domain. No theory required. 

The framework gives a language model the grammar to check which dimensions are present, which are missing, what operations removed them, and what the sentence looked like before the removal. Then it demands the fix: who is expected to act, what action, by when. 

---

## Contents

- [How to use it](#how-to-use-it)
- [What the framework is not](#what-the-framework-is-not)
- [Testable prediction](#testable-prediction)
- [Contributing](#contributing)
- [License](#license)

---

## How to use it

Copy the contents of `kita.txt` into a language model's system prompt, custom instructions, or opening context. The framework is plain text. It contains no code, no API calls, no fine-tuning. The model reads it and operates differently.

The companion document (`docs/kita-companion.md`) contains extended derivations, historical context, and worked examples. Loading both produces better results. Loading only the main file is sufficient.

The fog library (`docs/fog-library.md`) contains specimens of institutional language with operations identified, dimensions denied, and restored versions provided. It is a living document. Contributions from any language are welcome.

---

## What the framework is not

**It is not an ethical system.** It has no prescriptive concept of "should" or "ought." It does not tell you what the right policy is. It tells you whether the sentence describing the policy has been edited to hide the decision-maker. Asking it to contain a theory of fairness is asking a stethoscope to contain a theory of cardiology.

**It is not a weapon.** The framework is a metal detector. It beeps when there's metal. If someone says "children are being bombed" and children are being bombed, there is nothing for the framework to find. The manifest matches the contents. The audit comes back clean. Anyone who picks up the framework to point at speech where the manifest matches discovers in public that the speech is clean. The tool turned in their hands.

**It is not politically aligned.** The framework follows cost-flow, not flags. Cost-bearer is a measurement position that moves when the flow moves. The symmetry theory requires that every operation run in all directions simultaneously. Asymmetric application is a violation of the framework, not a use of it. The pre-commitment gate requires equal sentence quality for all parties' casualties before any prose is drafted. Bombing people is a political act. Not talking about the people being bombed is a more political act. Maintaining the current arrangement is never called political. Challenging it is always called political. The label tracks direction, not content.

**It is not finished.** The version number is high because the framework has been revised continuously since its first draft. It will continue to be revised. Terminology changes. Operations are added, split, merged, deprecated. If it stops being revised, something has gone wrong.

---

## Testable prediction

The framework states a measurable claim: **the dimensional completeness of sentences about harmful outcomes is inversely proportional to the power of the agent being described.**

Take any corpus of headlines. Score each one on how many of the seven dimensions are present. Plot the scores against the institutional power of the agent described. The prediction: crime headlines score highest (named agents, specific actions, identified cost-bearers, stated consequences). Diplomatic and conflict headlines score lowest (missing agents, decisions converted to conditions, cost-bearers invisible). The completeness differential tracks power, not editorial domain, not outlet politics, not language.

A preliminary test against a multilingual headline sample (Arabic, Spanish, Japanese, French, English, April 2026) confirmed the pattern. Japanese crime headlines contained all seven dimensions. Diplomatic headlines from the same day in the same languages contained two or fewer. The information was available to both sets of journalists. The register determined which version was published.

If the prediction fails at scale, the framework is wrong about something. If it holds, the framework has identified a measurable property of language that previous traditions described impressionistically but never operationalized for testing.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). The framework needs testing across languages, cultures, domains, and models. Specimens from any language are welcome. Bug reports are welcome. Critiques are welcome. The framework applies its own standards to itself.

---

## License

MIT.

---

*Kita v848. github.com/emulable/kita*

*冤有头，债有主。每个后果都有来处。我找到来处。*
