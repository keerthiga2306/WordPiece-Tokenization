# WordPiece-Tokenization
# WordPiece Tokenization From Scratch

## Project Overview

This project implements the **WordPiece Tokenization** algorithm from scratch using Python. WordPiece is a subword tokenization technique used in **BERT** and other Transformer-based language models to split words into meaningful subword units.

The project demonstrates how tokens are created, token pairs are merged, and new words are converted into token IDs without using external NLP libraries.

## Project Objective

The main objective of this project is to understand the working of the WordPiece algorithm by implementing its core steps using Python.

## Features

* Creates an initial vocabulary
* Splits words into subword tokens
* Calculates token frequencies
* Calculates pair frequencies
* Computes WordPiece scores
* Finds the best token pair
* Merges subword tokens
* Builds the vocabulary
* Tokenizes new words
* Converts tokens into token IDs
* Handles unknown words using `[UNK]`

## Technologies Used

* Python
* Collections
* Counter

## Project Structure

```text
WordPiece-Tokenization/
│
├── wordpiece.py
├── README.md
└── requirements.txt
```

## Training Data

```text
hug   → h ##u ##g
hugs  → h ##u ##g ##s
pug   → p ##u ##g
```

## WordPiece Score

The score for each token pair is calculated using:

```text
Score = Pair Frequency / (First Token Frequency × Second Token Frequency)
```

The pair with the highest score is selected and merged into a new token.

## How to Run

### Step 1: Clone the repository

```bash
git clone https://github.com/your-username/WordPiece-Tokenization.git
```

### Step 2: Open the project folder

```bash
cd WordPiece-Tokenization
```

### Step 3: Run the program

```bash
python wordpiece.py
```

## Example

### Input

```text
hugs
```

### Tokenization

```text
hug ##s
```

### Tokens

```python
['hug', '##s']
```

### Token IDs

```text
[7, 5]
```

## Sample Output

```text
Token Frequencies:
Counter({'##u': 4, '##g': 4, 'h': 3, '##s': 1, 'p': 1})

Pair Frequencies:
Counter({
('##u', '##g'): 4,
('h', '##u'): 3,
('##g', '##s'): 1,
('p', '##u'): 1
})

Best Pair: ('h', '##u')

New Token: hu
```

## Working Process

```text
Training Words
      ↓
Split into Subwords
      ↓
Calculate Token Frequencies
      ↓
Calculate Pair Frequencies
      ↓
Compute WordPiece Scores
      ↓
Find Best Pair
      ↓
Merge Tokens
      ↓
Build Vocabulary
      ↓
Tokenize New Word
      ↓
Convert Tokens to IDs
```

## Unknown Token

If a word cannot be fully tokenized using the available vocabulary, the tokenizer returns:

```python
['[UNK]']
```

## Learning Outcomes

* WordPiece Tokenization
* Subword Vocabulary Construction
* Token Frequency Analysis
* Pair Merging Algorithm
* Token ID Generation
* Natural Language Processing Basics
* Python Programming

## Conclusion

This project provides a complete implementation of the **WordPiece Tokenization** algorithm from scratch. It helps in understanding how BERT-style tokenizers create subword vocabularies and represent words as token IDs for NLP applications.

## Author

**Keerthiga K U**

B.Sc. Computer Science with Artificial Intelligence
