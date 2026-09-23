# Machine Learning From Scratch

A practical, code-first path to learning machine learning by building the important ideas yourself.

This repository is designed to help you understand **why machine learning works**, not just how to call a library. Start with the mathematics, implement small algorithms with NumPy, test them on real datasets, and only then compare your work with established libraries such as scikit-learn.

## What You Will Learn

- Python and NumPy for numerical computing
- Linear algebra, probability, statistics, and calculus for ML
- Data cleaning, visualization, and feature engineering
- Supervised learning: regression and classification
- Unsupervised learning: clustering and dimensionality reduction
- Model evaluation, validation, and avoiding data leakage
- Optimization, regularization, and the bias-variance tradeoff
- The foundations of neural networks and deep learning

## Learning Path

### 1. Build the foundations

Before implementing models, become comfortable with:

- Python functions, classes, modules, virtual environments, and testing
- NumPy arrays, broadcasting, vectorization, and matrix operations
- Matplotlib and pandas for exploration
- Git and the command line

Recommended mathematics:

- **Linear algebra:** vectors, matrices, dot products, projections, eigenvalues
- **Calculus:** derivatives, gradients, the chain rule
- **Probability:** random variables, expectation, variance, Bayes' theorem
- **Statistics:** distributions, sampling, correlation, confidence intervals

You do not need to master every proof before writing code. Learn each idea, implement it, and return to the theory when your experiments raise a question.

### 2. Learn the complete ML workflow

For every project, follow the same loop:

1. Define the problem and choose a measurable target.
2. Collect and inspect the data.
3. Split the data into training, validation, and test sets.
4. Establish a simple baseline.
5. Preprocess features using training data only.
6. Train a model.
7. Evaluate with metrics appropriate to the problem.
8. Inspect errors and improve one thing at a time.
9. Record assumptions, results, and next steps.

This workflow matters as much as the algorithm. A sophisticated model cannot rescue a poorly defined problem or a misleading evaluation.

### 3. Implement core algorithms

Suggested order:

1. Mean, variance, covariance, and correlation
2. Linear regression with the normal equation
3. Linear regression with gradient descent
4. Logistic regression
5. k-nearest neighbors
6. Naive Bayes
7. Decision trees
8. Random forests and boosting concepts
9. k-means clustering
10. Principal component analysis (PCA)
11. A single-layer perceptron
12. A small neural network trained with backpropagation

For each implementation, include:

- A short explanation of the mathematics
- Input and output shapes
- A small synthetic example
- Tests for important edge cases
- A comparison with a trusted implementation
- A note about time and space complexity

## Getting Started

### Requirements

- Python 3.10 or newer
- Git
- Basic command-line knowledge

### Create an environment

```bash
git clone https://github.com/your-username/ML-From-Scratch.git
cd ML-From-Scratch

python -m venv .venv
source .venv/bin/activate       # Linux/macOS
# .venv\\Scripts\\activate      # Windows PowerShell

python -m pip install --upgrade pip
python -m pip install numpy pandas matplotlib scikit-learn jupyter pytest
```

When this project gains a dependency file, prefer installing from it:

```bash
python -m pip install -r requirements.txt
```

## A Good First Project

Implement linear regression without using a machine learning library.

1. Generate a small dataset with a known linear relationship and some noise.
2. Implement the mean squared error function.
3. Implement predictions, gradients, and gradient descent.
4. Plot the loss after every iteration.
5. Check that the loss decreases and the learned parameters approach the known values.
6. Compare the result with `sklearn.linear_model.LinearRegression`.
7. Repeat the experiment with unscaled features and explain what changes.

This one project introduces data, a loss function, optimization, visualization, debugging, and evaluation.

## Evaluation Cheat Sheet

| Task | Useful first metrics | Important question |
| --- | --- | --- |
| Regression | MAE, MSE, RMSE, $R^2$ | How large are typical prediction errors? |
| Binary classification | Accuracy, precision, recall, F1, ROC-AUC | Which error is more costly: a false positive or false negative? |
| Multiclass classification | Accuracy, macro F1, confusion matrix | Are some classes being ignored? |
| Clustering | Silhouette score, domain inspection | Do the clusters make sense in context? |

Never choose a metric only because it is easy to calculate. Choose it based on the real cost of mistakes.

## Project Ideas

### Beginner

- Predict house prices with linear regression.
- Classify flower species with k-nearest neighbors.
- Detect spam using Naive Bayes.

### Intermediate

- Predict customer churn and investigate class imbalance.
- Cluster customers and describe each segment.
- Reduce image dimensions with PCA and visualize the result.

### Advanced

- Build a neural network for handwritten digit classification.
- Create a reusable preprocessing and evaluation pipeline.
- Compare several models with cross-validation and a documented error analysis.

Use public datasets from sources such as the UCI Machine Learning Repository, Kaggle, or OpenML. Read the dataset license and document the source.

## Recommended Resources

- [An Introduction to Statistical Learning](https://www.statlearning.com/) — gentle statistical foundation with practical examples
- [Mathematics for Machine Learning](https://mml-book.github.io/) — linear algebra, calculus, and optimization
- [Hands-On Machine Learning](https://github.com/ageron/handson-ml3) — practical workflows with modern Python tools
- [scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html) — reliable reference implementations and explanations
- [Dive into Deep Learning](https://d2l.ai/) — neural networks with code and interactive material

## Working Principles

- Prefer a small, correct implementation over a large framework.
- Make experiments reproducible with fixed random seeds where appropriate.
- Keep training, validation, and test data separate.
- Normalize or standardize features when the algorithm needs it.
- Plot data and errors; numbers alone often hide problems.
- Write tests for both normal inputs and awkward edge cases.
- Treat library implementations as references, not replacements for understanding.
- Document what failed. Failed experiments are useful evidence.

## Suggested Repository Structure

```text
ML-From-Scratch/
├── README.md
├── notebooks/              # Explanations and experiments
├── src/                    # Reusable implementations
│   └── ml_from_scratch/
├── tests/                  # Unit and numerical checks
├── data/                   # Small, documented datasets or download scripts
├── projects/               # End-to-end experiments
└── requirements.txt
```

## Progress Checklist

- [ ] Set up Python, Git, and a virtual environment
- [ ] Review NumPy, pandas, and plotting basics
- [ ] Implement descriptive statistics from scratch
- [ ] Implement linear regression and gradient descent
- [ ] Complete one regression project
- [ ] Implement and evaluate two classification algorithms
- [ ] Learn cross-validation and feature preprocessing
- [ ] Implement k-means and PCA
- [ ] Build a small neural network
- [ ] Publish one project with clear documentation and reproducible steps

## Contributing

Improvements are welcome. Keep examples focused, explain the underlying idea, add tests for new implementations, and avoid hiding the core algorithm behind a library call.

## License

Add a license before distributing code or datasets from this repository.