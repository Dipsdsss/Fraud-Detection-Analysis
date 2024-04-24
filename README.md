# Fraud-Detection-Analysis

Definition:
Online payment is the most popular transaction method in the world today. However, with an increase in online payments also comes a rise in payment fraud. The objective of this study is to identify fraudulent and non-fraudulent payments. The dataset is collected from Kaggle, which contains historical information about fraudulent transactions which can be used to detect fraud in online payments.

1. Data Collection:
Dataset1
https://www.kaggle.com/datasets/jainilcoder/online-payment-fraud-detection
 
Dataset2: 

https://tianchi.aliyun.com/dataset/89527 

In this dataset,we are analyzing the probability that an online transaction is fraudulent, as denoted by the binary target isFraud.
The data is broken into two files identity and transaction, which are joined by TransactionID. Not all transactions have corresponding identity information.

Transaction Table
1.	TransactionDT: timedelta from a given reference datetime (not an actual timestamp)
A timedelta is a duration expressing the difference between two dates or times. In this context, "TransactionDT" would indicate the amount of time that has passed since the reference datetime for each transaction.
For example, if the reference datetime is January 1, 2024, and "TransactionDT" has a value of 3600 seconds, it would mean that the transaction occurred one hour after the reference datetime.
This type of representation can be useful for analyzing the time elapsed between transactions or for calculating time-based features such as time of day, day of week, or time since last transaction.


2.	TransactionAMT: transaction payment amount in USD
3.	ProductCD: product code, the product for each transaction

c: clothing, computers, or cosmetics
h: household products, home appliances, or hardware items. It could include items like kitchenware, furniture, or tools.
r: This could represent products related to recreation or entertainment. It might include items like books, movies, sporting goods, or toys.
w: This could refer to products related to wellness or health. It might include items like vitamins, supplements, fitness equipment, or personal care products.

4.	card1 - card6: payment card information, such as card type, card category, issue bank, country, etc. The actual meaning is masked.
5.	addr: address
6.	dist: distance
7.	P_ and (R__) emaildomain: purchaser and recipient email domain
8.	C1-C14: counting, such as how many addresses are found to be associated with the payment card, etc.

Identity Table
•	Variables in this table are identity information – network connection information (IP, ISP, Proxy, etc) and digital signature (UA/browser/os/version, etc) associated with transactions.
They're collected by Vesta’s fraud protection system and digital security partners.
(The field names are masked and pairwise dictionary will not be provided for privacy protection and contract agreement)
•	Categorical Features:
DeviceType
DeviceInfo
RangeIndex: 590540 entries, 0 to 590539
Data columns (total 17 columns):
      	
 
 2.	Data visualization:
    For better insights and tell a data story, we utilized most powerful and modern visulization tool: Microsoft Power BI

Steps:
	1.	After loading the preprocessed data into power BI, data was transformed in Power Query Editor feature.
	2.	Changed Data header, removed unwanted columns, null valued rows, and changed data types in Power Query itself.
	3.	Relationships: To create a relation between both the tables, established a one-to-one relationship in both with the help of Manage relationship > modeling tab in Query Editor.
	4.	Visuals: In the report view, we have utilized multiple types of charts, graphs to make an interactive and value rich report from large size of data.
	5.	All the charts on dashboard are interactive and filters have been added where it was needed.
	6.	This dashboard consists of three pages namely: Home Page, Devices Insights, More insights.
	7.	Data has been modified by using DAX queries, new columns and deleting unwanted anomolies.

 
  3. Analytics:

  Here are some Key Performance Indicators (KPIs) tailored specifically for analyzing historical data related to online fraud detection:

	a.	Fraudulent Transaction Rate: The percentage of transactions flagged as fraudulent (isfraud = 1) out of the total number of transactions in the historical dataset. This KPI provides an overview of the prevalence of fraud over time.
	
	b.	Fraud Detection Accuracy: The percentage of transactions correctly identified as fraudulent (isfraud = 1) out of the total number of transactions flagged as fraudulent. This KPI indicates the effectiveness of the fraud detection system in accurately identifying fraudulent activities.
	
	c.	False Positive Rate: The percentage of legitimate transactions incorrectly flagged as fraudulent (isfraud = 0 but flagged as 1) out of the total number of legitimate transactions. This KPI measures the accuracy of the fraud detection system in avoiding false alarms.
	
	d.	Time to Detect Fraud: The average time elapsed between the occurrence of a fraudulent transaction and its detection as fraudulent. This KPI provides insights into the efficiency of the fraud detection process in historical data.
	
	e.	Transaction Review Time: The average time taken by fraud analysts to review and investigate flagged transactions in historical data. This KPI indicates the operational efficiency of fraud detection procedures over time.
	
	f.Fraud by Device Type: Analysis of fraudulent transactions by different device types (e.g., desktop, mobile) over historical data to identify patterns or trends in fraudulent activity associated with specific devices.
	
	g.	Fraud by OS Type: Analysis of fraudulent transactions by different operating system types (e.g., iOS, Android, Windows) over historical data to understand if certain operating systems are more vulnerable to fraud.
	
	h.	Fraud by Purchase Type: Analysis of fraudulent transactions based on different types of purchases (e.g., Household, Clothing, personal care etc.) over historical data to identify any patterns related to the method of purchase.
	
	i.	Fraud by Card Type: Analysis of fraudulent transactions based on the type of payment card used (e.g., credit card, debit card) over historical data to identify if certain types of cards are more susceptible to fraud.
	
	j. Trend Analysis: Tracking the changes in fraud patterns over time by analyzing fraud rates and detection accuracy across different date stamps or time periods in the historical dataset.
 

Report Details:

1. Fraudulent Transaction Rate Analysis:
Visuals: Line chart showing the trend of fraudulent transaction rates over time.
Filter Options: Datestamp, isfraud, transaction types.
Insight: Stakeholders can track the fluctuations in fraudulent activity and identify potential trends or patterns.

2. Fraud Detection Accuracy and False Positive Rate:

Visuals: Stacked bar chart comparing fraud detection accuracy and false positive rates.
Filter Options: Isfraud, transaction types, card types.
Insight: Stakeholders can assess the effectiveness of the fraud detection system and evaluate the impact of false positives on legitimate transactions.

3. Transaction Review Time Analysis:

Visuals: Histogram depicting the distribution of transaction review times.
Filter Options: Isfraud, purchase type, purchase email domain.
Insight: Stakeholders can analyze the efficiency of transaction review processes and identify areas for optimization.

4. Fraud Patterns by Device and OS Type:

Visuals: Pie charts illustrating the distribution of fraudulent transactions by device and operating system types.
Filter Options: Isfraud, device types, OS types.
Insight: Stakeholders can identify potential vulnerabilities associated with specific devices and operating systems, informing targeted fraud prevention strategies. By leveraging interactive visuals and filter options, stakeholders can make informed decisions and drive continuous improvement in fraud detection measures.


References:
https://www.kaggle.com/code/kavya2099/online-payment-fraud-detection-eda
https://www.kaggle.com/datasets/jainilcoder/online-payment-fraud-detection/code
https://github.com/seuwenfei/Online-payment-fraud-detection/blob/main/online-payment-fraud-detection.ipynb
https://www.datacamp.com/tutorial/running-python-scripts-in-power-bi-tutorial
https://github.com/GoogleCloudPlatform/fraudfinder/blob/main/02_feature_engineering_batch.ipynb
https://tianchi.aliyun.com/dataset/?lang=en-us
https://tianchi.aliyun.com/dataset/89527

