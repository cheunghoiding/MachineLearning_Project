# MachineLearning_Project
Car Insurance Claims Classification using machine learning models.
The purpose of this machine learning model is to determine classify using a binary classification system, the likelihood a customer will make claims on their car insurance based on their features.

## Data Collection
Car Insurance Data from Kaggle Dataset by Sagnik Roy:
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

## Logistic Regression Model
- use the training data to fit into the logistic regression model
- method for binary classification problems
- accuracy score is 84%
<img width="620" alt="Screenshot 2021-10-27 at 9 30 08 AM" src="https://user-images.githubusercontent.com/84705479/138984684-4e64b0b9-8019-45ba-8e0a-8e99b452a67b.png">

## K-Nearest Neighbours Model
- Use GridSearchCV to identify optimal n_neighbours
- Input 16 dimensions of x and regress with y label
- Compute and compare recall score of 0.68
- Possible next step:
  - Majority voting → Distance voting
<img width="836" alt="Screenshot 2021-10-27 at 9 31 54 AM" src="https://user-images.githubusercontent.com/84705479/138984804-72621923-ec92-449f-af7b-c6aabc50dfc7.png">
<img width="327" alt="Screenshot 2021-10-27 at 9 31 58 AM" src="https://user-images.githubusercontent.com/84705479/138984816-c281f539-de13-4db2-a975-f79fcfb5041e.png">
<img width="277" alt="Screenshot 2021-10-27 at 9 32 02 AM" src="https://user-images.githubusercontent.com/84705479/138984823-687f1fc4-4613-43c4-9fd7-199051e53448.png">

## Decision Tree Model
- Root Node, Decision Nodes, & Terminal Nodes (Leaf Nodes)
- Recursive Binary Splitting based on:
  - Information Gain
  - Loss functions: Entropy, Gini index
<img width="1141" alt="Screenshot 2021-10-27 at 9 34 35 AM" src="https://user-images.githubusercontent.com/84705479/138984990-a79ebf3d-f80a-47fd-861f-eb0bbbbabb0d.png">
- Using GridSearchCV for hypertuning the parameters
- max_depth, min_sample_split, & min_sample_leaf
<img width="1106" alt="Screenshot 2021-10-27 at 9 35 01 AM" src="https://user-images.githubusercontent.com/84705479/138985085-747d8f97-df88-42e3-83d0-e36f2be90063.png">

## Random Forest Ensemble Model
- Random forest is a classification algorithm consisting of many decisions trees.
- It uses bagging and feature randomness when building each individual tree to try to create an uncorrelated forest of trees, which is more accurate than any individual tree.
<img width="636" alt="Screenshot 2021-10-27 at 9 37 07 AM" src="https://user-images.githubusercontent.com/84705479/138985176-2afae5e9-269f-433a-aef0-4f02428c8e98.png">
- We chose to build 300 trees after CV and 8 min sample leaf, which is minimum 8 samples in a leaf and the accuracy we got is 83.96%.

## Model Evaluation & Comparison
<img width="986" alt="Screenshot 2021-10-27 at 9 38 41 AM" src="https://user-images.githubusercontent.com/84705479/138985295-be4d7b43-eb97-4d05-a959-8268da22925a.png">

## Conclusion & Future Improvements
Business Application
- Our model can classify if a potential insurance purchaser will claim a payout.
- This enables us to quickly segment customers into claimers and non-claimers.
- After segmentation, we can apply a secondary model that can calculate expected payout values, in order to determine the required price for each insurance client.
