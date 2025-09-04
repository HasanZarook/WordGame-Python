# Word Game (MIT 6.0001 Problem Set 3)

This project is a text-based implementation of a Scrabble-like **Word Game**.
It was built as part of **MIT 6.0001 (Introduction to Computer Science in Python)**.

Players form words from a given hand of letters, score points based on Scrabble letter values, and can substitute/replay hands.

---

## 📂 Project Structure

```
.
├── ps3.py            # Main game logic (functions to implement)
├── ps3_test.py       # Unit tests for scoring, updating hands, and word validity
├── words.txt         # Dictionary file with valid words
├── helper_versions/  # Earlier versions showing step-by-step solutions
│   ├── wordgame_v1.py
│   ├── wordgame_v2.py
│   ├── wordgame_v3.py
│   └── wordgame_v4.py
└── README.md         # Project documentation
```

---

## ⚙️ Features

* **Word Scoring** – Based on Scrabble letter values and bonus rules.
* **Hand Management** – Letters are randomly dealt, with option to substitute.
* **Wildcard Support** – `*` can be used as any vowel in words.
* **Word Validation** – Checks if a word is valid and possible with given hand.
* **Interactive Gameplay**:

  * Play multiple hands
  * Substitute one letter (once per game)
  * Replay one hand (once per game)
* **Unit Tests** – Validate correctness of scoring, updating, and word checks.

---

## ▶️ How to Run

1. Clone or download this project.

2. Make sure you have **Python 3** installed.

3. Ensure `words.txt` (dictionary file) is in the same folder as `ps3.py`.

4. Run the main game:

   ```bash
   python ps3.py
   ```

   Example:

   ```
   Loading word list from file...
     83667 words loaded.
   Enter total number of hands: 1
   Current Hand: a r * d t o p
   Would you like to substitute a letter? yes
   Which letter would you like to replace? *
   Enter word, or "!!" to indicate that you are finished:
   ```

5. Run tests:

   ```bash
   python ps3_test.py
   ```

---

## 🧪 Example Test Output

```
----------------------------------------------------------------------  
Testing get_word_score...
SUCCESS: test_get_word_score()
----------------------------------------------------------------------  
Testing update_hand...
SUCCESS: test_update_hand()
----------------------------------------------------------------------  
Testing is_valid_word...
SUCCESS: test_is_valid_word()
----------------------------------------------------------------------  
Testing wildcards...
SUCCESS: test_wildcard()
All done!
```

---

## 📖 Rules Recap

* Letter values follow Scrabble.
* Score for a word:

  ```
  score = (sum of letter values) × max(1, (7 × wordlen) − (3 × (n − wordlen)))
  ```
* `*` acts as any vowel (a, e, i, o, u).
* Replay hand → only once per game.
* Substitute letter → only once per game.

---

## 🔧 Requirements

* Python 3.x
* No external libraries required (only `math`, `random`, `string`).

---
