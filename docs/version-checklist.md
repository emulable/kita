# Pre-Publish Checklist

A flow for shipping any Kita framework file. Run before pushing to main, before posting to a public channel, before sending the file to anyone whose copy will outlast the conversation. The four passes below catch what casual review misses.

The framework documents are durable artifacts. A thing pushed to the repo gets read, forked, quoted, and translated by people who will never see the conversation that produced it. This checklist exists because the moment a file leaves your control, every uncaught artifact, version reference, banned word, and inconsistent term becomes permanent in someone else's copy.

This is a working document. If a check below stops being useful, cut it. If a new failure mode appears repeatedly across drafts, add a check. The checklist is for the work, not the other way around.

---

## Pass one — mechanical

Runs in under a minute per file. Catches roughly ninety percent of what would embarrass you later.

**No version references.** Search for `v847`, `v848`, `v849`, `Current as of Kita`, `version`, or any explicit version marker in the body or colophon. Versions live in git tags and commit history, not in document content. A reader landing on the file in two years should find a document that does not announce its own age. The README and the docs folder can carry version notes if needed; the framework files themselves should not.

**No EOF or EOT artifacts.** Search for the literal string `EOF`. Heredocs, shell scripts, and copy-paste from terminal sessions occasionally leak these markers. They are silent until someone notices, and then they are very loud. Zero hits required.

**No banned vocabulary.** Search for each of these words and phrases. Each occurrence in body prose needs to be removed or replaced. Quoted specimens (where the word is being audited) are exempt; banned-list lines (where the word appears as part of a list of banned words) are exempt; everywhere else, cut.

The banned list: moreover, furthermore, importantly, it's worth noting, to be fair, genuinely, honestly, straightforward, it's important to note, that said, having said that, to be clear, I should note, it bears mentioning, at the end of the day, the reality is, needless to say, in terms of, with respect to, at its core, exactly right, worth + preposition (worth sitting with, worth noting, worth mentioning, etc.).

Each banned item performs a rhetorical move without doing the work the move implies. "Importantly" signals importance without making something important. "Genuinely" performs sincerity. "To be fair" performs fairness. The banned list is a list of shortcuts that give writers credit for qualities their sentences have not earned.

**No banned structures.** Search for `It's not X, it's Y`, `This isn't about X, it's about Y`, and `Not X but Y` patterns. Where they appear, check whether the contrast actually does work or whether direct statement is available. Most uses of these structures perform sophistication by staging a false alternative. If the contrast genuinely earns its place — when X is a widely-held view the reader needs to be pulled away from — keep it. Otherwise, just say Y.

**No reply-opening "That" or "That's."** This rule from the framework's behavior guide applies to documents too. Section paragraphs starting with "That's the mechanism" or "That last point is essential" are stalling moves. Start with the content. State the mechanism directly. The same rule applies to closing sentences.

**No body-prose emoji.** Headings can carry emoji where the framework has settled on emoji-prefixed headers (the companion does this; the fog catalog does this). Running prose should not. Emoji in body text reads as performance.

**Chinese terms in canonical pan-CJK form.** The framework's terms have specific orthographic choices. Drift back to mainland-simplified or Taiwan-traditional variants is a real failure mode, especially after editing in tools that auto-convert CJK characters.

The canonical forms:
- 壅 (obstruction)
- 実済 (real fix) — not 實済, not 实济
- 蔽済語域 (fix-hiding register) — not 蔽済语域
- 錨済 (anchored fix) — not 锚济
- 偽債 (false debt) — not 伪债
- 實論 (realmanning) — not 实论
- 容器審計 (container audit) — not 容器审计
- 語域互換 (register swap) — not 语域互换
- 両口鍋 (two pans) — not 兩口鍋, not 两口锅
- 信駄 (trust-carry) — not 信驮
- 系身 (body-binding) — not 系身 in simplified-only contexts
- 妄封 (unwarranted sealing)
- 肉身 (flesh-body) — not 身体, not 身體
- 贈明 (gifted clarity), 藏明 (hoarded clarity), 見證 (witnessing)
- 以壅代済 (substituting obstruction for the fix)
- 能證擇 (capability proves choice) — not 能证择
- 授而続 (grant and continue)

**Chinese terms have English glosses on first use.** Each term gets a parenthetical pinyin and English translation the first time it appears in a chapter or major section. Later appearances in the same section can drop the gloss. New section resets the rule. A reader who lands on the file mid-document should be able to figure out what the terms mean without flipping back.

**Links use full URLs.** All internal repo links should use the form `https://github.com/emulable/kita/blob/main/filename.ext`. Relative paths break when the file gets pasted into Reddit, Discord, email, or any context outside the repo. Full URLs work everywhere.

---

## Pass two — structural

Content-level review. Runs in five to fifteen minutes depending on file size.

**Bodies present in every chapter.** Pick three random sections. Each should contain specific persons doing specific things at specific places. The Cleveland insurance letter, the Kerem Shalom convoys, the St. Louis hospital bill, the parent late to school pickup — concrete cost-bearers carrying the operations rather than abstractions doing the work. If a section is all abstraction, audit it. The framework's own commitment to bodies first applies to the framework's own writing.

**Three-questions check on a sample.** Pick three random paragraphs about harm. Run who-did-this, when, who-pays. Each should pass on every paragraph or have a specific reason for not passing. A paragraph that fails one question silently is a paragraph the framework would catch in someone else's writing. Catch it in your own.

