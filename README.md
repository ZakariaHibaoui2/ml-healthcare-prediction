# Healthcare ML — Diabetes & Autism Screening Prediction

> Supervised and unsupervised machine learning on two healthcare datasets: interpretable decision trees for **diabetes prediction**, K-Means + PCA patient segmentation, and a **Random Forest autism-screening desktop app**.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0)
![Tkinter](https://img.shields.io/badge/GUI-Tkinter-2C3E50)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Notebooks

| # | Notebook | Technique | Highlights |
|---|---|---|---|
| 1 | [Supervised learning](notebooks/01_supervised_learning_decision_tree.ipynb) | Decision Tree (gini/entropy, depth tuning) on the Pima diabetes data | EDA, tree visualisation, extracted human-readable **decision rules**, train-vs-test comparison that exposes overfitting, feature importance |
| 2 | [Unsupervised learning](notebooks/02_unsupervised_learning_kmeans_pca.ipynb) | K-Means clustering + PCA | Elbow method, silhouette score (0.18), 2-D PCA projection of patient clusters, cluster profiling |
| 3 | [Autism screening app](notebooks/03_autism_screening_app.ipynb) | Random Forest + Tkinter GUI | Cleans `?` values and outliers, label-encodes answers, trains and **pickles** the model, then serves predictions in a desktop form |
| 4 | [Autism screening app v2](notebooks/04_autism_screening_app_v2.ipynb) | Same pipeline, refined UI | Improved input validation and layout |

## Datasets

| File | Description |
|---|---|
| `data/diabetes.csv` | Pima Indians Diabetes dataset: 768 patients, 8 clinical features (glucose, BMI, insulin, age…) |
| `data/autism_screening.csv` | Adult autism screening (AQ-10 answers + demographics), UCI ML Repository |
| `models/autism_model.pkl` | Trained Random Forest used by the screening app |

## Getting started

```bash
git clone https://github.com/ZakariaHibaoui2/ml-healthcare-prediction.git
cd ml-healthcare-prediction
pip install -r requirements.txt
jupyter notebook
```

Notebooks 1–2 were written for Google Colab (`drive.mount`). Locally, skip that cell and point `pd.read_csv` to `data/`.

> ⚕️ Educational project, not a medical diagnostic tool.

## Author

**Zakaria Hibaoui** — [GitHub](https://github.com/ZakariaHibaoui2) · [LinkedIn](https://www.linkedin.com/in/zakaria-hibaoui-08b235337/)

## License

[MIT](LICENSE)
