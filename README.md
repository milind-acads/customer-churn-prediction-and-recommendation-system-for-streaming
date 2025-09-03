### Project Title
Streaming Service Customer Churn Prediction and Recommendation Engine

#### Executive summary

This project is for 1) customer churn prediction for a streaming service company and 2) to build a recommendation engine for the users.

Currently, this notebook has steps to perform exploratory data analysis (EDA) on a streaming service customer dataset to understand factors contributing to customer churn. 

The analysis focuses on identifying patterns, relationships, and insights within the data that can inform the development of a churn prediction model. Key areas explored include handling missing values, visualizing churn distribution, analyzing categorical and numerical features, and examining correlations.

This will later be enhanced with models to predict customer churn and provide recommendation engine.

#### Rationale
Why should anyone care about this question?
Understanding customer churn is crucial for streaming services to retain subscribers. By identifying the characteristics and behaviors of customers who churn, the service can implement targeted interventions to reduce churn rates and improve customer satisfaction and loyalty. One such example for reducing the churn is recommendation engine. By recommending the titles that a user may like, provider can potentially increase the services usage which may result in retaining the user for longer time.

#### Key Questions
1) What are the key factors and patterns in the customer data that are associated with churn in the streaming service?
2) Can we predict what a user would like to watch next based on existing reviews and recommend that to the user to improve engagement and therefore reducing the churn?

#### Data Sources
The two data sources for this project are below from kaggle:

1) Streaming Service Data: https://www.kaggle.com/datasets/akashanandt/streaming-service-data?resource=download which contains customer information, subscription details, engagement metrics, and churn status.
2) The Movie Dataset: https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset

#### Methodology
The EDA process involved the following steps:
1.  **Data Loading and Inspection**: Loading the dataset into a pandas DataFrame and inspecting its structure and initial rows.
2.  **Missing Value Handling**: Identifying and imputing missing values in the 'Age' and 'Satisfaction_Score' columns using the mean.
3.  **Churn Distribution Analysis**: Visualizing the distribution of the 'Churned' variable to understand class imbalance.
4.  **Categorical Feature Analysis**: Analyzing the relationship between categorical features (Gender, Region, Payment Method) and churn using count plots.
5.  **Numerical Feature Analysis**: Examining the relationship between numerical features (Age, Subscription Length, Support Tickets Raised, Satisfaction Score, Discount Offered, Last Activity, Monthly Spend) and churn through box plots and summary statistics.
6.  **Correlation Analysis**: Visualizing the correlations between numerical features using a heatmap.

#### Results
The EDA revealed several key findings:
*   Missing values in 'Age' and 'Satisfaction_Score' were successfully handled by imputation with the mean.
*   There is a slight class imbalance in the churn variable.
*   Visualizations provided insights into how churn varies across different genders, regions, and payment methods.
*   Box plots and summary statistics highlighted differences in numerical feature distributions between churned and non-churned customers, notably in 'Satisfaction_Score' and 'Monthly_Spend'.
*   The correlation analysis showed relatively low linear correlations between most numerical features.

#### Next steps
Based on the EDA, the following steps are recommended:
*   Further investigate the features that show potential relationships with churn, such as 'Satisfaction_Score' and 'Monthly_Spend'.
*   Consider feature engineering, such as creating interaction terms or polynomial features, to capture more complex relationships.
*   Address the class imbalance in the churn variable using techniques like oversampling or undersampling when building predictive models.
*   Develop and evaluate various classification models to predict customer churn, using appropriate metrics for imbalanced datasets.
    *   **Modeling**:
        *   Use of multiple machine learning models. Performing hyperparameter tuning using GridSearchCV with cross-validation for Logistic Regression, KNN, Decision Tree, and SVM models to find the best parameters.
        *   Cross-validation of models.
        *   Identification of an evaluation metric.
* Use the movies dataset to build a recommendation system ( using Content-based / Collaborative Filtering, surprise lib, hybrid systems) for users to improve the usage and reduce churn.

#### Outline of project
1.  Load the dataset.
2.  Perform initial data inspection.
3.  Handle missing values.
4.  Visualize churn distribution.
5.  Analyze categorical features and their relationship with churn.
6.  Analyze numerical features and their relationship with churn.
7.  Explore correlations between numerical features.
8.  Summarize key findings and insights.
9.  Define next steps for churn prediction model development and recommendation system development.
