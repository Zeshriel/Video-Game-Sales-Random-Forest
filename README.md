# Predicting Video Game Sales Using Random Forest Regression
### Team Members:
Etienne Laccruche, Ethan Lowery, Josiah Haines
## Objective / Abstract
This project aims to predict global video game sales using machine learning, specifically Random Forest regression. By using features such as genre, platform, publisher, and critic/user scores, the goal is to understand which factors most strongly influence game sales and create a model capable of estimating sales performance. This prediction helps developers, publishers, and marketers make data‑driven decisions in an industry with high financial risk.
### Problem Statement
Video game development and marketing involve substantial financial investments. Studios must decide which games to build, how to allocate budgets, and how to plan marketing strategies. However, predicting how well a game will sell is difficult. This project attempts to answer the question: Can global game sales be predicted based on metadata such as genre, platform, publisher, and review scores?
## Approach / Methods
### Data
We used a video game dataset sourced from Kaggle containing information such as:
- Genre
- Platform
- Publisher
- Developer
- Critic scores

After cleaning (removal of rows with missing values), 282 complete entries remained.
## Methods / Models
We applied a supervised machine learning approach because the project requires predicting a continuous target variable: global sales.

### Algorithm used:
- Random Forest Regression: chosen due to its ability to handle mixed feature types and reduce overfitting compared to a single decision tree.

Random Forest also provides feature importance measurements, which helps identify the biggest drivers of game sales.

## Google Colab Link for Model Detail
[Google Colab Link](https://colab.research.google.com/drive/1CWwb7uA7FPGPwV2CgJiU4HVmyn30FtnS?usp=sharing) <br>
`vgchartz-2024-clean.csv` is included in the repository

## Results

After training the Random Forest model, we evaluated performance using metrics such as R² and RMSE. The model performed reasonably well, showing that review scores, developer, and marketing (publishers) significantly influence predicted sales.

The Random Forest model provided stable predictions and avoided overfitting due to its ensemble averaging method.
### Conclusion / Lessons Learned
From the training of the model, we found that the largest 3 overarching drivers of videogame sales were the development team, the publishers (aka marketing), and the critic score. 
This gives insight, leading credence to the fact that developer trust and renown (Treyarch is a popular gamedev studio due to over a decade of yearly consistently successful game releases. However, there are instances where a new studio makes a massively successful release
which can skew that data) , marketing rigor, and positive early critic rating lead to a higher average of sales (The more people with early access to the game speak highly of it, the more people will be incentivised to buy the game).
However, due to how the read data was organized, the R^2 appears low in indication to the testing fit, but the importance can be easily discerned from the top-most important features.
We found that predicting video game sales is feasible using machine learning, although model performance is limited by the inherent unpredictability of consumer markets. Random Forest proved to be a strong choice because of its resistance to noise and its ability to provide interpretable feature importance.
### Future improvements could include:
- Testing additional models such as Gradient Boosted Trees or XGBoost
- Expanding the dataset
- Better handling of categorical variables using embeddings

## Five Takeaway Messages
- Random Forest is effective for mixed‑type tabular data like video game metadata.
- Global video game sales can be predicted **relatively** using genre, platform, publisher, and review scores.
- Feature importance helps identify which factors most strongly influence sales. However, there can frequently be outliers within game releases that can often skew the weight of the factors.
- Proper data cleaning significantly improves model accuracy. Having tested the raw uncleaned data separately, the model faced heavy amounts of inconsistency when certain data cells are missing.
- Machine learning can support high‑risk decision‑making in video game development. However, the complexity of the volatility of the gaming market is multi-faceted and can't be limited to just a couple main features.

## Five Multiple Choice Questions
1. What is the main benefit of Random Forest over a single decision tree?
  - A. Faster training
  - B. Lower memory usage
  - C. Reduced overfitting and higher accuracy
  - D. Works only on numerical data
2. Predicting global game sales is an example of what type of ML problem?
  - A. Classification
  - B. Regression
  - C. Clustering
  - D. Reinforcement Learning
3. What does feature importance tell us?
  - A. Which game sells best
  - B. Which platform is most popular
  - C. Which features influence sales the most
  - D. The best hyperparameters
4. Why is Random Forest suitable for this dataset?
  - A. It only works on text
  - B. It needs no training
  - C. It handles mixed data types and reduces overfitting
  - D. It guarantees perfect accuracy
5. What is the goal of the model?
  - A. Play video games automatically
  - B. Predict game sales
  - C. Rank all video games
  - D. Create AI game characters
## Contributions
Etienne Laccruche: Basically Everything
