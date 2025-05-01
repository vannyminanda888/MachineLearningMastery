# 🎯 TikTok Claim Detection Project
Welcome to the TikTok Claim Detection project!
This project aims to build a machine learning model that can distinguish between claims and opinions in TikTok videos — helping TikTok better prioritize which videos need human moderation.

## 🧠 Why This Matters
TikTok gets millions of video reports daily — far more than human moderators can review.
But here’s the insight:
#### 📌 Claims are much more likely to break community guidelines than opinions.
So, by automatically tagging videos as claims or opinions, we can help moderators focus on videos that matter most.

* ✅ Claims → Possible violation → Prioritized for review
* 💬 Opinions → Lower risk → Skip human review (usually)
* 🔍 The Goal
Create a model that flags videos making claims — even if that means occasionally misclassifying opinions. It's better to be cautious and review too many videos than to miss a harmful one!

## 🎯 Evaluation Metric: Recall
#### We care most about **recall**, because:

* ❌ False negatives (missing a claim) = Bad (potentially harmful content ignored)

* ⚠️ False positives (mistaking opinion as claim) = Not ideal, but manageable (still gets reviewed)

## 📁 Dataset Overview
* ~20,000 TikTok video records
* Target column: claim_status (1 = claim, 0 = opinion)
* Text data: video_transcription_text
* Also includes user metadata (e.g., banned author status)

## 🧹 Workflow Summary
#### 1. 🔀 Data Splitting
* Train: 60%
* Validation: 20%
* Test: 20%

#### 2. 🧽 Data Cleaning
* Dropped non-informative features
* Removed rows with missing values

#### 3. 🧰 Feature Engineering
* Encoded categorical features
* Tokenized and transformed video_transcription_text for use in models

#### 4. 🤖 Model Training & Tuning
* Multiple models were tested
* Hyperparameters tuned using the training set

#### 5. 🏁 Model Selection
* Best-performing model selected based on **validation performance (focusing on recall)**

#### 6. 📊 Final Evaluation
* Champion model tested on the untouched test set for unbiased performance check

## 🚀 What’s Next?
#### This model could plug right into TikTok’s moderation pipeline:
* Videos classified as claims go into a downstream priority queue.
* Human moderators only review the most reported and most risky content.
* By streamlining moderation, this project helps TikTok keep its community safer, faster.
