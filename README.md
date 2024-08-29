# FIFA-Predictive-Insight
roject Description
Purpose:
The primary objective of this project is to utilize advanced data science techniques to predict key performance metrics for FIFA23 players, specifically focusing on overall ratings and optimal positions. This project encompasses two main tasks, each aimed at leveraging different approaches and models to achieve accurate predictions.
Problem/Motivation:
In the world of professional football and gaming, accurately assessing and predicting player performance metrics, such as overall ratings and optimal positions, is crucial. Managers, scouts, and enthusiasts rely heavily on these metrics for team selection, player development, and gaming strategies. However, predicting these metrics with high accuracy remains a significant challenge due to the dynamic and multifaceted nature of player performance.

Impact:
For Football Managers and Scouts:
Enhanced Decision-Making: Accurate predictions of player ratings and best positions can significantly improve team formation and player recruitment strategies.
Player Development: Insights into optimal player positions can guide training programs and career development, maximizing player potential and performance.
Cost Efficiency: Better predictions can lead to more informed investment decisions, reducing the financial risks associated with player transfers.
For Gaming Enthusiasts:
Improved Gaming Experience: More accurate player metrics enhance the realism and enjoyment of football simulation games.
Strategic Advantage: Players can leverage accurate predictions to build stronger teams and improve their gameplay strategies.


#Research Tasks:
Task 1 - Predicting Players' Overall Ratings Using Diverse Attributes:
Task Goal: Predicting players' overall ratings using their diverse attributes.
For this task, we explored two different approaches:
Approach 1: We aimed to predict a player's overall rating based on their previous year data. This involved predicting a player's rating using historical data from the previous year.
Approach 2: In contrast, we aggregated player data across multiple years into a single dataset. This approach allowed us to predict total rating scores for players without prior historical data, leveraging the aggregated insights from past years.
These approaches provided different perspectives: Approach 1 focused on temporal prediction using recent data, while Approach 2 utilized aggregated historical data to infer ratings for players without specific historical records. Each method offered unique insights into player rating prediction strategies based on varying data utilization strategies.
Models: To achieve this, we chose Gradient Boosting and XGBoost models due to their robust ensemble learning capabilities, which improve predictive accuracy by combining multiple weak learners and optimizing computational resources.
Evaluation Metrics: MSE, MAE, and R-squared.


Task 2 - Predicting Players' Best Position:
Task Goal: In this task, we aim to classify players into their best playing positions using various machine learning models. The classification task involves analyzing player attributes to determine their most suitable position on the field.
Models and Evaluation: We focused on three models: Decision Tree, Random Forest, and XGBoost, evaluating their performance using metrics such as precision, recall, F1-score, and support. 
We worked to identify which model performs best in predicting player positions and understand the challenges in classifying certain positions. Our approach included generalizing similar positions to balance the dataset.

#Results and Running Times:
Task 1 – Predicting Players' Overall Ratings Using Diverse Attributes – Results:


Approach 1: Predicting a player's overall rating based on their previous year's data
Gradient Boosting Training Time: 11.510992527008057 seconds.
XGBoost Training Time: 8.48201322555542 seconds.
MSE and MAE: The XGBoost model outperformed the Gradient Boosting model with significantly lower Test MSE and Test MAE, indicating that XGBoost has, on average, smaller errors in its predictions.
R-squared (R^2): The R^2 score of the XGBoost model on the test set is higher than that of the Gradient Boosting model. This suggests that the XGBoost model explains a larger proportion of the variance in the target variable.
Overall Conclusion: Given these results, XGBoost appears to be a more effective choice for predicting player ratings. Its superior performance metrics, ability to handle complex relationships in the data, and optimized training process make it the recommended model for further refinement and deployment in our predictive modeling efforts.


Approach 2: Aggregating player data across multiple years to predict overall ratings for players without prior historical data
Gradient Boosting Training Time: 10.949445962905884 seconds.
XGBoost Training Time: 5.926482439041138 seconds
MSE and MAE: The XGBoost model demonstrated better performance than the Gradient Boosting model, with notably lower Test MSE and Test MAE, indicating smaller errors in its predictions.
R-squared (R^2):  The R^2 score of the XGBoost model on the test set is higher than that of the Gradient Boosting model. This implies that the XGBoost model explains a greater proportion of the variance in the target variable.
Overall Conclusion: The results indicate that XGBoost is a more effective model for predicting player ratings when using aggregated historical data. Its superior accuracy and ability to handle complex patterns in the data make it the preferred model for future development and deployment in our predictive modeling tasks.


Task 2 – Predicting Players' Best Position – Results:


Model 1 – Decision Tree:
Training Time: 5.514211654663086 seconds.
Macro F1-score of Decision Tree is: 0.75.
Accuracy: 77%.


Model 2 – Random Forest:
Training Time: 19.883801221847534 seconds
Macro F1-score of Random Forest is: 0.79.
Accuracy: 82%.


Model 3 – XGBoost:
Training Time: 13.99955677986145 seconds.
Macro F1-score of XGBoost is: 0.86.
Accuracy: 88%.



#Conclusions:


Task 1 - Predicting Players' Overall Ratings Using Diverse Attributes – Conclusions:
The task was approached using two different approaches, each evaluated using Gradient Boosting and XGBoost models.
Across both approaches, XGBoost consistently outperformed Gradient Boosting in terms of accuracy (MSE and MAE) and explanatory power (R^2). The results demonstrate that XGBoost is more capable of handling complex relationships and provides more accurate predictions of players' overall ratings. The superior performance metrics and efficient training times make XGBoost the preferred model for further refinement and deployment in predictive modeling tasks related to player ratings. Future work can focus on fine-tuning XGBoost hyperparameters and exploring additional features to enhance model performance further.
When comparing the two approaches, aggregating player data across multiple years (Approach 2) proved to be slightly more effective than predicting based on the previous year's data (Approach 1). Although both approaches demonstrated strong predictive capabilities, Approach 2 had a more comprehensive dataset that captured a broader range of player attributes over time, leading to improved model performance. The XGBoost model in Approach 2 achieved higher R^2 scores and lower error rates, indicating that this method is better suited for capturing the complexities and variations in player ratings. Therefore, for future predictive modelling tasks, using aggregated historical data is recommended for achieving more accurate and robust predictions.


Task 2 – Predicting Players' Best Position – Conclusions:
In Task 2, we focused on predicting players' best positions using three different machine learning models: Decision Tree, Random Forest, and XGBoost. The following conclusions highlight how different models, hyperparameters, and sets of features influenced the performance metrics.
XGBoost emerged as the best model for predicting players' best positions, thanks to its higher accuracy and ability to capture complex relationships in the data. The Random Forest model also performed well, offering a good balance between complexity and interpretability. The Decision Tree model, while simpler, provided reasonable performance but was less effective in distinguishing between certain positions.
Impact of Different Models and Hyperparameters:
Decision Tree: Simple and interpretable but limited in capturing data complexity.
Random Forest: Better performance due to ensemble learning, but still some limitations in role differentiation.
XGBoost: Superior accuracy and handling of complex patterns, though some closely related positions remain challenging.
Feature Sets: The use of diverse attributes (e.g., physical, technical, mental) across models highlighted the importance of comprehensive feature sets in enhancing predictive accuracy. Each model benefited from these features, though the extent varied based on the model's complexity and learning capabilities.
In summary, XGBoost is recommended for future development and deployment in predictive modeling tasks related to player positions, with potential improvements focused on fine-tuning hyperparameters and further exploring feature engineering to address misclassifications.
