# Fuel Cell Performance Prediction - Target5

## Problem Statement

The task involves using the **Fuel_cell_performance_data-Full.csv** dataset to predict the performance of fuel cells based on different targets. The dataset is divided into 5 different target categories based on roll numbers, and the goal is to apply regression models to predict the values for **Target5**.

### Target Definitions:
- **Target1**: Roll Numbers ending with 0 or 5
- **Target2**: Roll Numbers ending with 1 or 6
- **Target3**: Roll Numbers ending with 2 or 7
- **Target4**: Roll Numbers ending with 3 or 8
- **Target5**: Roll Numbers ending with 4 or 9 *(This is the target I worked on)*

### Dataset and Setup:
- **Dataset**: [Fuel_cell_performance_data-Full.csv](./Fuel_cell_performance_data-Full.csv)
- **Target**: Target5 (Roll number - 102203804)
- **Notebook**: [Regression_Targets.ipynb](./Regression_Targets.ipynb)
- **Plots**: Visualizations are stored in the [plots](./plots) folder.

### Task Overview:
1. **Dataset Split**: The dataset is divided into a training (70%) and testing (30%) set.
2. **Modeling**: Multiple prediction models were used to predict **Target5**.
3. **Model Evaluation**: Results were evaluated based on various metrics, including R-squared, Mean Absolute Error (MAE), Standard Deviation of Error, Maximum Absolute Error, and Median Absolute Error.

## Result Submission
- **Final Evaluation Table**:

| Model        | R-squared | MAE    | Std Dev of Error | Max Abs Error | Median Abs Error |
|--------------|-----------|--------|------------------|---------------|------------------|
| **CatBoost** | 0.7811    | 14.8276| 21.1452          | 98.4383       | 10.1270          |
| **Random Forest** | 0.7730 | 15.0386| 21.5354          | 107.8291      | 10.2331          |
| **Gradient Boosting** | 0.7664 | 15.7206 | 21.8442      | 100.2885      | 11.1736          |
| **Extra Trees** | 0.7653  | 15.0291 | 21.8979          | 121.9464      | 10.7970          |
| **LightGBM**  | 0.7544    | 15.2411| 22.4019          | 105.4545      | 9.3029           |

- **Evaluation Metrics**: Models were evaluated based on their **R-squared** values, and the table above is sorted by **R-squared** in descending order.

## Files and Folders
1. **Fuel_cell_performance_data-Full.csv**: The dataset used for the analysis.
2. **Regression_Targets.ipynb**: Jupyter notebook containing the model building, training, and evaluation.
3. **Plots Folder**: Contains the visualizations of the model results (e.g., residual plots, error distributions, predicted vs. actual plots).
   
## Conclusion:
In this project, multiple regression models were applied to predict **Target5** from the given dataset. The **CatBoost model** achieved the highest **R-squared** value of **0.7811**, showing the best performance among the models tested.

---

### How to Run:
1. Download the **Fuel_cell_performance_data-Full.csv** dataset.
2. Open the **Regression_Targets.ipynb** notebook in Jupyter or Google Colab.
3. Run the cells to train the models and generate the evaluation table.

---

### Acknowledgments:
- This analysis was conducted using multiple regression models such as **CatBoost**, **Random Forest**, **Gradient Boosting**, **Extra Trees**, and **LightGBM**.
