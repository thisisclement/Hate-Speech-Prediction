# Capstone: Automatic Hate Speech Detection

Author: Clement Ow

_Disclaimer: Dataset may contain offensive content. This is only discussed and used for research and academic purposes only and do not condone such behaviour. Let's try our best to eradicate hate speech! \#techforgood_

### Contents:
- [Abstract](#Abstract)
- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Abstract

In this era of the digital age, online hate speech residing in social media networks can influence hate violence or even crimes towards a certain group of people. Hate related attacks targeted at specific groups of people are at a 16-year high in the United States of America, statistics released by the FBI reported. [[1]](https://www.nytimes.com/2019/11/12/us/hate-crimes-fbi-report.html) Therefore, there is a growing need to eradicate hate speech as much as possible through automatic detection to ease the load on moderators.

Datasets were obtained from Reddit and a white supremacist forum, Gab where there contains human labelled comments that are determined as hate speech related. [[2]](https://github.com/jing-qian/A-Benchmark-Dataset-for-Learning-to-Intervene-in-Online-Hate-Speech)

Multiple modelling approaches will be explored, such as machine learning models and even state-of-the-art deep learning models. F1 score and recall will be the metrics to be prioritised in model comparison. In the event where both are the same, actual False Negatives and False Postive numbers will be looked at.

## Problem Statement

In this digital age, online hate speech has increased over the past few years. Studies has shown that online hate speech can lead to offline violence towards a certain group. [[3]](https://phys.org/news/2019-10-online-speech-crimes-minorities.html)

In some cases, social media can lead to a more direct role, in this case the New Zealand shooting incident was broadcasted live on Facebook. [[4]](https://www.nytimes.com/2019/03/14/world/asia/new-zealand-shooting-updates-christchurch.html)

Due to the societal concern and how widespread hate speech is becoming on the Internet  and especially on social media, there is a strong need to classify online hate speech comments that are considered hate speech. [[5]](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0221152#sec001)

## Executive Summary

In recent years, there has been many cases of suicide rates increasing, mental health disorders skyrocketing and hitting millions of people in the world. Hate speech online are plausible causes of such high statistics.

Hate speech definition: Hate speech is speech that attacks a person or a group on the basis of protected attributes such as race, religion, ethnic origin, national origin, sex, disability, sexual orientation, or gender identity. [[6]](https://en.wikipedia.org/wiki/Hate_speech)

Hate speech categories:
- misogyny --> aimed at women
- misandry --> aimed at men
- racism --> aimed at specific race
- sexual orientation
- religion
- disability

Data is gathered from Reddit and Gab, a white supremacist forum. [[7]](https://github.com/jing-qian/A-Benchmark-Dataset-for-Learning-to-Intervene-in-Online-Hate-Speech) The models explored will be:

__Machine Learning models__
- Logistic Regression
- Naive-Bayes Classifier
- Ensemble models
  - Random Forest Classifier
  - Extra Trees Classifier
  - Adaboost Classifier
  - Gradient Boosting Classifier

__Deep Learning models__
- LSTM
- CNN & LSTM
- BERT model [[8]](https://github.com/google-research/bert)

After evaluating all the models, the best model is Logistic Regression achieving an F1 score of `87.91%`.

However, to truly increase the performance of the model, further research on understanding texts through linguistic features and context would need to be performed. Identifying and inputting more features into the model can also aid in increasing F1 scores as well. Ultimately, to further tune the model we have to use an interpretable model such as Logistic Regression to read the results to ensure it makes sense apart from just the accuracy scores.  


## Conclusions and Recommendations

### Model Comparison

| Classifier                              | F1 score | Recall |
|-----------------------------------------|----------|--------|
| Logistic Regression                     | **87.91%**   | **87.35%** |
| BERT                                    | 87%      | 87%    |

The best model in terms of test F1 score will be the Logistic Regression model with an F1 score of `87.91%` and an ROC AUC score of `0.91`. State-of-the-art NLP BERT model came close in second with an F1 score of `87%`.  

### Limitations and Further Work

The challenge faced by automatic hate speech detection is the subjectivity of whether a comment is considered hate speech or not. This can be better managed by having more people labelling these datasets to cross reference and to take a majority vote.

Another challenge is that many new urban words that are deemed derogatory are coined every few years or decades and the models that are developed now might be obsolete in the future. Constant training of new data sets will thus be paramount in overriding this problem.

As with any hate speech classification problem, context is needed to determine whether it is hate speech or not in many cases. Looking at the context of the text of how a word is being used and linguistic features will be a better way of understanding text. Of course, understanding sarcasm is one of the ongoing research which will help immensely in NLP tasks and higher accuracy rates. Therefore, more models have to be developed to train on learning to read context left or right of the target word or having "multiple views" of the same comment by using Multi-view ensemble stacking models.

### Conclusions

With the rise of social media and users being able to stay anonymous, hate speech detection is ever important in the digital age.

We present current approaches to this classification task and also explored different techniques including deep learning models and state-of-the-art models such as BERT.

Even though context is important in determining if a comment is hate speech or not, the simplest classifier, Logistic Regression, is actually the best performing one. This goes to show that at times, the simpler the classifier the better in terms of interpretability and it has made it easier to choose the best model with a superior F1 score.

In comparison with the state-of-the-art NLP BERT model, Logistic Regression was still able to perform very well while generalises well for this specific task. It is no wonder why Logistic Regression has been around for many years and continues to be widely used.
