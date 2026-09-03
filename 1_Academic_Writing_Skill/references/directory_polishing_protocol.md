# Directory Polishing Protocol

Use this protocol whenever the user supplies a directory rather than a single pasted passage.

## 1. Resolve Scope

Treat the normalized absolute input path as the hard boundary. Do not read or write sibling or parent directories except for an explicitly named output directory or style-sample directory.

Resolve these fields from the request:

- `input`: required file or directory;
- `output`: explicit path, or a sibling named `<input-name>_polished` when omitted;
- `mode`: `polish`, `audit`, `style-profile`, or `polish-with-profile`;
- `intervention`: `light`, `standard`, or `deep`;
- `language`, `discipline`, and `target_venue`: use `unspecified` when absent;
- `style_samples`: optional, and separate from the manuscript input.

Do not default to in-place editing. If in-place editing is explicitly requested, create a recoverable pre-edit copy before the first write and record its location.

## 2. Inventory Before Editing

Recursively list files, preserve their relative paths, and classify them:

- Directly editable prose: `.md`, `.txt`, `.rst`, `.tex` and other plain-text manuscript formats.
- Editable with safe document tooling: `.docx`, `.odt`, or equivalent only when the environment can preserve layout, notes, citations, tracked elements, and embedded objects.
- Read-only context or style samples: `.pdf` unless a safe PDF-editing workflow is available and explicitly requested.
- Protected support files: `.bib`, CSL files, code, data, images, tables exported as data, and generated build artifacts. Read only when needed; do not polish them by default.

Skip the output directory itself and common generated or dependency directories such as `.git`, `.svn`, `node_modules`, `build`, `dist`, `_build`, caches, and temporary lock directories. Do not follow links that escape the input boundary.

Before editing, state the number of files in each class and any format limitation. A long directory may be processed in stable batches, but every batch must use the same glossary, Style Profile, and protected-content rules.

## 3. Establish Shared Context

Build a compact run-level context before rewriting:

- canonical technical terms, abbreviations, capitalization, and hyphenation;
- section and document order;
- target language and discipline register;
- recurring claims, uncertainty markers, and evidence boundaries;
- optional Style Profile;
- files or spans that must remain untouched.

Use this context across all files to prevent term drift. Do not use content from one paper to introduce claims into another.

## 4. Process Each File

For every editable file:

1. Record its original relative path and source format.
2. Identify protected regions: frontmatter, code blocks, equations, LaTeX commands, citations, reference lists, quotations, tables, captions, labels, and cross-references.
3. Apply the requested intervention level to prose only.
4. Run the complete core references from `SKILL.md`.
5. Compare revised content with the original using the Semantic Fidelity Check.
6. Write to the mirrored output path. Do not flatten directory structure or change extension unless format conversion was explicitly requested.
7. Record status as `processed`, `unchanged`, `skipped`, or `failed`, with a short reason.

When a binary document cannot be round-tripped safely, do not silently convert it or discard formatting. Mark it `skipped` or produce a separately named review artifact only if the user requested a fallback.

## 5. Cross-File Pass

After all files are processed, verify across the complete output:

- terminology, abbreviations, capitalization, and spelling are consistent;
- the same claim has not acquired different strength in different files;
- labels, links, citations, and cross-references still resolve as before;
- output files do not contain temporary notes, model chatter, or editing instructions;
- no input file was missed merely because a batch ended.

## 6. Output Manifest

Create `POLISHING_REPORT.md` in the output directory with:

```markdown
# Polishing Report

- Input: <absolute input path>
- Output: <absolute output path>
- Mode / intervention: <values>
- Language / discipline / venue: <values>
- Style Profile: <not used | path and sample count>

## File Results
| Relative path | Status | Notes |
|---|---|---|

## Material Changes
- <only changes affecting structure, terminology, claim presentation, or author review>

## Fidelity Gate
- Protected elements checked: <summary>
- Unresolved items: <none or list>
```

Keep the report concise. Do not turn it into a sentence-by-sentence diff unless requested.