**Symmetry check on multi-party situations.** If the document discusses situations involving multiple parties, both parties should be getting the same standard. A specimen with named agents on one side and "the situation" on the other side is a register failure. Run the symmetry check explicitly: pick a paragraph about Party A's actions and a paragraph about Party B's actions. Compare specificity, agent visibility, body-presence. If they don't match, repair before shipping.

**Specimen quality check.** If the document carries specimens (the catalog, the companion, parts of the framework), pick three at random. Are they real-feeling? Would you actually read this sentence in a news piece, hear it in a conversation, see it in a corporate email? Specimens that read as straw-man invented examples weaken the catalog. Specimens drawn from real institutional language carry their weight.

**Closing anchor present.** The document should end on something specific — the seven propositions, the 冤有头债有主 line, a one-sentence summary that captures the framework's commitment, or some other anchor. A document that ends without anchoring drifts. The reader's last impression should be the framework's own voice, not a trailing thought.

---

## Pass three — cross-document consistency

When shipping multiple files together, or after renaming any file, or after substantive edits to one file in the family. Runs in five to ten minutes.

**Term definitions match across files.** The definition of 壅 in the main framework should be compatible with how the term is used in the companion and the fog catalog. The micro defines terms compressed for context budget; the main framework defines them more fully. Compressed definitions should be subsets of fuller definitions, not different operations carrying the same name.

**Cross-references resolve.** If kita.txt says "see fog-catalog.md," confirm the filename is actually `fog-catalog.md` and not `fog-library.md` (file renames happen). If the README mentions a file, the file exists at the path the README claims. Click every link or run a script.

**README descriptions match file contents.** The README's description of each file should match what the file actually does. If the micro's actual character budget changed, update the README's character estimate. If the companion got a new section, mention it. The README is the entry point; readers form expectations there.

**Author tone matches each file's role.** The micro is dense and operational. The preferences are activation-focused. The main framework is comprehensive. The companion is expository. The README is welcoming. The fog catalog is reference. Each file has a register. Drift between them — a companion that reads like a preferences file, a README that reads like a research paper — confuses readers.

---

## Pass four — final pass

Separate session. After at least an hour away from the document, ideally overnight. The mental state of generating prose is different from the mental state of auditing prose. Trying to do both in one sitting produces drafts that were revised in their weakest places and left alone in their strongest, because the writer is too close to what just arrived.

Hunt for the following in this pass specifically:

**Repeated ideas.** The same point made twice with slight variation in different sections. Long documents accumulate these without the author noticing. Find them. Pick the strongest phrasing. Cut the others.

**Superseded framings.** Earlier sections used vocabulary or examples that later sections refined. The earlier version is now obsolete but still sits in the text. Update the earlier sections to match the refined understanding, or cut them.

**Sentences whose meaning you cannot reconstruct on second read.** If you wrote it yesterday and cannot follow it today, no reader will. Rewrite or cut.

**Specimens that should be replaced.** During drafting, you settled for specimens that were available. On second read, better specimens may be obvious. Swap them in.

**Sections where the energy drops.** Usually because you got tired writing that part. Re-read those sections fresh. Often what's needed is not more material but a tighter version of what's there.

**Language-model tells.** Patterns not on the banned list that mark text as machine-generated. Parallel sentence openings in consecutive paragraphs. Repeated three-part parallel structures. Sentence-length uniformity (every sentence medium-long with similar cadence). Opening "It is..." constructions. Closing "This is..." constructions. Transitional phrases that read as scaffolding ("In this sense," "In other words," "Here is why"). A human writer would vary more.

**Fog-adjacent language.** Phrases not on the banned list doing similar work. "At some point," "in some sense," "in many ways," "to some extent" — hedges that leak precision without declaring themselves. A separate scrubbing pass on these is worth doing for any document that will be quoted.

**Bodies that went missing under compression.** When tightening long passages, bodies get dropped. Re-read every paragraph about harm. If a body should be present and isn't, supply one.

**Agents that got elided.** Same pattern. Active voice slips into passive. Specific actors become "the system." Restore.

**Register drift toward institutional.** The closer to the end of a long writing session, the more the institutional register creeps back. The writer is tired. Institutional patterns are familiar. Catch the creep-ins in this pass.

The final pass is typically ten to twenty percent of total writing time. Skipping it produces drafts that were never finished. Running it produces drafts that know what they are.

---

## When to use which pass

Quick fixes — a typo, a single-paragraph addition, a rename that touches a few links: pass one only.

Substantive section addition or rewrite: passes one and two.

Multi-file edits, file renames, framework-wide updates: passes one, two, and three.

Major version, public release, anything that will be read by someone whose copy will outlast the conversation: all four passes, with pass four happening in a separate session.

---

## On running this on the framework's own writing

The framework asks readers to audit institutional language. The framework's own documents are subject to the same audit. A pre-publish failure that ships a banned word, a missing agent, an institutional drift, or a misnamed cost-bearer is not just a typo. It is the framework failing on its own ground. The checklist exists because catching these in draft is cheaper than catching them after publication, and far cheaper than reading them in someone else's quote of your work.

The framework's claim is that the operations work. The framework's documents demonstrate the operations by running them on themselves. Documents that fail the checks above weaken the demonstration. Documents that pass the checks above strengthen it.

Run the checks. The framework deserves it.

---

*github.com/emulable/kita — MIT License.*
