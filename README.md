### Comprehensive Report on Predictive Modelling: K-Nearest Neighbours and Random Forest Regression  

This report outlines the development of predictive models using K-Nearest Neighbours (KNN) and Random Forest (RF) regression to forecast purchase amounts based on the Black Friday Sale Dataset. It covers every stage, from data preparation to model evaluation, providing insights into the methodologies and results of both approaches.  

---

### Data Cleaning and Preprocessing  

The dataset was cleaned and prepared before modelling. This involved identifying and handling missing values, detecting outliers, and resolving inconsistencies. Missing values were addressed with various imputation techniques, such as zero-filling for logical gaps and mean, median, or mode imputation for numerical fields. Outliers were identified using Z-scores, and extreme values were removed to minimise distortion. A heatmap visualisation further revealed patterns in missing data.  

To prepare the data for machine learning, categorical variables were encoded using one-hot encoding. The data was then divided into training and testing sets in an 80-20 ratio to facilitate model training and evaluation.  

---

### K-Nearest Neighbours Regression  

The KNN regression model was trained to predict purchase amounts. Since KNN is sensitive to feature scales, the dataset was standardised before training. A grid search approach was employed to determine the optimal number of neighbours, with cross-validation ensuring reliable results.  

- **Best Hyperparameters:** n_neighbors = 9  
- **Model Evaluation:**  
  - Mean Absolute Error (MAE): 2168.66  
  - Root Mean Squared Error (RMSE): 2933.38  
  - R-squared: 0.655  

The KNN model exhibited moderate performance, explaining approximately 65.5% of the variance in purchase amounts. While the scatter plot of actual versus predicted values revealed some discrepancies, the model's overall performance was reasonable.  

#### Residuals Analysis  
The histogram of residuals (differences between actual and predicted values) is presented below. It demonstrates a near-normal distribution, centred around zero, which indicates that the KNN model's errors are largely unbiased and symmetrically distributed. However, the presence of residuals at the extremes suggests that the model struggles with some outlier predictions.  

![Actual vs Predicted Values with KNN](https://github.com/user-attachments/assets/fc704eda-23fb-4a77-ab83-2ba86ca5f1e0)
![Residuals Distribution](https://github.com/user-attachments/assets/08bd5fd3-4ca5-4dec-a785-f75d5e81dc83)

---

### Random Forest Regression  

Random Forest regression, a tree-based ensemble model, was also implemented. Since Random Forest is scale-invariant, no feature scaling was required. A grid search combined with cross-validation optimised the number of trees and tree depth for the model.  

- **Best Hyperparameters:** Selected via cross-validation with grid search.  
- **Model Evaluation:**  
  - Mean Absolute Error (MAE): 2062.80  
  - Root Mean Squared Error (RMSE): 2760.86  
  - R-squared: 0.694  

Random Forest outperformed KNN, explaining 69.4% of the variance in purchase amounts. Scatter plots of actual versus predicted values demonstrated closer alignment compared to KNN, affirming the model's robustness. 

![Top Feature Importance](https://github.com/user-attachments/assets/2b9506be-ba3b-4404-a03d-f114521c734b)

---

### Model Comparison and Conclusion  

The Random Forest model delivered better predictive performance than the KNN model, as reflected by a higher R-squared value and lower RMSE. While both models captured patterns in the data, Random Forest proved more effective, especially in handling complex relationships and outliers.  

Both models were evaluated with metrics like MAE, RMSE, and R-squared, complemented by scatter plot visualisations to assess performance. The trained models were saved for future use, ensuring they can be deployed without retraining.  

The project successfully demonstrated the process of predictive modelling, starting from meticulous data cleaning to comprehensive evaluation of models. Random Forest emerged as the superior approach, but both methods underscored the importance of robust preprocessing and hyperparameter tuning in machine learning. This report highlights the critical role of data-driven insights in decision-making and the power of predictive analytics in real-world scenarios.
