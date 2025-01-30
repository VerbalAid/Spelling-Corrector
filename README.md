# **Spelling Correction with Python**

## **Overview**

This project implements a simple spell checker using Python. It utilizes **tokenization**, **word frequency analysis**, and **edit distance calculations** to suggest the most probable correction for misspelled words.

## **Features**

- **Tokenizes** text and creates a **frequency table** from a large corpus (**big.txt**).
- Generates possible **spelling corrections** based on:
  - **Known words** in the corpus
  - **Words one or two edits away**
- Selects the **most probable correction** based on **word frequency**.

## **Usage**

Ensure **big.txt** (a large text corpus) is in the same directory.

Import the script and use the `rectify` function:

```python
from spell_checker import rectify

corrected_word = rectify("speling")
print(corrected_word)  # Output: "spelling"
```

## **How It Works**

### **Tokenization & Frequency Analysis:**

- Reads **big.txt** and **counts occurrences** of words.

### **Generating Possible Corrections:**

- Checks if the **word exists** in the corpus.
- If not, generates words with **one or two edits**.

### **Probability-Based Selection:**

- Chooses the **correction with the highest frequency** in the corpus.

## **Dependencies**

- **Python 3**

## **Acknowledgment**

Inspired by **Peter Norvig’s spell checker algorithm and concepts from Packt Publishing's tutorial**.

