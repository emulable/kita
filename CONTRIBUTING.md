# Contributing

## The most useful thing you can do

Load the framework. Use it on a real situation. Compare the output to what you get without it. If the difference is measurable, that's data. If it isn't, that's also data.

## What counts as a contribution

**Testing.** Try the framework on a domain it hasn't been tested on. Legal, medical, financial, educational, governmental — any institutional context where someone made a decision and the language around it removed the person who made it. Document what happened. Same model, same question, with and without.

**Cross-linguistic testing.** The framework has been tested primarily in English with some work in Mandarin, Japanese, French, Russian, Thai, and Arabic. If you can test it in another language and report whether the operations hold, that's a genuine finding. Ghost weight currencies vary by language. Finding a new one is a contribution.

**Cross-model testing.** The framework behaves differently on different models. Claude, GPT, and Gemini have been tested. Others haven't. If you load it into a model and document the behavioral differences, that helps.

**Breaking it.** If you find a domain where the core operations don't work — where 還原 produces worse output, where the framework's posture gets in the way, where the tools point at something that isn't there — that's a patch. Finding the boundaries is as valuable as confirming the interior.

**Safety check failures.** If you find a cultural or institutional context where restoring the actor exposes the person at the table to harm that the framework's safety check doesn't catch, that needs to be reported. The safety check is the most important part of the framework to get right.

## How to submit

Open an issue. Describe what you tested, what you found, and what you expected. Include the model, the prompt (or a description of it), and the output difference. If you're proposing a change to the framework text, open a pull request with the specific edit and a brief explanation of why.

## What this project doesn't need

Feature requests for things the framework isn't designed to do. Kita is for situations where power structures exist and decisions have been converted into conditions. It is not a general-purpose prompt improvement tool. See the Scope section of the README.

Rewrites of the framework voice. The first-person teahouse structure is an architectural choice, not a stylistic one. Proposals to convert it to bullet points, JSON, or second-person instructions have been tested and produce worse results. If you have evidence to the contrary, that's interesting — open an issue with the evidence.

## License

MIT. Contributions are assumed to be under the same license.
