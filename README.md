# Whisper Normalization

A Python package for text normalization, specifically designed for use with Whisper models.

**Note:** This code is extracted from [OpenAI's Whisper repository](https://github.com/openai/whisper) to allow for standalone usage of the text normalization modules without the heavy dependencies of the full Whisper package.

- Original Source: [openai/whisper](https://github.com/openai/whisper)
- License: MIT

## Installation

You can install this package directly from source:

```bash
pip install .
```

## Usage

```python
from whisper_normalization import EnglishTextNormalizer, BasicTextNormalizer

# English Normalization
normalizer = EnglishTextNormalizer()
text = "Mr. Smith bought $5.50 worth of apples in the 1990s."
normalized = normalizer(text)
print(normalized)
# Output: "mister smith bought five dollars and fifty cents worth of apples in the nineteen nineties"

# Basic Normalization
basic_normalizer = BasicTextNormalizer()
text = "Bonjour à tous!"
normalized = basic_normalizer(text)
print(normalized)
```

## Features

- Basic text cleaning (symbol removal, diacritic handling)
- Advanced English normalization:
  - Number to text conversion (integers, decimals, currencies, years)
  - Contraction expansion
  - Abbreviation expansion
  - British to American spelling normalization
