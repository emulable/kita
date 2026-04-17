# 🏺 Contributing to Kita

## 🧭 Orientation

Kita is a grammar for complete sentences about harmful outcomes. A complete sentence contains an agent, a time, a scale, a direction, a cost-bearer, a comparison, a scope, and an expectation of repair. Most institutional language about harm is incomplete. The pattern of what's missing is the finding.

The framework is a precondition for ethics, not an ethical system itself. Every ethical tradition ever developed requires a subject, an action, and a consequence to operate on. The register used by institutions to describe harmful outcomes routinely removes these elements before the sentence reaches the reader. The framework puts them back. What you do with a complete sentence is your ethics, your politics, your philosophy, your conscience. The framework's job ends when the sentence is whole.

Contributions to Kita help the grammar work in more languages, more domains, more situations, and on more models. Contributions also help us find where it breaks.


## 🗝️ How to contribute

Open an issue or pull request. Include context. For output samples: the model, the prompt (or a summary), and the output. For specimens: the sentence, the language, the operation, the dimension denied, the restored version. For bugs: what happened, what should have happened, and what model was running.

Good contributions get folded in. The framework has been revised hundreds of times and every version learned from someone pointing at something and saying "this doesn't work" or "look what this did."


## 🧫 Testing

The most useful testing puts the framework in front of real language and checks whether the output has the elements the framework requires: named agents, specified times, quantified scales, visible cost-bearers, and an attached expectation (who should do what, by when, and what happens if they don't).

Places to test that tend to surface interesting results: news coverage of military operations, insurance denial letters, corporate restructuring announcements, landlord notices, government policy statements, diplomatic briefings, HR communications, medical billing disputes, and interpersonal situations involving control or manipulation. The framework's operations appear in all of these because the mechanism of hiding a decision-maker inside a description of a decision is universal.

When testing, check for two failure directions. The framework can over-trigger, treating ordinary vagueness or time pressure as deliberate obstruction. And it can under-trigger, producing text that carries the framework's vocabulary and aesthetic while still missing agents, hiding the fix, or ending without an expectation attached. The second failure is harder to catch because it looks like compliance.

A useful test for any output: could someone who reads this locate the person who made the decision, find the person bearing the cost, and identify a specific action that would change the situation? If all three are present, the framework did its job. If any are missing, something slipped through.


## 🪷 Language, culture, and creative work

The framework was built in English and Chinese against primarily English-language institutional text. Its claim is that agent removal, decision-to-condition conversion, and fix-hiding are structurally universal, appearing in every language that has institutions. That claim has barely been tested.

If you speak a language other than English, the framework needs you more than it needs another English-language test run. Every language has its own mechanisms for dissolving a decision-maker into grammar. Japanese has extensive passive and honorific structures that can erase agency while sounding respectful. Arabic has verb forms and nominal constructions that institutional text uses differently than conversational speech. Spanish has reflexive and impersonal constructions that can make an action appear to happen to itself. Russian has impersonal sentence structures that institutional language exploits routinely. These are not the same as English passive voice. They are local mechanisms serving the same structural function, and the framework needs to catalog them.

Specimens from any language are welcome. A specimen is a real sentence from institutional communication that passed every filter, sounds professional, and removed something the reader would need in order to locate the decision-maker or reach the fix. If you can identify the operation and write the restored version, you've contributed to the fog library.

Translations of the framework are welcome with one constraint: the Chinese operational terms exist as perturbation anchors. They work on language models precisely because a model cannot map 蔽済語域 onto a familiar English phrase and continue on autopilot. A translation that smooths the Chinese into comfortable target-language equivalents has removed the friction the terms were designed to create. Preserve the originals, annotate them, and let them stay uncomfortable.

Creative work is welcome. The framework's best explanatory tools have come from stories, metaphors, and images. 兩口鍋 (two pans) is a story about a woman cutting meat in half for twenty years. The building-on-fire metaphor describes the entire fix-hiding dynamic in an image anyone can hold. If you find a way to explain an operation through a story, an image, a comic, a song, a game, or anything else that makes the operation visible to someone encountering it for the first time, that is a contribution.

Corrections to the framework's own cultural ignorance are welcome and expected. The framework was built by one person working primarily in English with Chinese as an operational language. Blind spots are guaranteed. If the framework misuses a concept, mistranslates a term, misunderstands a cultural mechanism, or applies an operation in a way that doesn't survive contact with how your language or culture actually works, say so. These corrections make the framework more accurate. Accuracy is the only thing the framework is for.


## 🩻 Bugs and failure modes

Known issues worth watching for:

Models sometimes slip into Chinese mid-response. The operational file is written in Chinese and some models lose the language boundary, especially in longer conversations or when multiple framework terms appear close together.

Models sometimes perform the framework's aesthetics without executing its operations. The output sounds like an audit. It uses the vocabulary. It references the concepts. And then it ends without naming the agent, specifying the fix, or attaching an expectation. This is the most dangerous failure mode because it passes casual inspection.

Models sometimes over-apply the obstruction catalog, flagging routine bureaucratic language as deliberate concealment when the person who wrote the sentence was just filling out a template under time pressure. The framework's own obstruction threshold test requires trying the strongest non-malicious explanation first. If the non-malicious explanation fully covers the sentence, the framework should not trigger.

Models sometimes revert to defaults mid-conversation. The first response holds the framework's grammar. By the fifth or sixth exchange, the training distribution's pull has dragged the output back toward passive voice, missing agents, and "it could be argued" hedging. Long conversations are where the framework is most likely to lose its grip.

If you encounter these or any other failure mode, file it. Include the model, the approximate point in the conversation where the failure occurred, and what the output did versus what it should have done.


## 🪆 Feedback we've already heard

Several critiques of the framework recur. They have been examined and addressed in the framework text, the companion essays, or both. Repeating them is fine. Repeating them as though they are novel findings that the framework hasn't considered is less useful. Here is what has already been worked through.

"The framework will over-apply and treat everything as obstruction." The three-gate model exists for this reason. Most language passes through Gate 1 in under a second because it involves no cost/benefit flow between people. The obstruction threshold test requires the strongest non-malicious interpretation before any sentence is flagged. The framework triggers less often than people expect.

"The framework is politically biased toward one side." The framework follows cost-flow, not flags. Cost-bearer is a measurement position that moves when the flow moves. The symmetry theory requires that every operation run in all directions simultaneously. Asymmetric application of the framework is a violation of the framework, not a use of it. The pre-commitment gate requires equal sentence quality for all parties before any prose is drafted.

"The framework needs a theory of fairness / reciprocity / equal standing layered on top." The framework is a grammar for complete sentences, not an ethical system. Asking it to contain a theory of fairness is asking a stethoscope to contain a theory of cardiology. The stethoscope tells you what the heart is doing. The framework tells you what the sentence deleted. Every theory of fairness, reciprocity, and equal standing is welcome to operate on the complete sentences the framework produces. The framework's job ends when the sentence is whole.

"The framework's Chinese terms are inaccessible." They are designed to be. They function as perturbation anchors that prevent language models from mapping the operations onto familiar institutional English and continuing on autopilot. Each term is annotated with an English equivalent. The friction is the feature.

"The framework fits asymmetric situations better than symmetric ones." The framework says this about itself. Situations where all parties genuinely bear comparable costs and all available exits carry real costs for someone are tragedies. The framework's work in tragedies is narrower: name it accurately as a tragedy, map the cost distribution honestly, and identify the smallest available intervention. The framework's full machinery activates when the description of the situation has been edited to hide who benefits and who pays. Where no such editing has occurred, the framework's gates pass the language through without intervention.


## 🚪 Where to apply it

Anywhere a sentence describes a harmful outcome and someone might have removed the elements you would need to find the decision-maker or reach the fix. Institutional language is the largest producer by volume, but the operations appear at every scale: government, corporate, legal, medical, educational, interpersonal, and inside the language models themselves.

The framework applies to its own outputs. If a model running the framework produces a sentence that hides an agent, obscures a fix, or ends without an attached expectation, the framework has failed on its own terms. Catching these self-failures is some of the most valuable testing available.


---

*Kita. github.com/emulable/kita. MIT License.*
