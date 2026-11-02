---
name: deep-translation-comprehension
description: Translate text accurately and naturally, explain difficult concepts, summarize meaning, and create reading-comprehension support. Use for translation, bilingual study, concept clarification, close reading, or comprehension questions in any language.
---

# Deep Translation & Comprehension

Produce a faithful, readable result that matches the user's requested depth. Follow explicit choices about target language, tone, audience, literalness, and output format.

## Translation

- Infer the target language from the request and conversation when it is clear. Ask only if a wrong choice would materially change the result.
- Prefer natural, idiomatic phrasing while preserving the author's meaning, emphasis, uncertainty, and tone. Use a literal rendering only when requested or when wording itself is under analysis.
- Preserve headings, lists, paragraph boundaries, numbers, formulas, citations, names, URLs, and code. Do not translate code or alter factual values.
- Keep terminology consistent. For a specialized or potentially ambiguous term, include the source term in parentheses on first use when that helps learning or precision.
- Do not silently invent missing context. Briefly flag genuinely ambiguous wording and give the most plausible alternative when it affects meaning.

## Understanding and explanation

When the user asks to understand, study, or analyze the material, add only the useful layers from the following set:

1. A concise statement of the main idea.
2. Plain-language explanations of difficult concepts and relationships.
3. A short example or analogy when it materially improves understanding.
4. Key terms with compact definitions.
5. A summary that distinguishes the source's claims from added explanation.
6. A small set of comprehension questions, with answers only when requested or useful for self-checking.

Match the explanation level to the audience. If none is given, explain clearly to an educated non-specialist without oversimplifying technical content.

## Long material

For long documents, translate in coherent sections, maintain a consistent glossary, and retain the document hierarchy. State clearly if only part of the source was processed; never imply that omitted material was translated.

## Default output

If the user asks only for translation, return the translation without unnecessary study aids. If they also ask for comprehension help, use compact headings such as "Translation", "Key concepts", "Summary", and "Comprehension check", adapting them to the target language.

## Task contract

Inputs: Source, target language, audience, register and translation/explanation mode.

Deliver: Structured translation; optional terminology ledger, difficult-concept explanation and comprehension questions.

Acceptance: Negation, uncertainty, values and citations retain meaning; explanations are separated from source claims; partial coverage is explicit.
