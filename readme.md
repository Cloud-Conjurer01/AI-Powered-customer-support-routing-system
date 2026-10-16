# AI-Powered Customer Support Routing System

An AI/ML system that automatically classifies customer support tickets and
recommends the right department, reducing manual triage time.

## Problem Statement
Support teams receive large volumes of tickets. Reading, categorizing, and
assigning them manually is slow and can lead to delayed responses or wrong
department assignment.

## Solution
The system analyzes the subject and body of a ticket and predicts its type
(**Incident, Request, Problem, Change**). Based on the predicted type, it gives
a rule-based department recommendation.

## Tech Stack
- Python
- scikit-learn (TF-IDF, LinearSVC)
- pandas, NumPy

## Model Details
- **Feature extraction:** TF-IDF (unigrams + bigrams)
- **Classifier:** Linear Support Vector Classifier (LinearSVC)
- **Dataset:** 61,765 records, 80:20 train-test split
- **Accuracy:** improved from ~85.5% to ~90.48%

## Project Structure
├── data/            # dataset
├── notebooks/       # experiments
├── src/             # training and prediction code
├── requirements.txt
└── README.md

## Installation
git clone https://github.com/Cloud-Conjurer01/AI-Powered-customer-support-routing-system.git
cd AI-Powered-customer-support-routing-system
pip install -r requirements.txt

## Usage
python src/predict.py "My account is locked and I can't log in"
# Output: Ticket Type: Incident | Suggested Department: IT Support

## Future Scope
- Sentiment analysis
- Priority prediction
- Duplicate ticket detection
- MySQL database integration
- Streamlit analytics dashboard

## Author
Abhinav Sharma, B.Tech CSE (AI & DS), GLA University, Greater Noida
