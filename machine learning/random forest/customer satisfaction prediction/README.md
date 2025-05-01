# 🚀Customer Satisfaction Prediction

## 🎫 Goal : Will This Passenger Be Happy? Let's Find Out!

Ever wondered what makes someone love or hate their flight? In this project, I take on the role of a data detective 🕵️‍♀️, digging into real airline survey data to predict whether a future passenger will leave the plane smiling — or swearing never to fly that airline again.

The dataset includes feedback from 129,880 travelers, covering everything from legroom complaints to in-flight entertainment scores 🍿✈️. My mission? Build a model that not only predicts satisfaction but also reveals which flight features matter most to passengers.

Think of it as turning air turbulence into clean, predictive insights.

## 📦 Dataset Overview
The dataset used is Invistico_Airline.csv, containing features such as:
* Travel type & class
* Flight distance
* In-flight services (entertainment, wifi, food, etc.)
* Customer type (loyal vs. disloyal)
* Delay times and more!
### Target variable: Satisfaction (satisfied or neutral/dissatisfied)

## 🧹 Data Preprocessing & Cleaning
#### Before modeling, I took the time to clean things up:
* Removed rows with missing or null values.
* Encoded categorical features using LabelEncoder and OneHotEncoder where appropriate.
* Scaled numerical features like flight distance and delay times for better model performance.
* Checked for class imbalance and ensured fair model evaluation.

## 📊 Exploratory Data Analysis (EDA)
* Explored distributions of flight class, travel type, and satisfaction.
* Found that business class passengers and loyal customers tend to report higher satisfaction.
* Delays and poor in-flight services strongly correlate with dissatisfaction.

## 🤖 Modeling & Results
#### 🔍 Models Built:
* Random Forest without CV
* Random Forest with GridSearchCV for Hyperparameter Tuning

## 🏁 Results:
After training and evaluating multiple models, here's how they stacked up:

### 🌳 Random Forest without Hyperparameter Tuning:
Accuracy: 95.7% — This looks impressive at first glance. However, it's important to note that this result might be overly optimistic, possibly due to the test set being particularly well-suited for this model by chance. Without cross-validation, the performance may not be as reliable across different data splits.

### 🌲🌲 Random Forest with GridSearchCV:
Accuracy: 94.2% — Although slightly lower in raw accuracy, this model is more stable and representative of true performance. By incorporating cross-validation and hyperparameter tuning, this model is better equipped to generalize to unseen data, making it the more trustworthy of the two.

#### 🔍 Key takeaway: Sometimes, higher accuracy doesn't mean better performance. A well-tuned model with cross-validation provides a more robust and dependable benchmark, even if the raw score appears slightly lower.


