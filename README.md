# Neural Architecture Dynamics: A Systematic Analysis of Hyperparameter Effects on MLP Performance

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/downloads/)

## Overview
A comprehensive empirical investigation into the behavioral dynamics of multilayer perceptron (MLP) architectures under varying hyperparameter conditions. This research provides detailed analysis of activation functions, learning rate algorithms, and batch size configurations, with particular emphasis on their effects on model convergence and classification robustness using the Iris dataset.

## Key Research Areas
- Comparative analysis of activation function performance and convergence characteristics
- Learning rate algorithm optimization and stability analysis
- Batch size impact on gradient descent variants
- Model architecture optimization and hidden layer analysis
- Classification performance benchmarking using the Iris dataset

## Project Structure
```
neural-architecture-dynamics/
├── neuralnet_analysis.ipynb    # Main research notebook with implementations and visualizations
├── iris.csv                    # Dataset
├── requirements.txt            # Project dependencies
├── venv/                       # Virtual environment
└── __pycache__/               # Python cache files
```

## Key Findings

### Activation Function Analysis
- Tanh activation demonstrates fastest convergence but lower accuracy compared to other functions
- ReLU shows consistent performance with unperturbed data but significant degradation with negative perturbations
- Logistic activation achieves optimal performance with single hidden layers but shows vanishing gradient issues in deeper architectures

### Learning Rate Dynamics
- Adaptive learning rate algorithms show superior stability with high initial learning rates
- Inverse scaling learning rate performs optimally with large batch sizes (100+)
- Constant learning rate (0.001) shows best performance in standard gradient descent (batch size = 1)

### Architecture Insights
- Single hidden layer with 100 neurons proved optimal for the classification task
- Multiple hidden layers showed signs of overfitting without significant performance improvement
- Batch normalization significantly reduces model sensitivity to initial parameter values

## Technologies Used
- Python 3.7+
- NumPy
- Pandas
- Scikit-learn
- Matplotlib/Seaborn
- Jupyter Notebook

## Getting Started
1. Clone the repository
```bash
git clone https://github.com/[your-username]/neural-architecture-dynamics.git
```

2. Create and activate virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook
```bash
jupyter notebook
```

## Documentation
The complete research analysis is available in two formats:
- Interactive Jupyter Notebook (`neuralnet_analysis.ipynb`)
- Detailed technical write-up documenting methodology and findings
