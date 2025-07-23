# Customer-Loyalty-Prediction
This project predicts customer loyalty using machine learning on profiles and behavior data. It applies clustering and classification (logistic regression, decision trees) to identify segments and forecast loyalty, aiming to improve retention and support data-driven marketing strategies.

# Insights And Discussion
The study employed dimensionality reduction methods, including Principal Component Analysis (PCA) with both 2 and 3 principal components, as well as t-SNE (t-Distributed Stochastic Neighbor Embedding), to simplify the dataset while retaining meaningful patterns. However, neither PCA nor t-SNE achieved the desired cumulative explained variance of 90%, which was the predefined threshold for considering the reduction effective. PCA, while useful for visualizing high-dimensional data, only captured a limited portion of the variance, suggesting that the underlying structure of the data may not be strongly linear or that critical information was spread across many dimensions. Consequently, these techniques were excluded from the final modeling pipeline, and the original features were retained to avoid losing predictive power.
The clustering analysis identified three distinct customer segments, each with unique purchasing behaviors and financial profiles. The first segment comprised individuals with high purchasing power but surprisingly low spending scores, indicating a disconnect between their financial capacity and actual expenditure, a potential target for personalized engagement strategies. The second segment exhibited high spending scores paired with moderate income, suggesting financially savvy consumers who maximize value. The third and most lucrative segment combined high income with high spending, representing ideal candidates for premium offerings and loyalty programs. These findings enable marketing strategies, such as incentivizing the first segment to increase spending or deepening relationships with high-value customers in the third segment. The clear differentiation between clusters confirms the value of unsupervised learning in revealing hidden customer profiles that may not be apparent through traditional analysis.
Among the classification models tested—including logistic regression, random forests, and decision trees—the decision tree algorithm delivered the best results, albeit with a modest accuracy of only 53%. While this performance was suboptimal, the decision tree's interpretability provided valuable insights into feature importance, revealing that behavioral and demographic variables were the primary drivers of predictions. The model's limitations likely stem from the absence of key predictive features, particularly emotional or sentiment-based data, which could better explain customer decision-making. Unlike more complex ensemble methods, the decision tree’s simplicity may have helped it avoid overfitting, but the low accuracy underscores the need for richer input variables. Future iterations of this model should incorporate psychographic or transactional sentiment data to improve predictive capability.
To improve classification performance, future research should consider incorporating emotional, attitudinal, and psychographic variables, such as brand sentiment, trust, perceived ethical alignment, and customer satisfaction metrics. These could significantly enhance the model’s ability to capture the complexity behind customer loyalty and produce more accurate predictions.

# Visualizations 

**Figure 1.**
*Spending Score Distribution Across Preferred Categories*
<img width="686" height="482" alt="image" src="https://github.com/user-attachments/assets/ad9eb662-8548-4e9f-a2fd-ee0cb3620334" />

**Figure 2.** 
*Cluster plot using PCA, with evaluation metrics*
<img width="844" height="684" alt="image" src="https://github.com/user-attachments/assets/20e41c26-9c87-4bb5-b7af-e7faa6dfdc8b" />

**Figure 3.**
*Confusion Matrix of Logistic Regression Model*
<img width="614" height="415" alt="image" src="https://github.com/user-attachments/assets/1acac88f-565a-45ac-9fec-9810c82a385b" />


**Figure 4.** 
*Confusion Matrix of Decision Tree Classifier*
<img width="712" height="478" alt="image" src="https://github.com/user-attachments/assets/eeae60e2-8447-4350-aaa4-bbfee02fa090" />






