# Character-Level Name Generation

I built a character-level linear language model in PyTorch that supports different context sizes, then used it to run experiments and compare model performance.

For this project, I tested two configurations:
- **Bigram:** `block_size=1`
- **Linear Trigram:** `block_size=2`

I ran 24 training experiments with different learning rates, training steps, and regularization strengths. I compared the results, selected the best configuration for each model using validation loss, and evaluated both on the test set.

## Results

| Model | Test Loss |
|---|---|
| Bigram | 2.4608 |
| Linear Trigram | 2.3506 |

The Linear Trigram performed better, although both models still generate some unrealistic names.

## How to Run

1. Install `torch`, `pandas`, and `matplotlib`.
2. Open `character-level-name-generation.ipynb` in Jupyter, VS Code, or Google Colab.
3. Run all cells in order. The dataset (`names.txt`) is included in the repository. If using Google Colab, upload `names.txt` to the session first.

## Credits

This project started from Andrej Karpathy's *Building makemore* lecture and exercises.

**From Karpathy:** The names dataset, the core character-level modeling approach, and parts of the original encoding, training, and sampling code.

**My implementation:** A generalized model supporting variable context sizes, reusable training and evaluation functions, automated hyperparameter search, model selection, and a train/dev/test comparison pipeline.

**Original resources:**
- [Neural Networks: Zero to Hero](https://github.com/karpathy/nn-zero-to-hero)
- [Original makemore notebook](https://github.com/karpathy/nn-zero-to-hero/blob/master/lectures/makemore/makemore_part1_bigrams.ipynb)
- [Dataset](https://github.com/karpathy/makemore)