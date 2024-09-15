# Heart Disease Diagnostics Ananlysis

### Context
We were Required to perform EDA on a Dataset containing details of heart disease diagnostics, with over a thousand rows of patient details. 
[The Dataset can be viewed here:](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/heart_disease_data.csv)

 
### Problem Definition
   Objective: To analyze and derive insights from the features associated with heart disease through the application of various visualization techniques.

[The complete code for this project is available here]( https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/heart_disease_diagnostics_analysis.ipynb)

## Process of deriving insights
First, to begin the process of extracting valuable insights from the dataset, I employed a range of machine learning algorithms, including Logistic Regression, Random Forest Classifier, and Decision Tree. Each of these algorithms was used to evaluate the feature importances, which provided a measure of how each feature contributes to predicting the target values. Logistic Regression, known for its interpretability, offered a straightforward assessment of feature weights. In contrast, the Random Forest Classifier and Decision Tree algorithms provided a more nuanced understanding by evaluating the relative importance of each feature through their hierarchical and ensemble-based approaches.

Once I had the feature importance scores from each algorithm, the next step involved analyzing these results to identify intersecting points. By comparing the lists of feature importances derived from each model, I was able to discern which features consistently held significance across different algorithms. This comparative analysis allowed me to determine the features that have a robust contribution to the target values, irrespective of the specific algorithm used. The intersection of these feature importance lists highlighted those features that are critical in influencing the outcome.

Through this process, I gained a clearer understanding of how each feature impacts the target values individually. By synthesizing the insights from multiple algorithms, I was able to develop a more comprehensive view of the dataset’s key attributes and their relative importance. This approach not only validated the significance of certain features but also provided a nuanced perspective on their individual contributions, leading to more informed decisions and interpretations in the project.

To initiate the process of determining feature importance, I first created a plot illustrating the column values in relation to their accuracy in detecting heart disease suing Logistic Regression. This initial visualization provided a foundational understanding of how different features impacted the model’s performance. Following this, I applied various machine learning algorithms to further analyze feature importance.

Specifically, I used the Random Forest Classifier to evaluate feature importances. After training the model with the training dataset, I obtained the feature importances, which reflect the relative contribution of each feature to the prediction of heart disease. Similarly, I employed the Decision Tree Classifier to generate another set of feature importance scores. By comparing these importance scores across the two algorithms, I was able to compile a comprehensive DataFrame that details each feature along with its importance score. This DataFrame helped visualize which features were most influential.

Additionally, I evaluated the model performance using a confusion matrix, which provided insights into the accuracy of predictions, and I created a heatmap to visually represent the feature importances within the context of the heart disease diagnostics dataset. Further visualizations included plots depicting the detection of heart disease relative to age and percentages of positive detections for each feature and its associated values. These analyses collectively contributed to a deeper understanding of how individual features impact the target values and informed subsequent steps in the project.

