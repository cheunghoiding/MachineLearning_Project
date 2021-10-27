# MachineLearning_Project
Car Insurance Claims Classification using machine learning models.
The purpose of this machine learning model is to determine classify using a binary classification system, the likelihood a customer will make claims on their car insurance based on their features.

## Data Collection
Car Insurance Data from Kaggle Dataset by Sagnik Roy
- https://www.kaggle.com/sagnik1511/car-insurance-data
<img width="1034" alt="Screenshot 2021-10-27 at 9 24 39 AM" src="https://user-images.githubusercontent.com/84705479/138984214-b67e179c-d37b-4cd3-a4fa-aa138c1aaa36.png">

## Data Preprocessing

1. Feature scaling
  - Since the range of mileage is quite different from other columns, we have make a standard scaler to scale all columns.
2. Label encoding
  - Encode categorical features and define numerical order of categorical values.
3. Clean missing values
  - “Credit_Score” & “Annual Mileage” features had some missing values, which was filled with the mean value for the respective column.
4. Drop columns
  - “ID” & “Postal Code” features removed since they seem to have no impact on the outcome.
<img width="371" alt="Screenshot 2021-10-27 at 9 25 41 AM" src="https://user-images.githubusercontent.com/84705479/138984320-5d427915-6062-4fad-ba36-075bab53ed09.png">
<img width="1122" alt="Screenshot 2021-10-27 at 9 25 51 AM" src="https://user-images.githubusercontent.com/84705479/138984327-a9428abd-ce5f-4aac-9434-7ccc2adb421c.png">
<img width="1150" alt="Screenshot 2021-10-27 at 9 26 01 AM" src="https://user-images.githubusercontent.com/84705479/138984337-1b435943-216f-48e1-9ffe-e02b4652a2a6.png">
