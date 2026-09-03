---
name: academic-language-polishing
description: Polish academic manuscripts from a user-specified file or directory while preserving claims, evidence, citations, numbers, equations, terminology, and document structure. Use for English or Chinese academic language polishing, copyediting, prose-quality audits, batch manuscript polishing, or optional author-style calibration from writing samples. Do not use it to fabricate content, strengthen unsupported claims, or evade AI detection.
---

# Academic Language Polishing

Improve the language and rhetorical delivery of an existing academic text without changing the study. This skill is platform-neutral: follow the same contract in any AI environment that can read the named files and write the requested outputs.

## Load the Complete Polishing Rules

Before rewriting any academic prose, read all four core references. None is optional in `polish` mode:

1. [references/academic_writing_style.md](references/academic_writing_style.md) — precision, concision, register, hedging, transitions, paragraphs, tense, and disciplinary conventions.
2. [references/writing_judgment_framework.md](references/writing_judgment_framework.md) — paragraph value, reader journey, disciplinary voice, section purpose, and revision decisions.
3. [references/writing_quality_check.md](references/writing_quality_check.md) — the complete terminology, punctuation, opener, structure, and sentence-rhythm sweep.
4. [references/semantic_fidelity_check.md](references/semantic_fidelity_check.md) — protected content and the post-revision fidelity gate.

For a directory target, also read [references/directory_polishing_protocol.md](references/directory_polishing_protocol.md). For author-style matching, also read [references/style_calibration_protocol.md](references/style_calibration_protocol.md) and [references/style_profile_schema.md](references/style_profile_schema.md).

Do not silently omit a rule because it is inconvenient, because the manuscript is long, or because a particular model cannot finish the whole directory in one pass. Split the work into traceable batches and finish every batch under the same rules.

## Modes

- `polish` (default): revise the text and run all quality and fidelity gates.
- `audit`: diagnose issues and give targeted recommendations without changing source files.
- `style-profile`: analyze the supplied writing samples and produce `STYLE_PROFILE.md`; do not polish the target unless requested.
- `polish-with-profile`: create or load a Style Profile, then polish with it as a soft guide.

Infer the mode from the request when clear. A named directory is the complete scope boundary, not permission to edit its parent or unrelated files.

## Non-Negotiable Content Boundary

- Preserve the author's intellectual contribution, meaning, stance, uncertainty, and scope.
- Preserve all citations, quotation boundaries, numbers, units, equations, symbols, model and dataset names, identifiers, labels, cross-references, URLs, file paths, code, and table/figure values.
- Never invent evidence, references, experiments, results, mechanisms, limitations, or causal explanations.
- Never strengthen a descriptive or correlational statement into a causal one, or turn a qualified claim into a universal claim.
- Do not rewrite quoted text, bibliography entries, source code, mathematical expressions, or venue-required boilerplate unless the user explicitly requests that exact change.
- Treat AI-pattern signals only as prose-quality cues. Never promise that output is human-written, undetectable, or able to bypass an AI detector.

When a useful language improvement conflicts with semantic fidelity, keep the original meaning and flag the unresolved wording.

## Working Sequence

1. Resolve the exact input, output, mode, target language, discipline, venue, and intervention level. Use the request as authority; do not expand scope.
2. Inventory the target before editing. For directories, follow the directory protocol and preserve relative paths.
3. Record the protected factual and technical surface defined in the fidelity check.
4. If style samples are provided, build the six-dimension Style Profile before polishing. Apply the priority order: discipline norms (hard) > target-venue conventions (strong) > personal style (soft).
5. Diagnose from macro to micro: section purpose, paragraph function, sentence-to-sentence flow, agency and referents, wording, syntax, punctuation, and rhythm.
6. Revise only as much as the selected intervention level requires. Retain text that is already precise, natural, and structurally sound.
7. Run the entire Writing Quality Check across the assembled output, not merely on isolated edited sentences. Apply every exception in that checklist; do not replace legitimate technical terms mechanically.
8. Run the Semantic Fidelity Check against the original. Revert or repair any unsupported meaning change.
9. Re-read the revised work as continuous prose and perform one corrective second pass. The second pass must also pass the fidelity gate.
10. Write outputs and a concise `POLISHING_REPORT.md` according to the directory protocol. Report unresolved factual or formatting risks instead of guessing.

## Intervention Levels

- `light`: grammar, spelling, punctuation, collocation, and unmistakable local ambiguity.
- `standard` (default): light editing plus sentence design, transitions, paragraph cohesion, concision, and academic register.
- `deep`: standard editing plus paragraph reordering or local restructuring. Preserve the same claims and evidence; flag any change that would require author judgment.

Language polishing alone does not authorize adding new arguments, deleting substantive content, checking the truth of citations, or redesigning the research narrative.

## Delivery Contract

For a single passage returned in chat, present the polished text first and explain only consequential meaning, evidence, or terminology decisions.

For file or directory work:

- keep originals unchanged unless the user explicitly requests in-place editing;
- mirror the input structure in the output location;
- preserve the source format only when the environment can round-trip it safely;
- list processed, unchanged, skipped, and failed files in `POLISHING_REPORT.md`;
- include material structural changes, style-profile use, protected-content checks, and unresolved questions;
- never claim a check was completed when the required file or tool could not be read.

Use [TASK_REQUEST_TEMPLATE.md](TASK_REQUEST_TEMPLATE.md) as a portable request format for any AI agent.
