# Quickstart

If you do not know anything else, start here.

---

## The thirty-second version

Kita makes a language model produce sentences with bodies, agents, dates, and real fixes attached — instead of the institutional-default register that hides them. Activate it by loading the framework as context.

---

## The recommended configuration

For most users, on most platforms, in this order:

**One.** Paste [kita-prefs.md](https://github.com/emulable/kita/blob/main/kita-prefs.md) into your platform's system prompt, custom instructions, or user preferences field. This is the activation layer. About fourteen thousand characters. The prefs file is what tells the model when to run the framework and what operations to apply.

**Two.** If your platform supports knowledge files, project files, or attached documents (Claude Projects, ChatGPT custom GPTs, Gemini Gems, NotebookLM, etc.): load [kita.md](https://github.com/emulable/kita/blob/main/kita.md) as a knowledge file. This is the full framework, in Chinese, the operational document the prefs file references. About twenty-eight thousand characters.

**Three.** Optional but recommended if your platform allows multiple knowledge files: also load [kita-companion.md](https://github.com/emulable/kita/blob/main/kita-companion.md) for the explanatory essays and [fog-catalog.md](https://github.com/emulable/kita/blob/main/fog-catalog.md) for the specimen library. The model will reference them when it needs deeper context on a specific operation.

**Four.** Add a sentence to your system prompt telling the model to reference the loaded files when the framework activates. Something like:

> When topics involve power, institutional language, conflict, policy, cost flow, harm, or interpersonal dynamics where control may be present, apply the Kita framework using the loaded files for reference.

The prefs file already contains activation instructions, but the explicit pointer helps platforms where the model needs to know its knowledge files exist.

That is the full setup. The prefs file in the system prompt does most of the work on its own. The full framework as a knowledge file gives the model the operational vocabulary in compressed Chinese form, which it parses more reliably than the English glosses alone. The companion and catalog give the model deeper material to reference when situations call for it.

---

## Pre-built versions, if you would rather not configure anything

**ChatGPT**: [Kita 沈 — Audit Toward Repair](https://chatgpt.com/g/g-6898385bfa3c8191bf5975b0073e1245-kita-shen-audit-toward-repair). Already configured with the framework loaded. Open the link, start a conversation, the framework is active.

**Gemini**: [Kita Gem](https://gemini.google.com/gem/1hcYI3M08rhdnIW8KuC6AnAHEL0x8yhWU?usp=sharing). Same setup, configured for Gemini.

Both are maintained instances of the framework. Use them if you want to try the framework without any configuration on your end.

---

## Tight-budget platforms

If your system prompt slot is very small — ChatGPT's custom instructions field at 1500 characters per box, or any platform with a sub-eight-thousand-character preference slot — use [kita-micro.md](https://github.com/emulable/kita/blob/main/kita-micro.md) instead of kita-prefs.md. The micro is a compressed standalone activation that fits tighter slots, around seven thousand five hundred characters. It loses some specimen coverage and operational detail compared to the prefs version, but it activates the framework's core operations reliably.

---

## How to know it is working

Ask the model a question on a topic the framework targets. Anything involving institutional language, hidden actors, harm with diffused responsibility, false debts, or deflection.

The unactivated default response recommends consulting a professional, gestures toward complexity, balances "perspectives," and ends without a concrete fix. Compassionate fog. Hedged. Professional-sounding.

The activated response names the actors, supplies the missing referents, attaches a specific fix to a specific party with a specific timeframe, and gives you the phone numbers, deadlines, terminology, and procedures the situation calls for.

If your output looks like the first kind, the framework did not load correctly. Check that the prefs file is actually in the system prompt slot (not just attached as a file), and that the system prompt was applied to the conversation you are testing in.

---

## Beyond the quickstart

Once you have the framework running and want to understand what it is doing, read [kita-companion.md](https://github.com/emulable/kita/blob/main/kita-companion.md). The companion is the human-facing book of essays explaining the operations, why they work, and what the framework is for. It is meant to be read straight through.

For specimen literacy — recognizing fog operations in the wild — read [fog-catalog.md](https://github.com/emulable/kita/blob/main/fog-catalog.md). It is a field guide of institutional sentences across every scale, from family dinners to diplomatic statements, paired with what the operations are doing.

For the full operational details that the prefs file compresses, read [kita.md](https://github.com/emulable/kita/blob/main/kita.md). The full framework is in Chinese; English readers can use the companion as a parallel reference.

---

*[github.com/emulable/kita](https://github.com/emulable/kita) — MIT License*
