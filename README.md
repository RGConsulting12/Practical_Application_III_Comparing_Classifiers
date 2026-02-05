# Practical_Application_III_Comparing_Classifiers
The dataset comes from the UCI Machine Learning repository [link](https://archive.ics.uci.edu/ml/datasets/bank+marketing).  The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns.  I made use of the article accompanying the dataset [here](CRISP-DM-BANK.pdf) for more information on the data and features.

## Executive Summary (For Non-Technical Stakeholders)

### The Business Question
**"How can I predict which customers are most likely to subscribe to a term deposit, so I can prioritize our telemarketing calls?"**

### What Was Done
Started by analyzing 41,188 past customer interactions and built machine learning models to predict subscription likelihood. Then tested four different prediction approaches and identified the best one for production use.

### Key Results
- **Best Model**: Logistic Regression achieved **79% AUC** (meaning it correctly ranks likely subscribers above non-subscribers 79% of the time)
- **Potential Impact**: By calling only the top 20% of prospects (ranked by model score), this captured approximately 60% of all subscribers while reducing call volume by 80%

### Top Factors That Predict Subscription
1. **Economic conditions** (Euribor rate, employment levels) - When rates are lower, subscriptions increase
2. **Contact history** - Clients contacted 1-3 times respond better than those contacted 5+ times
3. **Previous campaign success** - Clients who subscribed before are more likely to subscribe again

### Recommended Actions
1. ✅ **Prioritize outreach** using model-ranked prospect lists
2. ✅ **Limit contact attempts** to 3-4 per campaign to avoid customer fatigue
3. ✅ **Adjust intensity** based on economic indicators (pause during high-rate periods)
4. ✅ **Exclude "duration"** from pre-call predictions (only known after call ends)
