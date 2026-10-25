# Heart Health Risk Explorer

This project explores cardiovascular health data from the Framingham study in a Jupyter notebook. It uses regression, classification, and clustering to examine blood pressure, 10-year coronary heart disease (CHD) risk, and patient groups.

## Project structure

```text
.
├── Data/
│   └── framingham.csv
├── Notebooks/
│   └── Heart_Attack.ipynb
└── README.md
```

## Notebook workflow

Run [Notebooks/Heart_Attack.ipynb](Notebooks/Heart_Attack.ipynb) to explore:

1. **Linear regression** — predicts systolic blood pressure (`sysBP`) from selected patient characteristics.
2. **Logistic regression** — estimates the probability of a 10-year CHD event (`TenYearCHD`), with cross-validation to select model parameters.
3. **Classification evaluation** — reviews accuracy, a confusion matrix, ROC/AUC, and the effect of different risk thresholds.
4. **Clustering** — compares K-means and hierarchical clustering on selected health measures.
5. **Cluster interpretation** — trains a decision tree to approximate the K-means group assignments and compares clusters by CHD rate.

The notebook also discusses model interpretability and the limits of applying a model trained on one population to another.

## Data

The dataset is [Data/framingham.csv](Data/framingham.csv). It contains 3,658 records and Framingham risk factors, including age, sex (`male`), smoking, blood pressure, cholesterol, BMI, glucose, and the `TenYearCHD` outcome. The CSV has an unnamed leading column in addition to its named fields.

## Setup and run

Use Python 3 with Jupyter Notebook or JupyterLab. The notebook imports NumPy, pandas, seaborn, Matplotlib, scikit-learn, and SciPy.

From the project root, install the dependencies and launch Jupyter from the `Notebooks` directory so the notebook's `../Data/framingham.csv` path resolves:

```bash
python -m pip install numpy pandas seaborn matplotlib scikit-learn scipy jupyter
cd Notebooks
jupyter notebook Heart_Attack.ipynb
```

Run the notebook cells in order.

## Important note

This is an educational data-analysis project, not a clinical tool. Its model outputs are not medical advice and should not be used to diagnose or guide treatment.
