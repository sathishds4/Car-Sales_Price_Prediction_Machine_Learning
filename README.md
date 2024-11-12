# Car-Sales_Price_Prediction_Machine_Learning
Car Sales Price Prediction using Machine Learning
Overview:
This project aims to predict the price of cars based on various features like model, engine type, transmission, color, dealer region, and more. By leveraging machine learning models, we are able to create a predictive system that estimates the car prices with high accuracy, based on historical data and trends.

Objective:
To develop a predictive model that can accurately estimate the price of a car based on various features such as:

Model: The make and model of the car.
Engine Size: The type and capacity of the car's engine.
Transmission Type: Whether the car is automatic or manual.
Color: The color of the car.
Body Style: The design and structure of the car (e.g., Sedan, SUV).
Dealer Region: The location or region where the car is sold.
Annual Income: The financial background of the car owner or buyer (helps in pricing the car to match target customer demographics).
Year and Month: The year and month the car was sold, which may indicate seasonal trends or market variations.
Data Processing:
The dataset contains multiple columns representing various attributes of the cars:

Categorical Variables: Such as Gender, Dealer_Name, Company, Model, Engine, Transmission, Color, Body Style, Dealer_Region.
Numerical Variables: Such as Annual Income, Year, Month.
These features are preprocessed using the following methods:

Missing Value Handling: Imputation is performed for missing data. For numerical columns, the median is used, while for categorical columns, the most frequent category is used.
Scaling: Numerical columns are scaled using StandardScaler to normalize the data.
Encoding: Categorical variables are transformed into numeric form using one-hot encoding.
Modeling:
A Random Forest Regressor model is used for price prediction. This model is suitable for regression tasks due to its ability to handle large datasets with complex relationships and its ability to prevent overfitting.

The model is fine-tuned using Grid Search to find the best hyperparameters, such as:

n_estimators: The number of trees in the forest.
max_depth: The maximum depth of each tree.
min_samples_split: The minimum number of samples required to split an internal node.
Performance Evaluation:
The model’s performance is evaluated using:

R-squared (R²): Measures how well the model explains the variance in the target variable (price). A higher value indicates a better fit.
Mean Absolute Error (MAE): The average of absolute differences between predicted and actual prices, showing the model's accuracy.
Final Model:
After hyperparameter tuning and cross-validation, the best-performing model is saved using joblib to facilitate easy loading and reuse in production. The final model can predict the price of a car based on new input data, helping businesses or users make informed pricing decisions.

Applications:
Car Dealerships: Can use the model to set competitive prices for cars based on historical trends and market data.
Pricing Optimization: Helps businesses optimize car prices in real-time based on available features.
Consumer Insights: Provides buyers with price predictions based on car features to make better purchasing decisions.
