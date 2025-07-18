# Knights Logic Puzzles

This Python project implements a set of logic puzzles about knights and knaves—classic characters that either always tell the truth (knights) or always lie (knaves). The logic for modeling sentences and checking solutions is implemented from scratch.

## Files Overview

### logic.py

Defines a symbolic logic system, including:
- **Sentence (base class):** Abstract class for logical sentences.
- **Symbol:** Represents a logical variable (e.g., "A is a Knight").
- **Not, And, Or, Implication, Biconditional:** Logical operators for combining sentences.
- **model_check:** Recursively determines whether a knowledge base entails a query by evaluating all possible models (truth assignments).

### puzzle.py

Defines four classic knights and knaves logic puzzles:
- Each character (A, B, C) can be either a Knight or a Knave, represented as Symbols.
- Each puzzle creates a knowledge base using the logic classes from `logic.py` to encode the constraints.
- The `main()` function runs each puzzle, checking which roles for each character are entailed by the puzzle’s information.

## Usage

Run the solver:
```bash
python puzzle.py
```
The script will print out which characters are knights or knaves in each puzzle, per logical deduction.

## Requirements

- Python 3.x

No external dependencies.

## How it works

- Logical statements (such as "A says 'I am both a knight and a knave'") are represented using the logic primitives in `logic.py`.
- For each puzzle, a knowledge base is constructed by combining the appropriate logical statements.
- The model checking algorithm exhaustively tests all possible truth assignments to determine which roles are necessarily true.

