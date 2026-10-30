# CSL2050 Pattern Recognition & Machine Learning — Labs (Winter 2022)

Lab assignments from the Jan–Apr 2022 offering.

Each `LAB-NN_*` folder has:

- `question.pdf` — the assignment handout
- `data/` — datasets the lab uses
- `solution.ipynb` — the solution, executed, with all outputs
- `report.tex` / `report.pdf` — the write-up (LaTeX), built from `figures/` and `results.json`

| Lab | Topic | Highlights |
|---|---|---|
| 01 | Python, NumPy, pandas, plotting, evaluation metrics | Cars93 cleaning & encoding; metrics from scratch match sklearn |
| 02 | Decision trees | ID3 tree from scratch (entropy), 98.6% on penguins; regression-tree tuning |
| 03 | Bagging & boosting | CART from scratch, bagging, RF, AdaBoost, XGBoost, LightGBM depth/leaves analysis |
| 04 | Bayes classification | Mixed (categorical + Gaussian) Naive Bayes from scratch on Titanic; seeds posteriors |
| 05 | QDA, LDA, Gaussian MLE, text Naive Bayes | 20 Newsgroups multinomial NB from scratch, 80.8% |
| 06 | PCA & LDA from scratch | Jacobi eigen-solver; ROC/AUC from scratch on the anneal dataset |
| 07 | Neural networks | Two-branch PyTorch net (abalone); MLP from scratch with backprop (Dry Bean, 91.3%) |
| 08 | ICA & sequential feature selection | ICA from scratch separates the three audio sources (\|r\| > 0.9997); SFS from scratch |
| 09 | Clustering | k-means from scratch on Fashion-MNIST; Ward vs k-means on brain MRI |
| 10 | SVM | Linear / quadratic / RBF kernels on Spambase, 95.5% with log features |

## Running

The notebooks use the virtual environment at the repository root:

```bash
cd ~/IITJ && source .venv/bin/activate      # numpy, pandas, scikit-learn, torch, xgboost, lightgbm, mlxtend
```

In VS Code / Jupyter, pick the kernel **"PRML (venv)"**. Run each notebook from its own lab folder (paths are relative to it).
Reports compile with `pdflatex report.tex` (run twice).

## Data notes

- **LAB-05** `data/20news/` — the bag-of-words 20 Newsgroups files (`train.data`, `test.data`, labels, vocabulary).
- **LAB-08** `data/Q1/` — the three source recordings; `outputs/` holds the mixtures and separated signals as WAV.
- **LAB-09** `data/fashion_mnist/` — Fashion-MNIST in the original IDX format (from zalandoresearch/fashion-mnist).
  `data/Q3/br35h_64x64.npz` — the Br35H brain-MRI set (1 500 tumour / 1 500 healthy), converted once to 64×64 greyscale
  to keep the repository small (the original 3 000 JPEGs are 71 MB).
