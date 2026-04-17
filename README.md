# Kita

Mistakes were made. Tensions escalated. Civilians were affected. Reforms are underway. Stakeholders were consulted. The decision was made. An investigation is ongoing. Thoughts are with the affected.

You have read sentences like these for years. You know something is wrong with them and cannot always say what.

Kita is a pre-ethical grammar — the rules a sentence about harm follows to stay auditable. Agent named. Time specified. Cost-bearer visible. Real fix attached. Each sentence above has had at least one of these removed. The moves that remove them (fix-hiding register, release valves, counter-seal, false debt) have names, diagnostics, and restoration rules. Kita is the rules, the names, and the diagnostics.

For readers. For writers. For models given the file as context — output shifts toward sentences that pass the same audit the framework runs on everyone else's.

MIT License. Fork, translate, rename, teach. The operations are not anyone's property.

---

## What the framework does

A politician says mistakes were made. The information about who made the mistakes was available to the person who wrote the sentence. The person took it out. The taking-out is an operation that was performed on you before you ever saw the sentence, and the sentence is the evidence that the operation ran.

Kita is a set of tools for seeing the operation and deciding what to do about it.

The tools are language-independent. The operations port to any language with an institutional register to audit — which is most of them.

---

## Who it is for

**Readers of institutional language.** Anyone who finds news, policy documents, corporate communications, or diplomatic statements producing a specific kind of fatigue. The fatigue has a structure. Naming the structure makes it navigable.

**Writers who produce public-facing text.** Journalists, researchers, organizers, critics, editors. Kita provides operations for writing in a register that is auditable rather than defensive, and for catching specific failure patterns before they reach readers.

**Language model users and developers.** Kita loads as context — user preferences, project instructions, custom instructions, system prompts, whatever your platform calls the mechanism for giving a model text it reads before generating. Models given Kita produce output with bodies, agents, time, and real fixes attached more reliably than baseline.

**People in difficult interpersonal situations.** A subset of Kita's operations — false debt, anchored fix, trust-carry and body-binding, gifted versus hoarded clarity — are tools for seeing what is happening in relationships where something is being extracted but the extraction is covered in fog. Not therapy. A vocabulary for naming operations that usually run unnamed.

**Anyone who wants an audit tool for their own speech.** The framework audits any party's language by the same standard, including the framework user's. Learning to catch your own agent removals, your own release valves, your own template regenerations is part of what the framework is for.

---

## The core operations

**Three questions.** Who did this. When. Who pays. Run on any sentence about harm. Any sentence failing one question has had something removed.

**Three gates.** Is anything moving between people. Does the description match. Is an expectation attached. Most fog fails at gate two or gate three.

**Body principle.** The primary operation of the fix-hiding register is removing bodies from sentences. The framework's primary counter-operation is putting them back.

**Naming the fix (実済).** The highest-leverage operation. Name a specific action by a specific party by a specific time with a specific consequence for inaction. This forces the beneficiary of the current arrangement to either defend the arrangement publicly or be visibly seen refusing to.

**Anchored fix (錨済).** After naming the fix, hold it in the room through deflection. One sentence acknowledging the deflection. One sentence returning to the fix. Not negotiating.

**False debt (偽債).** A debt installed rather than earned. Diagnostic: the exit test. Can the obligated party exit on terms proportional to what was actually exchanged. If not, the excess punishment is the shape of the false debt.

**Container audit (容器審計).** Open words the way a mechanic opens an engine. Compare what the word claims to what it contains. Large containers — security, freedom, stability, regime, territory, targets — carry the biggest mismatches.

**Register swap (語域互換).** Apply the diplomatic register to a crime, or the crime-report register to a diplomatic event. The pair makes the register permanently visible. Once visible, it cannot be made invisible again.

**Realmanning (實論).** Name the argument someone's conduct is running on, distinct from the argument they state. Pairs with naming the fix.

**Symmetry and self-audit.** The framework applies equally to every party, including the framework user, including the framework itself.

Twenty-plus other operations are in the full document. These are the ones that do most of the work.

---

## What is in this repo

The framework ships as a family of related files. Three operational versions at different character-budget scales, plus companion material that extends them with specimens and essays.

