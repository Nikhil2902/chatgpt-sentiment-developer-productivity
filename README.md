# ChatGPT Sentiment vs Developer Productivity

Me and Nitul Patel built this project because we were curious whether the way people talk about AI tools online actually reflects how useful those tools are in real life. So we decided to analyze Twitter data about ChatGPT and cross-reference it with real developer productivity data.

## Why we built this

Everyone has an opinion about ChatGPT. Some people love it, some hate it. But do the people who use it actually get more work done? That is the question we wanted to answer.

We honestly did not expect the results we got, which made this project way more interesting than we thought it would be.

## What we did

We collected two datasets - one with tweets about ChatGPT and one with developer activity logs. Then we:

- Cleaned and preprocessed both datasets. The missing data was a bigger problem than we expected and took a lot of time to fix properly
- Analyzed sentiment in tweets using a Naive Bayes classifier
- Used machine learning to predict developer commits based on AI usage and coding behavior
- Compared multiple models to find the best one

## Results

The sentiment model correctly classified tweets as positive, negative, or neutral with 71.5% accuracy. Getting to that number took a few tries with different approaches.

For predicting developer productivity (commits), we tested 3 models:

| Model | RMSE |
|---|---|
| Linear Regression | 3.88 |
| Random Forest | 4.88 |
| Decision Tree | 8.36 |

Honestly Linear Regression surprised us here because we expected Random Forest to perform better since it is more complex. But the data had a pretty straightforward relationship between variables which is why the simpler model won.

The biggest thing we found was that developers who use AI tools more tend to make more commits. So yes, AI tools do seem to actually help with productivity, at least based on this data.

## Tech stack

Python, Pandas, scikit-learn, Matplotlib, Jupyter Notebook

## Project notebooks

- 01_EDA_and_Preprocessing.ipynb
- 02_Sentiment_Analysis_Model.ipynb
- 03_ML_Models_and_Evaluation.ipynb
- 04_Complete_Final_Project.ipynb

## How to run

```
pip install pandas scikit-learn matplotlib jupyter
```

Open the notebooks in order from 01 to 04. You will need pdata.csv and sdata.csv to run the code.

## Authors
Nikhil Patel and Nitul Patel
