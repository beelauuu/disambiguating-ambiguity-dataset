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

## File Formats

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

## Ambiguity Types Explained

### PP-ATTACH (Prepositional Phrase Attachment)
Ambiguity in how prepositional phrases attach to different parts of the sentence.
- Example: "I saw the man with the binoculars"
  - Using binoculars to see
  - The man had binoculars

### STRUCT (Structural/Syntactic)
Ambiguity arising from different syntactic structures.
- Example: "The shooting of the hunters was terrible"
  - Someone shot the hunters
  - The hunters were doing the shooting

### LEXICAL (Lexical/Word-level)
Ambiguity from words with multiple meanings.
- Example: "Flying planes can be dangerous"
  - The act of piloting planes
  - Planes that are in flight

### COMPARE (Comparative)
Ambiguity in comparative constructions.
- Example: "I like visiting relatives more than my sister"
  - More than sister likes visiting
  - More than I like visiting sister

### TEMPORAL (Temporal Reference)
Ambiguity in time-related expressions.
- Example: "He's been working since 12"
  - Since 12:00 (time)
  - Since age 12

### SCOPE (Quantifier/Negation Scope)
Ambiguity in the scope of quantifiers or negation.
- Example: "Two students read every book"
  - Two specific students read all books
  - Each book was read by two students

### PRONOUN (Pronoun Reference)
Ambiguity in pronoun antecedents.
- Example: "Sarah told Emily that she got the promotion"
  - Sarah got it
  - Emily got it

### COORD (Coordination)
Ambiguity in coordinated noun phrases.
- Example: "Blue shirts and pants were donated"
  - Both blue
  - Only shirts are blue

### CAUSAL (Causal Relationship)
Ambiguity in causal or reason clauses.
- Example: "I didn't go to the store because I was tired"
  - Went but not for that reason
  - Didn't go; tiredness was why

### RECIPROCAL (Reciprocal Interpretation)
Ambiguity in reciprocal actions.
- Example: "John and Mary got married"
  - To each other
  - Each married someone else

## Use Cases

This dataset is useful for:

- **NLP Research**: Testing disambiguation algorithms
- **Semantic Parsing**: Training and evaluating parsers
- **Language Models**: Benchmarking understanding of ambiguity
- **Linguistics Education**: Teaching syntactic ambiguity
- **Annotation Studies**: Inter-annotator agreement studies
- **Question Answering**: Testing contextual understanding

## Loading the Dataset

### Python (JSON)
```python
import json

with open('ambiguous_sentences_dataset.json', 'r') as f:
    data = json.load(f)

for item in data:
    print(f"Sentence: {item['sentence']}")
    print(f"Type: {item['ambiguity_type']}")
    print(f"Interpretations: {item['interpretations']}")
    print()
```

### Python (CSV)
```python
import pandas as pd

df = pd.read_csv('ambiguous_sentences_dataset.csv')
print(df.head())
```

### R
```r
library(jsonlite)
data <- fromJSON('ambiguous_sentences_dataset.json')

# Or with CSV
data <- read.csv('ambiguous_sentences_dataset.csv')
```

## Citation

If you use this dataset in your research, please cite:

```bibtex
@dataset{ambiguous_sentences_2024,
  title={Ambiguous Sentences Dataset},
  author={[Your Name]},
  year={2024},
  publisher={GitHub},
  url={https://github.com/[your-username]/ambiguous-sentences-dataset}
}
```

## License

[Choose an appropriate license, e.g., MIT, CC-BY-4.0]

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request with:
- Additional ambiguous sentences
- New ambiguity types
- Corrections or improvements to existing interpretations

## Acknowledgments

This dataset was compiled for research in computational semantics and natural language understanding.

## Contact

For questions or suggestions, please open an issue on GitHub.
