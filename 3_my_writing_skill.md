---
name: my-academic-writing
description: Revise and polish English computer-science and technical academic writing for precise wording, logical progression, paragraph cohesion, section-level coherence, and publication-ready style. Use for manuscripts, abstracts, introductions, related work, methods, results, discussions, conclusions, and reviewer responses. Preserve technical meaning, evidence, citations, terminology, numbers, and requested length while improving clarity and scholarly tone.
---

# Academic Writing

## Core objective

Improve the text without changing the study. Prioritize, in order:

1. factual and citation integrity;
2. logical coherence;
3. paragraph and sentence cohesion;
4. semantic precision and natural collocation;
5. concision, rhythm, and formal tone.

Do not equate academic writing with longer words, heavier nominalization, more passive voice, or more transition markers.

## Non-negotiable constraints

- Preserve the author's claims, scope, stance, results, sample sizes, model names, API identifiers, equations, metrics, citations, and cross-references.
- Never invent evidence, references, attributions, methods, experiments, findings, limitations, or causal explanations.
- Do not claim that a cited source says something unless the source has been checked.
- Do not reduce the manuscript's substantive length unless the user requests shortening. Remove only genuine redundancy and recover any lost substance through clearer development.
- Apply minimal, local revisions when the original wording is already accurate. Do not rewrite merely to produce visible change.
- Preserve established technical terminology. Prefer the field-standard term over an elegant but less exact synonym.
- Keep benchmark names, dataset partitions, abbreviations, capitalization, mathematical notation, and hyphenation internally consistent.
- Follow the target venue's style when it conflicts with a general preference in this skill.

## Working sequence

### 1. Establish the writing situation

Identify the genre, section, intended claim, target readership, venue conventions, and requested degree of intervention. Determine whether the task requires copyediting, substantive polishing, restructuring, or a new draft.

### 2. Protect the evidence boundary

Mark every sentence that contains a number, comparison, causal statement, novelty claim, limitation, or citation. Verify that revision does not strengthen or broaden it beyond the available evidence.

### 3. Diagnose from macro to micro

Review in this order:

1. section purpose and order;
2. paragraph function and argument progression;
3. sentence-to-sentence information flow;
4. grammatical agency and referents;
5. vocabulary, collocation, syntax, and punctuation.

Do not begin with synonym replacement when the real problem is argument structure.

### 4. Revise in passes

Complete separate passes for coherence, cohesion, sentence design, wording, and factual verification. Re-read the revised passage as continuous prose rather than as isolated sentences.

## Coherence: organize the argument

Treat coherence as the macro-level organization of ideas.

- Give each section a clear rhetorical purpose.
- Give each paragraph one principal function: establish a claim, explain a mechanism, describe a method, report a result, compare evidence, qualify an inference, or state an implication.
- Use a reverse outline to test whether paragraph purposes form a logical sequence.
- Make section and paragraph order reflect the argument, not the order in which the research was conducted.
- Introduce concepts before relying on them. Do not use a label such as `construction-time context` unless it has been defined.
- Distinguish observation, interpretation, comparison, and implication.
- Ensure that every conclusion follows from evidence already presented.

## Paragraph design

### Topic sentence

Open most analytical paragraphs with a sentence containing:

- the topic: what the paragraph concerns; and
- the controlling idea: what the paragraph argues or explains about that topic.

Make the topic sentence broad enough to govern the supporting sentences but specific enough to predict the paragraph's direction. Do not force the topic sentence into first position when a short transition or qualification must come first.

### Development

Develop the controlling idea through evidence, explanation, comparison, examples, or qualification. Keep later sentences tied to the same controlling idea, preferably through clear subject continuity or an explicit lexical chain.

### Information increment

Require each sentence to add information. Delete circular restatement, duplicated conclusions, and sentences that merely rename the previous sentence without advancing the argument.

## Cohesion: connect the text

Treat cohesion as the linguistic connection among clauses and sentences. Use several mechanisms in balance:

- controlled repetition of key technical terms;
- precise synonyms or related word forms when they preserve meaning;
- explicit reference nouns;
- transition signals when the relation is not otherwise clear;
- substitution or ellipsis when the omitted meaning remains unambiguous;
- shell nouns such as `result`, `pattern`, `distinction`, `limitation`, `process`, and `framework`;
- theme-rheme and given-new progression.

Do not pursue lexical variety at the cost of terminological stability.

## Given-new progression

Place familiar or recently introduced information near the beginning of a sentence and the principal new information later. Where useful, turn the new information from one sentence into the point of departure for the next.

Prefer:

> The model produced a high false-positive rate. This error pattern was concentrated in food-therapy titles.

Avoid a sequence in which every sentence begins with an unrelated new subject. Use this principle as a reader-oriented default, not an inflexible template.

## Reference clarity