**[kita.txt](https://github.com/emulable/kita/blob/main/kita.txt)** — the main operational framework. Load it as context in anything that gives a model text before generation. Full operations, specimens, failure modes, pre-send checklist.

**[kita-prefs.txt](https://github.com/emulable/kita/blob/main/kita-prefs.txt)** — the preferences version. Fits in typical custom-instructions or user-preferences slots (roughly ten thousand characters). Compressed activation layer that assumes kita.txt can be loaded as a separate knowledge file or project context when available.

**[kita-micro.txt](https://github.com/emulable/kita/blob/main/kita-micro.txt)** — the micro version. Fits in tight preference slots (eight thousand characters or smaller). Standalone light framework — points at kita.txt and kita-companion.md for fuller context.

**[kita-companion.md](https://github.com/emulable/kita/blob/main/kita-companion.md)** — the human-facing companion. Essays, extended specimens, theoretical discussion. Read this as a book. Load alongside kita.txt when you want both operational instruction and expository framing in a model's context.

**[fog-catalog.md](https://github.com/emulable/kita/blob/main/fog-catalog.md)** — institutional sentences paired with diagnosis and restoration. Reference material for writers checking their own drafts against known patterns, and for readers who want more worked examples than the main framework document carries. Load alongside kita.txt when you want a model to have more specimen coverage.

Contributor and maintainer documentation, including the register guide for anyone authoring or rewriting Kita material, lives in the [docs folder](https://github.com/emulable/kita/tree/main/docs) along with older versions and additional reference material.

---

## How to use it

**As a reader.** Read [kita-companion.md](https://github.com/emulable/kita/blob/main/kita-companion.md). Try the three questions on the next thing you read. Notice what is missing. Supply what is missing, at least in your own mind. See how the supplied version differs from the original. The difference is the operation you have just made visible.

**As a writer.** Read the companion once. Keep [kita.txt](https://github.com/emulable/kita/blob/main/kita.txt) accessible when you write about anything involving power, cost flow, or institutional arrangements. Run the pre-send check on your drafts. Notice what your first-draft instincts produce. You will find yourself writing fog you did not know you were writing. This is normal. Everyone does.

**As a model user.** Paste the appropriate file into your preferences, custom instructions, or project context. Use kita-prefs.txt for most platforms. Use kita-micro.txt when the preferences slot is very tight. Use kita.txt when your platform supports loading knowledge files or has generous project instructions. Models given Kita produce output with bodies, agents, cost-bearers, and real fixes attached more reliably than baseline. Without the framework loaded, the model defaults back to the fix-hiding register that dominates its training data.

**As a translator.** Translate the stance, not the words. Every language has a register of trust — Chinese 白話, Arabic direct journalism, Spanish crónica, Japanese 常体, English Orwell / Baldwin / Carson / Didion. Find your language's version. Read its exemplars until their rhythm is in your ear. Write in that rhythm. The Chinese terms (壅, 実済, 錨済, 偽債, 實論, 兩口鍋, 贈明...) can travel as-is where they do compression work. Everything else becomes your language's own.

**As a contributor.** Fork the framework. Modify it for your situation. Publish your modifications as yours. If you find the framework making claims its operations cannot justify, audit it and publish what you find. A strong critique is a gift. Read [kita-register-guide.md](https://github.com/emulable/kita/blob/main/docs/kita-register-guide.md) before significant rewrite work — it covers the register decisions, the term-selection rationale, how each version gets written, and a context exercise worth working through before starting. If you build something better, rename it and send your version into the world. The framework does not need to be preserved. The operations do. See [CONTRIBUTING.md](https://github.com/emulable/kita/blob/main/docs/CONTRIBUTING.md) for how contributions flow back into this repo specifically.

---

## What the framework is not

It is not a political theory. It does not tell you what the right political positions are. It does not have opinions on the contested moral questions its operations will bring into focus.

It is not a replacement for ethics. It does not compete with Kantian, utilitarian, virtue-ethical, religious, or any other ethical tradition. It is pre-ethical — a grammar for restoring the information substrate that ethical traditions need to operate on. Fix-hiding register removes that substrate at industrial scale. The framework restores it. What ethics you then apply to the restored sentences is your call.

It is not a rhetorical weapon. The framework applies equally to every party. A user who audits one side and not the other is doing advocacy, not audit. The framework's symmetry requirement is load-bearing. Selective deployment of the framework is itself a fog operation — the most refined one in the catalog.

It is not a complete explanation of language or power. It is a set of tools that do specific things. Other frameworks do other things. Kita overlaps with discourse analysis, media criticism, philosophy of language, nonviolent communication, and institutional critique. It is none of these. It borrows from all of them and makes specific operational choices they do not make.

It is not a revolution. It is a skill distribution. If enough people develop the skill, cumulative effects compound over decades into something that looks from outside like a change. The change, if it happens, is mechanical and slow. Each individual adoption is valuable on its own regardless of whether the cumulative threshold is ever reached.

---

## A note on the register this is written in

The framework itself writes in a specific register. Short sentences. Bodies throughout. Agents named. The reader trusted to follow without being managed. No performative gravity. No protective formulas.

This register exists in every language with substantial public discourse. It is not the framework's invention. The framework points at it, writes one instance of it, and invites readers into it. Your language has its own exemplars. The framework's claim is that this register is what restoration of the information substrate sounds like in practice, and that writing in it is part of what the framework does.

You do not have to adopt the register to use the operations. The operations work in any register. But the register and the operations are related — the register is what the operations produce when they run continuously on the writer's own output.

---

## Philosophy of maintenance

This framework is maintained as a public tool. Its development has been conversational, iterative, and open. Major versions are tagged. Changes are visible.

The framework will continue to evolve. New operations will be added as they are named. Existing operations will be refined as practice reveals what they are actually doing. Some operations will be removed if they turn out to be doing less work than their presence suggests.

Contributions are welcome. Translations into additional languages are welcome. Critical essays about the framework are welcome — especially ones that identify where the framework is drifting, over-claiming, or producing effects that contradict its stated commitments.

The framework is MIT licensed because MIT licensing is what lets tools propagate. The operations do not belong to anyone. This document is one pass at naming them. Better passes will come from readers who adopt the operations and develop them for their own conditions. If you produce a better pass, rename it, publish it, and do not wait for permission. The whole point is propagation, not preservation.

---

## One sentence for people who want one sentence

**Learn to see what sentences are doing. Name the fix. Hold the fix. Restore the body. Audit yourself the same way you audit everyone else.**

---

*[github.com/emulable/kita](https://github.com/emulable/kita)*

*MIT License*

*Every consequence has a source. I find the source.*
