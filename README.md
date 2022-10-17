# Job-Posting-Fraudulent
Machine Learning Application with R (Random Forest, XGBoost)

Executive Summary (All tables and figures are shown in pdf file)
[Job Fraudulent Report.pdf](https://github.com/EvanaZhang/Job-Posting-Fraudulent/files/9805166/Job.Fraudulent.Report.pdf)

Business Problem

The online job posting service and the work of this service have been hit by many fraud job postings. Scammers post fake jobs to carry out some form of identity theft. The company believes that the existence of the company logos, the salary range and whether they have problems are the indicators of legitimate job postings. False employment postings are very detrimental to those aspiring individuals entering the labor market. In addition, job search companies have begun to step up investigations into fraud-related job postings in order to maintain their reputation.
This project will use the construction of a random forest model and XGBoost model to point out the key to the high possibility of fraud to determine the relevant factors leading to false recruitment and how to avoid it. Furthermore, according to the analysis of the data, there’s around 5% of the recruitment information in this data set count as fraudulent.


Key Findings

• Telecommuting and whether having questions or not are the insignificant variables for predicting the target variable, “fraudulent” with a less than 4.93% of the fraudulent and both variables show an extremely week comparison between with or with no fraud.
• Posting job with no company logo has a possibility of 20% higher to cause a fraudulent.
• A job requires an associate, internship and mid-senior level of the experience has an around 90% higher possibility lead to non-fraudulent, and there’s no significant different between each feature; thus, required experience can be counted as an insignificant variable for further predicting.
• Job posting with an employment type of temporary, full-time, and contract has a rate lower than 5% of causing fraudulent.


Model Performance Summary Interpretation

This dataset has total 18 variables which includes 5 numeric variables, 13 character variables. The first step is check dataset profile by using skim() function, and then check the percentage of with or without fraudulent by presenting as a target frequency table and classification graph. Next, explore the relationship between each of the categorical variables and numeric variables to see if each of them is being impactful and significant enough for building the models or further predicting. After that, converting the description variable to a variable called “sentiment_title” by using encoding. The final step before the partition target variable “fraudulent” and other categorical/numeric variables (employment type, telecommuting, has company logo, has questions, required experience, required education, job function) to a factor before building the models.


XGBoost Modeling & Radom Forest Modeling

• Set the number of trees as 10
• Randomly tuned three parameters (tree depth, min_n, and learning rate) with different sizes of 10
• The best and the most reasonable XGBoost model will be the model with 13 tree depth, 12 minimum number of variables and a learning rate of 0.002877158. (See Detailed Analysis & Steps Table 1)
• By comparing the ROC_AUC and the accuracy from both XGBoost and Random Forest models, random forest model will fit the data more. That’s why using the random forest model to do the kaggle prediction. (See Detailed Analysis and Steps Table 3 and Figure 1)

Recommendations

• Based on the key findings, companies should consider to focus on their company logos while posting jobs. They could let someone who’s in charge of job posting check whether they put logos on each job, or for those jobs which had already been posted online, company can check those jobs first of whether logos were posted with the job and make sure there’s no copyright infringement of the logos to avoid fraudulent.
• As a formal release of a legal position, company usually prioritize the level of education required for the job, the necessary work/required experiences, and the detailed information firms’ industry and job function. However, due to there’s too much missing values and the imbalance of the datasets, these variables are not significant enough for helping building the model and impact the rate of fraudulent. Therefore, the company should consider to add more info and focus on these aspects along with the company logos to avoid high possibility of fraudulent.

