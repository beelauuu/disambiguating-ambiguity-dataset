# Ambiguous Sentences Dataset

A comprehensive collection of syntactically ambiguous English sentences with labeled interpretations and ambiguity types.

## Overview

This dataset contains **90 ambiguous sentences**, each with 2-3 possible interpretations. The sentences demonstrate various types of linguistic ambiguity commonly studied in computational linguistics, natural language processing, and semantic analysis.

## Dataset Statistics

- **Total Sentences**: 90
- **Ambiguity Types**: 10 categories
- **Format**: JSON and CSV

### Ambiguity Type Distribution

| Type | Count | Description |
|------|-------|-------------|
| PP-ATTACH | 19 | Prepositional phrase attachment ambiguity |
| STRUCT | 14 | Structural/syntactic ambiguity |
| LEXICAL | 14 | Lexical/word-level ambiguity |
| COMPARE | 9 | Comparative construction ambiguity |
| TEMPORAL | 9 | Temporal reference ambiguity |
| SCOPE | 6 | Quantifier/negation scope ambiguity |
| PRONOUN | 7 | Pronoun reference ambiguity |
| COORD | 5 | Coordination ambiguity |
| CAUSAL | 3 | Causal relationship ambiguity |
| RECIPROCAL | 4 | Reciprocal interpretation ambiguity |

### JSON Format (`ambiguous_sentences_dataset.json`)

```json
{
  "sentence": "The girl watched the boy with the telescope",
  "ambiguity_type": "PP-ATTACH",
  "interpretations": [
    "The girl had a telescope",
    "The boy had a telescope"
  ]
}
```

### CSV Format (`ambiguous_sentences_dataset.csv`)

Columns: `sentence`, `ambiguity_type`, `interpretation_1`, `interpretation_2`, `interpretation_3`
