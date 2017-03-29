Proposal – Walmart Sales Forecasting

Problem:
Walmart is a multinational retail corporation that operates globally. Walmart runs several promotional markdown events throughout the year. These markdowns precede prominent holidays, the four largest of which are the Super Bowl, Labor Day, Thanksgiving, and Christmas. The weeks including these holidays are weighted five times higher in the evaluation than non-holiday weeks. Walmart would like to forecast sales data by store and department using historical store sales data for 45 Walmart stores.

Client:
Walmart is the client. Based on forecast sales, Walmart will determine if more employees are needed during high sales days. Also, the analysis will help Walmart determine if additional resources should be allocated to the departments that have low sales.

Data:
Historical data is obtained from 45 Walmart stores without geographic information. Only store features, store types, historical sales data (train data set) and test data set (for predictions and final deliverable) are provided. Data is acquired through Kaggle (https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting).

Approach to Solving Problem:
The tool used to solve this problem is Jupyter and the scripting language is Python. Jupyter notebook and Python will be used for data analysis, data discovery, visualization, and determining the best fit time series model. The following is an approach to solving the problem:

1)Exploratory analysis  
    a. Data Pre-processing 
    b. Visualize the data to discover trends  
    c. Determine subset to use for training the model  
2) Test Harness  
    a. Partition Dataset into Training & Validation  
    b. Determine Model Evaluation and Metrics  
        - weighted mean absolute error (WMAE)   
3) Persistence Model – establish a baseline of performance measure by which all more predictive models can be compared  
4) Model Selection and Fitting – data is fitted to each model and residual errors reviewed   
    a. AR Model (Autoregression)  
    b. MA Model (Moving Average)          
    c. ARIMA Model (Autoregressive Integrated Moving Average)  
    d. SARIMA Model (Seasonal Autoregressive Integrated Moving Average Model)  
5) Model Evaluation – Determine best model using WMAE  
6) Model Validation  
    a. Finalize Model - train and save the final model  
    b. Make Prediction - load the finalized model and make a prediction  
    c. Validate Model - load and validate the final model  
7) Prepare the results of the final model for delivery  

Deliverables:
The test dataset will contain the weekly sales prediction by store and department.

For each row in the test set (store + department + date triplet), the weekly sales of that department should be predicted. The file should have a header and looks like the following:

    Id,Weekly_Sales  
    1_1_2012-11-02,0  
    1_1_2012-11-09,0  
    1_1_2012-11-16,0  

