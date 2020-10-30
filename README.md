# LinkedIn-Response-Prediction
The datasets used for this project are stored in the `data` folder

<p><b>Introduction</b><br>
This project aims to build a predictive model for linkedin responses as well as email responses. We have a number of factors that we think would hold predictive power. When deciding to reach out to potential partners, we need to be efficient as we only have so much time and want to focus on the avenues that are most likely to result in response.<br><br>
<b>Attributes of Interest</b><br>
LinkedIn Connections(# of connections), LinkedIn Summary Complete(Yes/No), Age(Current year - year graduated from college), Gender(M/F), Number of Skills Endorsed, Profile Picture(Yes/No), State,	City, Month Request Was Sent, Day of Week Request Was Sent, Time of Day Request Was Sent<br><br>
<b>Target Attributes</b><br>
Response to Linkedin Message(Yes/No)<br><br>
<b>Analysis</b><br>
Information were scrapped using <b>Python Selenium</b> from about 100 targeted LinkedIn profiles. The data cleaning process fixed missing value. Then, feature generation process was performed. Age was categorized into 4 groups: 'Below 5 Yrs', '5 - 15 Yrs', '15 - 30 Yrs', '30+ Yrs', and Months Worked for Most Recent Job feature was generated and categorized into 4 groups: 'Below 12 Months', '12 - 36 Months', '36 - 60 Months', '60+ Months'.<br>
<b>Random Over-Sampling</b> was utilized in order to fix data imbalance. And categorical data was encode into binary data. Next, <b>Logistic Regression</b>, <b>Random Forest</b> and <b>LGB</b> models were constructed. After tuning, the model with the highest ROC AUC score is LGB, which has an accuracy of 0.928.<br><br>
<b>Conclusion</b><br>
The top 4 highest feature importance identified by using feature importance function embedded in Random Forest, SHAP and Permutation Feature Importance are quite similar, which are <b>Number of Connections</b>, <b>Time Sent - 10:45</b>, <b>Time Sent - 11:45</b> and <b>City - Greater Los Angeles Area</b></p>