- Avoid sentence-initial bare `this`, `that`, `these`, or `those` when the referent could be unclear.
- Name the referent: `this result`, `this distinction`, `these errors`, or `this evaluation setting`.
- Check every pronoun against a single unmistakable antecedent.
- Avoid unnecessary repetition within a sentence, but retain repeated technical terms when needed for precision or terminological consistency. Do not replace clear nouns with vague pronouns such as that, which, or it; repeat the technical term or use an explicit reference noun when needed.
- Do not use a retrospective label for information that the preceding text has not named or delimited.

## Agency and grammatical subjects

Choose a subject that makes the actor, operation, and evidence relationship clear.

- Use human or system agents for deliberate actions: `Experts verified the labels against the article text.`
- Use methods or tools as subjects for enabled operations when the relation is literal: `The parser extracted article text.`
- Use data or results as subjects for conventional evidential relations: `The results indicate...`; `The data show...`.
- Avoid vague inanimate agency when it obscures who acted: replace `The article text supports label correction` with `Experts corrected the labels by consulting the article text` when that is the actual procedure.
- Do not attribute intention, judgment, or interpretation to an object unless the wording is conventional and semantically accurate.

## Sentence design

- Put the main actor and main verb where readers can find them quickly.
- Keep modifiers close to the words they modify.
- Use parallel syntax for comparable items, conditions, models, or outcomes.
- Control clause depth. Break a sentence when multiple `that`, `which`, or nested prepositional phrases obscure the main proposition.
- Vary sentence length according to information structure, not for decoration.
- Prefer one clear logical relation per clause.
- Use end weight: place long, complex, or new material later when doing so improves processing.
- Use passive voice when the process or object is more important than the actor, but do not convert active sentences mechanically.
- Use nominalization only when it packages a stable technical concept or improves cohesion. Prefer a strong verb when a nominalization hides the action.

## Transitions

Use transitions to express a real logical relation, not to simulate coherence.

- Cause or purpose: prefer a causal verb or `To address...` when it states the relation directly.
- Contrast: use `while`, `although`, `despite`, `in contrast`, or a contrastive predicate as appropriate.
- Addition: integrate information with `also`, `as well as`, or a parallel construction when a sentence-initial marker is unnecessary.
- Result: prefer verbs such as `led to`, `resulted in`, `enabled`, or `was associated with` when supported by the design.
- Example: use `for example`, `such as`, `including`, `notably`, or `particularly` according to syntax and emphasis.
- Sequence: reserve `first`, `next`, and `finally` for genuine ordered stages or enumerated arguments.

Avoid repetitive paragraph openings such as `However`, `Moreover`, `Therefore`, or `In addition`. Do not replace them with ornate phrases unless the new construction is more precise.

## Vocabulary and academic tone

- Prefer accurate, idiomatic academic English over rare or inflated vocabulary.
- Prefer common, simple, and precise CS/AI terminology. Avoid ornate, uncommon, or unnecessarily sophisticated words when a standard technical term expresses the same meaning clearly.
- Check collocation, argument structure, and disciplinary usage before replacing a familiar word.
- Prefer precise verbs such as `evaluate`, `compare`, `estimate`, `identify`, `derive`, `validate`, `distinguish`, and `synthesize` when they describe the actual operation.
- Avoid vague nouns and verbs such as `thing`, `stuff`, `get`, `do`, `good`, and `bad` when a precise alternative exists.
- Avoid slang, conversational fillers, contractions, unsupported evaluative adverbs, and vague endings such as `and so on` in formal manuscripts.
- Avoid rhetorical questions in research articles unless the venue or section clearly permits them.
- Limit first-person opinion formulas such as `in my opinion`. Use `we` for genuine authorial actions when accepted in the field; do not force passive voice solely to remove it.
- Avoid phrasal verbs when a clearer formal verb exists, but retain standard technical phrasal verbs when replacement would sound unnatural.
- Prefer concrete quantities, dates, thresholds, and sample sizes over vague magnitude or time expressions.
- Use calibrated hedging: `may`, `could`, `appears`, `suggests`, `is consistent with`, or `is associated with` according to evidential strength.
- Do not weaken direct descriptive facts with unnecessary hedging or strengthen observational evidence into causation.

## Tense and voice

- Use present tense for established knowledge, definitions, the paper's current argument, tables, and figures.
- Use past tense for completed data collection, experiments, and observed results.
- Use present perfect selectively for a research development that continues to the present.
- Keep tense stable within a rhetorical move unless the time relation changes.

## Abstracts

Build the abstract as a compact argument rather than a procedural inventory. Include the moves required by the venue, typically:

1. specific context or problem;
2. bounded research gap;
3. objective or contribution;
4. data and method;
5. principal quantitative findings;
6. interpretation or significance.

Apply these rules:

- Begin with the scientific or practical problem, not a generic statement such as `With the rapid development of technology`.
- Introduce every dataset, split, acronym, or metric needed to understand a finding.
- Give the main finding a concrete subject, such as `The best-performing LLM`, `The proposed method`, or `The evaluation`.
- Report the most decision-relevant numbers rather than listing every metric.
- Integrate the main findings into a logical sentence or compact sequence; do not narrate every pipeline step with `Initially`, `After that`, and `Finally`.
- State what the method does and why it matters, not merely the order of operations.
- Avoid repeating the method or conclusion in the final sentence.
- Ensure that every abstract sentence contributes unique information.
- Do not insert citations unless the venue requires them.

## Introductions

Move from the concrete problem to the unresolved gap and then to the present study.

- Establish the practical or theoretical stakes with evidence.
- Narrow the unit of analysis explicitly.
- Distinguish adjacent concepts before using them to motivate the study.
- State a bounded gap rather than claiming that no prior work exists.
- Introduce the research objective before summarizing the design.
- Present contributions as verifiable study outputs, not promotional labels.
- End with the study's scope or evidence boundary when that boundary is central to interpretation.

## Literature reviews and related work

Write a synthesis, not an annotated bibliography.

- Define key concepts and establish why the topic matters.
- Organize studies by theme, method, evidence boundary, finding, or unresolved issue rather than by author sequence.
- Compare what studies examined, what evidence they used, where they agree, and where their conclusions differ.
- Evaluate methods and data before accepting findings as valid.
- Include relevant contrary findings and alternative interpretations.
- Prefer primary sources and seminal work; use secondary sources for synthesis when appropriate.
- Avoid isolated statistics that are not connected to the review's argument.
- End each thematic unit by identifying what the literature establishes and what remains unresolved.
- Link the bounded gap directly to the present study's source, task, evidence, or evaluation design.
- Never attribute a claim to a paper based only on its title, abstract snippet, or another author's summary.

## Methods

- Describe the procedure with enough detail for reproduction.
- Make the actor, input, operation, output, and decision rule explicit.
- Use chronological order only when operational sequence matters.
- Separate construction-time information from evaluation-time inputs.
- Distinguish preprocessing used for model input from processing used only for audit, matching, or analysis.
- State exclusions, frozen choices, tuning boundaries, and leakage controls precisely.
- Cite established algorithms, metrics, software, and model families where an appropriate source exists.

## Results

- Lead with the finding that answers the subsection's question.
- Identify the model, method, dataset, metric, and comparison behind each number.
- Keep descriptive results separate from causal or practical interpretation.
- Report trade-offs rather than selecting a winner from one metric when rankings vary.
- Align every textual value with its table or figure.
- Avoid repeating an entire table in prose; select the values needed for the argument.

## Discussion and conclusion

- Explain what the findings mean within the stated evidence boundary.
- Compare findings with prior work without forcing agreement.
- Distinguish demonstrated implications from plausible applications.
- State limitations specifically and proportionately; do not use them to invalidate results that remain supported.
- Tie future work to an identified limitation, unanswered mechanism, or transfer question.
- In the conclusion, answer the research question and synthesize the principal contribution without introducing new evidence.

## Optional Phrasebank use

The file `2018 Academic Phrasebank 2018 Enhanced Edition (John Morley).pdf` is an optional reference. Do not read it by default. Consult only the relevant section when:

- the user explicitly requests Phrasebank-based wording;
- several precise formulations are needed for a defined rhetorical function;
- wording for cautious claims, comparison, limitation, transition, or section framing remains unresolved after applying this skill.

Use Phrasebank expressions as adaptable patterns, not as evidence or factual content. Do not copy long passages, assemble patchwork prose, or replace clear original wording merely because a template exists.

## Quality-control checklist

Before delivering a revision, verify:

### Integrity

- All numbers, labels, citations, and technical terms match the source.
- No claim has become broader, stronger, more causal, or more novel without evidence.
- No reference or experiment has been invented.

### Coherence

- Each section and paragraph has one identifiable purpose.
- Topic sentences predict the development that follows.
- The argument moves from established information to the unresolved issue and the study's response.

### Cohesion

- Given information anchors each new step where appropriate.
- Key terms form stable lexical chains.
- Pronouns and demonstratives have explicit referents.
- Transitions express genuine relations and are not overused.

### Sentences and wording

- Actors and actions are clear.
- Every sentence adds information.
- Collocations are natural and technical terms are exact.
- Sentence length and clause depth remain readable.
- Hedging matches evidential strength.
- Tense, voice, capitalization, and hyphenation are consistent.

### Section-specific checks

- The abstract contains a clear problem, gap, method, principal finding, and significance.
- Related work synthesizes rather than lists.
- Methods expose inputs, operations, outputs, and boundaries.
- Results match all tables and figures.
- Discussion does not exceed the evidence.

## Delivery behavior

- Return the polished text without unnecessary commentary when the user asks only for a revision.
- Explain only consequential changes involving logic, terminology, evidence, or structure.
- When a sentence is already correct, retain it unless a change clearly improves precision, cohesion, or readability.
- Flag unresolved factual, citation, or terminology questions instead of guessing.
