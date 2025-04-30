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
* Decision Tree with Cross-Validation
* Random Forest with GridSearchCV for Hyperparameter Tuning

## 🏁 Results:
After training and evaluating multiple models, here's how they stacked up:
### 🌳 Decision Tree with Cross-Validation:
Accuracy: 94% — solid and interpretable, but room for improvement.
### 🌲🌲 Random Forest with GridSearchCV:
Accuracy: 95% — a clear winner! Thanks to ensemble learning and proper hyperparameter tuning, performance improved while maintaining generalization.
This shows how combining GridSearchCV with powerful ensemble methods can push your model from good to great.



