# Semantic Fidelity Check

This gate decides whether a polished version remains the same scholarly work. Run it after each file and again after the final corrective pass.

## Protected Elements

Compare the original and revision for unchanged:

- citations, citation keys, author-year strings, quotations, footnotes, and bibliography entries;
- all numbers, signs, ranges, percentages, units, dates, thresholds, sample sizes, p-values, confidence intervals, and metric values;
- equations, symbols, variables, LaTeX commands, labels, references, code blocks, filenames, paths, URLs, IDs, model names, dataset names, and version strings;
- table and figure identifiers, values, captions' factual content, and cross-references;
- negation, modality, comparison direction, causal status, novelty status, generalization scope, limitations, and stated uncertainty.

Stylistic reformatting is permitted only when it does not alter these elements or break the source format.

## Claim-Strength Test

For each changed claim, compare:

1. subject and population;
2. action or relation;
3. direction and magnitude;
4. conditions and scope;
5. evidential status;
6. certainty and causality;
7. time and version boundary.

The revision must not move upward in strength without author-supplied evidence. In particular, do not change:

- `may/could` to `does/will`;
- `suggests/is consistent with` to `demonstrates/proves`;
- `is associated with` to `causes`;
- `in this sample/setting` to an unrestricted population;
- `one of the first` to `the first`;
- `improved on metric X` to `outperformed overall`.

## Completeness Test

Confirm that no substantive premise, qualification, exception, limitation, example, or reasoning step disappeared through concision. Shorter is not better when it removes scholarly content.

## Resolution

- If meaning and protected elements match, mark the file `PASS`.
- If a discrepancy is clearly an editing error, repair it and rerun the gate.
- If author judgment or source verification is needed, retain the safer original wording and list the item as unresolved.
- If the environment cannot inspect a protected element, do not claim `PASS`; report the check as incomplete.
