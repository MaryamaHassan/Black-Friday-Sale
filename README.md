---

## Black Friday Sale Dataset: Data Cleaning

### Overview

In this project, I focused on cleaning the Black Friday sale dataset to address missing values and prepare the data for further analysis. The dataset contains information about customer purchases, product categories, and other relevant features. I employed various strategies to handle missing data, including visualisation techniques, imputation methods, and outlier detection.

### Key Steps in the Data Cleaning Process:

1. **Loading the Data:**
   I began by loading the dataset and inspecting its structure to understand the types of data and identify any missing values.

2. **Visualising Missing Data:**
   To assess where the missing values were located, I used a heatmap. This provided a clear view of which columns had missing data, helping to identify patterns in the missingness.

3. **Outlier Detection:**
   For columns like `Product_Category_2`, I applied Z-score-based outlier detection. This allowed me to remove extreme values that could affect the imputation process, ensuring that the remaining data was more reliable for filling missing values.

4. **Handling Missing Data:**
   I used several methods to handle the missing data:
   - **Dropping Rows/Columns**: In some cases, I removed rows or columns with missing values, especially when the percentage of missing data was low.
   - **Filling Missing Values**: For columns with more significant missing data, I filled the missing values using different strategies:
     - **Zero Filling**: For columns where zero was a reasonable assumption.
     - **Median, Mean, and Mode Imputation**: I filled missing values using the median, mean, or mode for numerical columns. Each method was chosen based on the distribution of the data and the nature of the missingness.

5. **Saving Cleaned Data:**
   After cleaning the data, I saved the dataset using different imputation techniques (mean, median, mode) to separate CSV files for future use.

### Conclusion

This project demonstrates various techniques for handling missing data in a real-world dataset. By visualising the missing values, detecting outliers, and applying appropriate imputation methods, the dataset was successfully cleaned and is now ready for further analysis. Future work could involve further outlier analysis, feature engineering, and building predictive models based on the cleaned data.

### Next Steps:
- Further outlier analysis and data transformations
- Feature engineering for improved predictive modelling
- Developing models to forecast sales based on the cleaned data

---
