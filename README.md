# House Price Prediction using Linear Regression
### Overview
This project focuses on predicting house prices using a linear regression model. The model is built in several steps, including feature engineering, data splitting, model training, and evaluation. The dataset used is from a housing market, and the goal is to predict the SalePrice based on various features. I chose to Implement this project to get practical experience in using regression models.

### Features
The model uses the following features:

- **LotShape** (Categorical)
- **LotConfig** (Categorical)
- **Neighborhood** (Categorical)
- **OverallQual** (Ordinal)
- **OverallCond** (Ordinal)
- **YearRemodAdd** (Numeric)
- **GrLivArea** (Numeric)
- **MoSold** (Ordinal)

### Steps
1. Feature Engineering
Data Cleaning: Dropped duplicates and removed rows with missing values.
One-Hot Encoding: Converted categorical features (LotShape, LotConfig, Neighborhood) into one-hot encoded vectors.
Normalization: Scaled numeric and ordinal features using MinMaxScaler for uniformity.
2. Data Splitting
The dataset is split into training (80%), validation (10%), and test (10%) sets using scikit-learn's train_test_split.
3. Model Training
A linear regression model is trained using scikit-learn's LinearRegression module on the training set.
4. Model Evaluation
Evaluated the model on the validation set using Mean Squared Error (MSE), Mean Absolute Error (MAE), and Pearson correlation coefficient.
Results indicate a strong linear correlation but high MSE and MAE, suggesting that while the model captures trends, its predictions are not highly accurate.
5. Weight Interpretation
Analyzed the weights assigned by the model to each feature. Some features like LotShape had unexpected weight distributions, indicating potential issues with model interpretation.
### Conclusion
While the model demonstrates a strong correlation between predicted and actual prices, the high MSE and MAE suggest it may not be reliable for practical use, especially in high-stakes real estate decisions.

### Future Work
Investigate alternative models or feature engineering techniques to improve prediction accuracy.
Explore the use of more complex models such as decision trees or random forests.
Running the Project
Install dependencies:
bash
Copy code
pip install pandas scikit-learn scipy matplotlib
Run the script to preprocess the data, train the model, and evaluate its performance.