## Insights Derived
### 1. 
[The boxplot for the column age](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/Screenshot%202024-09-15%20203001.png) suggests that more of younger people have been testing positive for heart disease cases as compared to older people, depicted by a higher median age for False target values as compared to   True target values.
### 2.
[Plot of column values filtered with respect to accuracy>0.64 in detecting heart disease](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/Screenshot%202024-09-15%20202256.png) suggest that the attributes: Chest Pain, Heart Rate , Exercise Induced Angina, Oldpeak, Slope , CA( no. of major blood vessels colored by flourosopy) and Thalessemia Class have high accuracy in detecting heart disease in an individual. This list is later extended with further insights.
### 3. 
[The Feature-Importance Dataframe created by Random Forest](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/Screenshot%202024-09-15%20205735.png) further deem the features Chest Pain, Heart Rate ,CA, Oldpeak and Thalessemia Class important with respect to target values, Chest Pain being most important in the Random Forest algorithm.
### 4. 
[The Feature-Importance plot created by Decision Tree](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/Screenshot%202024-09-15%20202323.png) regards  Chest Pain ,CA, Oldpeak and Thalessemia Class as important features, with Chest Pain being significantly more important than all.
### 5. 
[The Confusion Matrix created from results of Decision Tree](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/Screenshot%202024-09-15%20202343.png) shows high accuracy in determination of True positives and True negatives with an error rate of 2.9%, suggesting an overall good model for the dataset.
### 6. 
[The Heatmap for the columns of Heart_Diasease_Diagnostics Dataset](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/Screenshot%202024-09-15%20202922.png) gives the same insights as the plot of column values with respect to their accuracy in detecting heart disease with Chest Pain, Heart Rate , Exercise Induced Angina, Oldpeak, Slope , CA( no. of major blood vessels colored by flourosopy) and Thalessemia Class appearing as columns with highest correlation with the target column in the dataset with Chest Pain and Heart Rate as the most important of attributes.
### 7. 
[The plot of positively detected heart disease with respect to respective values of each attribute](https://github.com/sooryanshi/heart_disease_diagnostics/blob/main/Screenshot%202024-09-15%20203024.png) give the following insights for each feature:
####         1. Chest pain:
   The Chest Pain types 1, 2 and 3 , all show detected heart disease cases as more than 60% of total cases in the dataset , with type 1 having                  about 80% detected cases , type 2 and type 3 having a little above 70% and 60% positive cases each. This emphasizes that Chest Pain of most                  types correlates with Heart Disease.
####         2. Heart Rate Class:
   The Heart Rate Classes 1 and 2 , i.e, normal and high heart rate, consisiting of values greater than 85% and 100% of MPHR , both showing                     about 60% positive detected cases for heart disease, suggesting a normal heart rate does not always correspond to good heart health.
####         3. Exercise Induced Angina(pain): 
   The insight shows that cases with absent exercise induced angina has more detected cases(over 60%) of heart disease than those with exercise                 induced angina present(20%), suggesting it might not be a strong determinant of heart disease diagnostics since the results are quite                        counter-intuitive.
####         4. Oldpeak Values:
   The oldpeak categories 0, 1(0 to 1), 2(1 to 2) and 3(greater than 2) show percentage of heart disease cases decreasing from 0 to 3 , with a  
   decrease of 10% cases from 0 to 2 and a decrease of 20% cases from 2 to 3, which is counter - intuitive to theory since higher oldpeak  
   values correspond to higher risk pf Heart Disease. This suggests that oldpeak values are a weak determinant of heart disease diagnostics and                 have to be taken into account along with other attributes to give valuable insights.
####         5. CA Values:
   The insight from the graph corresponds to the result that CA values of 0 and 4 correspond with higher cases of heart disease, 65% and 80%   
   respectively , and values 1-3 showing heart disease present in around 20% of all cases with some fluctuations. This suggests that even though the value 0 
   in theory is interpreted and very low risk, in practice it might not be of much significance. The values 1-3 ranging from mild-moderate risk show not 
   much significance in the insights of the data, whereas class 4 associated with severe risk in theory is as such in practice.
####         6. Thalessemia Class:
   The bars from the graph suggest class 2 corresponding to over 70% detected heart disease cases of all, with classes 0,1 and 3 comparing to 40% , 30% and     20% cases repectively. This suggests that Reversible Defect correlates to more heart disease cases than rest types of defects. The value 0 which is    
   interpreted as no defect has the second most cases in the graph, suggesting that a 'no defect' in thalessemia class may not be of significance in 
   correctly diagnosing heart disease. It must be studied with a combination of other attributes to give meaningful insights.
####         7. Slope Class:
   The slope classes indicate that the highest number of heart disease diagnoses (touching 80%) were found in cases with slope class = 2 which indeed is 
   associated with significant risk of heart disease. Slope classes 0 and 1 correspond to over 30% of cases diagnosed with heart disease. This suggests that 
   though the class 2 compare significantly to heart disease, 0 and 1 might not be that reliable in determination of diagnosis.

With this, I conclude the insights for the problem definition outlined above.
        

## Tools and Technologies

 ● Programming Language: Python

 ● Libraries: pandas, numpy, seaborn, matplotlib, sklearn 

---

## Conclusion
By meticulously analyzing the features associated with heart disease and employing a range of visualization techniques, I aim to uncover key patterns and relationships that contribute to a deeper understanding of this condition. The insights gained through this analysis will provide a clearer perspective on the factors influencing heart disease, enhance the interpretability of the data, and support the development of more effective diagnostic and preventive strategies. Through visualization, I will not only present the data in an accessible and meaningful manner but also facilitate better decision-making and strategic planning in the context of heart health.

---

