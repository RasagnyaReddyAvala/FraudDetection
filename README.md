# FraudDetection
Fraud risk is everywhere, but for companies that advertise online, click fraud can happen at an overwhelming volume, resulting in misleading click data and wasted money. Ad channels can drive up costs by simply clicking on the ad at a large scale. With over 1 billion smart mobile devices in active use every month, China is the largest mobile market in the world and therefore suffers from huge volumes of fraudulent traffic

Talking Data[2], China’s largest independent big data service platform, covers over 70% of active mobile devices nationwide. They handle 3 billion clicks per day, of which 90% are potentially fraudulent. Their current approach to prevent click fraud for app developers is to measure the journey of a user’s click across their portfolio, and flag IP addresses who produce lots of clicks, but never end up installing apps. With this information, they've built an IP blacklist and device blacklist.

While successful with the current approach, simultaneously the current process involves a huge amount of manual scrutiny i.e. categorise users based on individual portfolios while handling huge volume of clicks per day.
Hence, we in this project want to be one step ahead of fraudsters and have taken up this problem to further develop a solution that automates this process through Data Mining / Machine Learning techniques. The idea is to build an algorithm that predicts weather a user will download an app after clicking the mobile app ad. To support this modelling, we have a data set covering nearly 200 million clicks over a specific time.

Data Description:

File Descriptions:

	train.csv - Approximately 7.5GB file for training set

	test.csv - Approximately 700MB file for test set

Data fields: Each row of the training data contains a click record, with the following features.

	IP: IP address of click

	App: App id for marketing

	Device: Device type ID of user mobile phone (e.g., iphone 6 plus, iphone 7 etc.)

	OS: OS version ID of user mobile phone

	Channel: Channel ID of mobile ad publisher

	Click_time: Timestamp of click (UTC)

	Attributed_time: User app download time after clicking ad

	Is_attributed: The target that is to be predicted, indicating the app was downloaded

Data Insights:

	Training set contains 200 million rows and Test set contains 18 million rows. IP, App, Device, OS and Channel are categorical variables encoded as integers which needs to be converted to categories if required.

	New features on hourly and week day basis from Click_time attribute needs to be added and we need to group IP’s to analyse whether an IP represents a network ID with multiple hosts or a unique public user.

Notes:

	is_attributed is a binary target to predict

	IP, App, Device, OS, Channel are encoded

	Attributed_time is not available in the test set

Data Exploration:

Data is highly unbalanced, i.e. we have 99.8% of the negative samples and 0.2% positive side.

	We will first plot the scatter plot to draw conclusion of volume of the missing data (if any).

	Histogram of the attributes to analyse the data distribution.

	Correlation matrix scatter plot to analyse the correlation between the attributes.

	Visualize the Principal components of the attributes  for correlation analysis and feature engineering.

	Time series visualization to analyse the clicks per hour and clicks per day to draw inferences to build statistical modelling.

Data Mining Tasks:

	Feature engineering or dimension reduction through Principal Component Analysis.

	Transforming categorical data as factors for data visualization and model building.

	Extract pairwise relationship for highly correlated attributes and data.

	Use Boosting algorithms to treat imbalanced data .

	We plan to use Gradient boosting.

Data Mining Models/ Methods:

	Since this is a binary classification problem, we plan to initially use logistic regression for our initial modelling and analysis. 
Later we’ll take up discriminative analysis and classification with decision tree algorithm.

	The evaluation metric used will be dependent on ROC Curves.

Performance Evaluation:

We might consider a few performance evaluating metrics like 

i.	Confusion matrix – To evaluate the correctness and accuracy of the predicted model

ii.	AUROC


Impact of Project Outcomes:

The predicted model potentially helps us determine whether the user will download the app after clicking on the app ad. This might help the ad channels to focus on the right kind of audience.

Data Sources: 
Wikipedia , Kaggle.com.
https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection
