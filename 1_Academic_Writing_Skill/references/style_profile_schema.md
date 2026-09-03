# Style Profile Schema

Adapted from `academic-research-skills/shared/handoff_schemas.md`, Schema 10. It retains the complete six-dimension Style Calibration output while replacing pipeline-specific handoff fields with a portable Markdown artifact.

## Required Fields

| Field | Type | Description |
|---|---|---|
| `calibration_source` | list[string] | Filenames or titles of the analyzed writing samples |
| `sample_count` | integer | Number of samples analyzed (minimum 1, recommended 3+) |
| `sentence_length` | object | `{mean: float, stddev: float, rhythm_pattern: string}` |
| `paragraph_length` | object | `{mean_sentences: float, variation: string}` |
| `vocabulary_preferences` | object | `{hedging_words: list[string], transition_words: list[string], preferred_verbs: list[string], formality: string}` |
| `citation_style` | object | `{narrative_ratio: float, parenthetical_ratio: float, density: float, placement: string}` |
| `modifier_style` | enum | `minimal`, `moderate`, or `elaborate` |
| `register_shifts` | list[object] | `[{section_name: string, assertiveness_level: string}]` |

## Optional Fields

| Field | Type | Description |
|---|---|---|
| `conflicts_with_discipline` | list[string] | Conflicts between personal style and discipline or venue norms |
| `partial_profile` | boolean | `true` when fewer than three samples were analyzed |
| `language_mismatch` | boolean | `true` when samples use a different language from the target |

## Consumption Priority

```text
Priority 1 (HARD):   Discipline conventions
Priority 2 (STRONG): Target-venue conventions, when specified
Priority 3 (SOFT):   Author's personal style, where compatible
```

## Portable Markdown Form

```markdown
# Style Profile

**Calibration Source**: ["sample_1", "sample_2", "sample_3"]
**Sample Count**: 3

**Sentence Length**: mean: 22, stddev: 8, rhythm: "variable"
**Paragraph Length**: mean 5 sentences, variation: "moderate"
**Vocabulary Preferences**:
  - Hedging: suggests, appears to, may
  - Transitions: However, In contrast, Yet
  - Reporting verbs: found, argued, noted
  - Formality: moderate-formal
**Citation Style**: narrative 40%, parenthetical 60%, density 2.3/paragraph, placement: mixed
**Modifier Style**: minimal
**Register Shifts**: [Methods: neutral, Results: descriptive, Discussion: assertive]
**Conflicts**: <none or documented conflicts>
**Partial Profile**: false
**Language Mismatch**: false
```

Save this artifact as `STYLE_PROFILE.md` in the requested output directory or another explicitly named reusable location.
