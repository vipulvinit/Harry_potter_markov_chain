# Harry Potter Story Generator with Markov Chains

This project implements a Markov Chain model to predict and generate text based on a dataset of Harry Potter stories. By analyzing the dataset and building a probabilistic model, the program can generate plausible story fragments that align with the patterns found in the source material.

## Features
- **Preprocessing Text**: The script reads and cleans the input text files, removing punctuation and non-alphabetic tokens.
- **Markov Chain Model**: Constructs an n-gram Markov Chain model from the cleaned dataset.
- **Text Generation**: Generates new Harry Potter-inspired story fragments by sampling from the Markov Chain.

---

## Prerequisites

Before running the script, ensure you have the following installed:

1. Python 
2. [NLTK](https://www.nltk.org/) (Natural Language Toolkit)
   - Used for tokenizing words.

Install NLTK using pip if not already installed:
```bash
pip install nltk
```

---

## Directory Structure

Make sure your project directory has the following structure:
```
Markov Chain/
├── harry-potter-dataset/
│   ├── story1.txt
│   ├── story2.txt
│   └── ...
├── markov_chain_model.py (your script)
```

- **`harry-potter-dataset/`**: Folder containing the Harry Potter stories in `.txt` files.
- **`markov_chain_model.py`**: The main Python script for this project.

---

## How to Run

1. Place all `.txt` files containing Harry Potter stories in the `harry-potter-dataset` directory.
2. Update the `story_path` variable in the script to match the path to your dataset folder:
   ```python
   story_path = r"C:\path\to\harry-potter-dataset"
   ```
3. Run the script:
   ```bash
   python markov_chain_model.py
   ```

---

## Workflow

### 1. Read and Clean Text Data
The script:
- Reads all `.txt` files in the dataset directory.
- Tokenizes and cleans the text to remove punctuation and non-alphabetic words.

### 2. Build the Markov Chain Model
The model:
- Creates an n-gram-based Markov Chain from the cleaned text.
- Calculates transition probabilities for each state.

### 3. Generate Stories
Using the Markov Chain model, the script generates text fragments based on a given starting phrase.

---

## Key Functions

1. **`read_all_stories(story_path)`**  
   Reads all `.txt` files from the dataset directory and extracts lines of text.

2. **`clean_txt(txt)`**  
   Cleans and tokenizes the text data, removing punctuation and non-alphabetic tokens.

3. **`make_markov_model(cleaned_stories, n_gram=2)`**  
   Constructs the Markov Chain model using n-grams.  
   - **Input**: List of cleaned words.  
   - **Output**: A dictionary representing the Markov Chain.

4. **`generate_story(markov_model, limit, start)`**  
   Generates a story of a specified word limit starting with a given phrase.

---
