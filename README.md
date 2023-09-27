Machine Learning Practices with Imbalanced Dataset \n
Overview 
The goal of this project was to build a model to detect fraudulent credit card transactions. We examined credit card transactions in two days by European cardholders in September 2013. The dataset is highly unbalanced, where only 492 out of 284,807 transactions are frauds. SMOTE approach was selected to resample a balanced sample. The final logistic regression model yielded the best recall score of 94.9%.
Business Understanding 
Fraud detection is essential for companies to safeguard their customers’ transactions and accounts. Otherwise, the bill could be quite hefty. According to Wallhub.com, the global cost due to credit card frauds in 2022 was US$219 million. Being able to detect fraudulent transactions. Being able to detect frauds can prevent financial and reputational losses of a credit card issuer.
Data Understanding
The dataset has been collected and analysed during a research collaboration of Worldline and the Machine Learning Group (http://mlg.ulb.ac.be) of ULB (Université Libre de Bruxelles) on big data mining and fraud detection. The dataset contains 284,807 credit card transactions and 30 features. 28 variables are anonymised due to confidentiality concern. We were interested in classifying the binary variable “Class”, whose value is 1 if fraud and 0 otherwise.            
The pie chart above shows the highly imbalance between frauds and non-frauds. This issue has to be tackled before we train the models otherwise we will end up having biased results where the model predicts the majority class every time.








Modeling and Evaluation 
4 machine learning models: decision tree, random forest, XGBoost and logistic regression were built and evaluated. Confusion matrix is used to visualize the predicted results.In this fraud detection scenario, it's more important to minimize false negatives, the model evaluation metric is recall. 



The plot above is the confusion matrix of the champion logistic regression model. The lower-left quadrant displays the number of false negatives: the number of frauds that the model misclassified as normal transaction. The logistic regression model has the best recall score of 94.9% and performed exceptionally on the test data. So it’s the champion model.
Conclusion
In an imbalanced data, the sample size of the majority class is significantly larger than the minority class. With an imbalanced data, a machine learning model is more likely to predict the majority class every time and therefore provide a biased result. In this project, we have shown that SMOTE is an effective approach to resample and provide a balanced sample for the later machine learning process. We recommend the logistic regression model because it performed well on the test data. Furthermore, the recall score is highest among all candidate models. The model very successfully classified frauds and non-frauds.
