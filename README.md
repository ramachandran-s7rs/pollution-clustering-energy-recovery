# pollution-clustering-energy-recovery
Clustering countries by pollution (K-Means, Hierarchical) and predicting energy recovery with a Keras neural network
# Global Pollution Analysis and Energy Recovery – Clustering and Neural Networks

Analyzing pollution data across countries with **K-Means** and **Hierarchical (Agglomerative) clustering**, and testing how well pollution-related factors predict **energy recovery (GWh)** with a **Keras neural network** compared to linear regression.

## Project Workflow

**Phase 1 – Data Preprocessing and Feature Engineering**
- Cleaning and median/mode imputation
- Label encoding of Country and Year
- Scaling of air, water and soil pollution indices; composite pollution score
- Energy consumption per capita
- Yearly pollution trend analysis vs. energy recovery

**Phase 2 – Clustering**
- K-Means with the Elbow Method and silhouette scores to choose K
- Hierarchical clustering (Ward linkage) with a dendrogram
- Cluster profiling by pollution, energy use and energy recovery
- Comparison of the two methods (silhouette, Davies-Bouldin, Calinski-Harabasz, Adjusted Rand Index)

**Phase 3 – Neural Network for Energy Recovery**
- Feedforward network (Keras/TensorFlow) predicting energy recovered in GWh
- Hyperparameter search over layers, neurons, activation, learning rate and dropout (3-fold CV with early stopping)
- Compared against linear regression and a predict-the-mean baseline (R², MSE, MAE)

**Phase 4 – Reporting and Insights**
- Comparison of clustering-based prediction and neural network
- Strengths and weaknesses of each method
- Strategy recommendations generated from the results

## Method Notes

- Clusters are built from the three pollution indices and energy consumption per capita. Energy recovery is **not** used to form clusters, so it can be used to profile them and for a fair comparison with the neural network.
- Imputation and scaling for the supervised models are fitted on the training set only; hyperparameters are chosen with cross-validation on the training set, and the test set is used once at the end.

## Results

*(Fill in after running the notebook on the real dataset.)*

| Model | R² | MSE | MAE |
|---|---|---|---|
| Mean baseline | – | – | – |
| Linear Regression | – | – | – |
| Baseline Neural Network | – | – | – |
| Tuned Neural Network | – | – | – |
| K-Means cluster average | – | – | – |

| Clustering | Silhouette | Davies-Bouldin | Calinski-Harabasz |
|---|---|---|---|
| K-Means | – | – | – |
| Hierarchical | – | – | – |

## Limitations

- The dataset has only about 200 country-year records, so clusters and neural-network results can change with a different split or seed.
- Clusters describe patterns; they do not show that pollution causes higher or lower energy recovery.
- An R² at or below 0 means a model is no better than predicting the average.

## Dataset

`Global_Pollution_Analysis.csv` should be placed in the project root next to the notebook.
Download link: https://drive.google.com/file/d/1AEMcCWzJ24fc26Q761SEOa1sOsZiJBC5/view?usp=sharing
