# [Safe Handling Instructions for Probabilistic Classification](https://youtu.be/RXMu96RJj_s)

## Keywords
Machine Learning, Data Science, Metrics, Classification, Probability 


## Abstract
In Machine Learning, Data Scientists use Classification algorithms to classify new observations (such as cats or dogs). However, a lot of times, people are more interested to know the probabilities of belonging to different classes rather than just the most likely class. For example, in the mortgage industry, knowing the probability of a mortgage being default is more interesting than just knowing the prediction label 0 or 1. In the retail industry, business stakeholders may need the conversion probabilities of leads to calculate the profit margin. Hence, traditional classification problems become probabilistic classification problems. 

Traditional classifiers and probabilistic classifiers are very similar since they all share the same machine learning algorithms, and only the output looks different (labels vs. scores). Because of the similarity, people may use the same metrics of traditional classifiers to evaluate the models, which may result in selecting the wrong models. 

Moreover, people may interpret the probability-ish outputs from the probabilistic classifiers are true probabilities, this mistake looks subtle but can be vital to business. For example, if a mortgage company uses Light GBM to predict mortgage defaulting, and later on interprets the scoring output from Light GBM as probabilities, people may become too optimistic because Light GBM tends to push all scores close to 0. 

Those are not rare mistakes people make in real life, even for experienced Data Scientists. This talk should help people who use Machine Learning in their work to better interpret probabilistic classifiers output, choose the best models for the business problems, and avoid using wrong metrics in the evaluation.  This talk also helps non-technical people understand data science problems and solutions better. 

## Agenda
* At the beginning of my talk (about 5 minutes), I talk about the difference between the traditional classification and probabilistic classification, and the scenarios people use probabilistic classification. 
* In the second part (about 6 minutes), I explain why the probability-ish outputs from models such as Random Forest or Support Vector Machines are not true probabilities even they are calculated from functions like predict_proba().  
* In the third part (about 7 minutes), I deep dive into the AUC score to explain why the metrics such as AUC score or F1 score fail on evaluating probabilistic classification models. I recommend a better metric Brier Score in this section for people to use to evaluate probabilistic classification models. 
* Lastly (about 7 minutes), I talk about different ways to avoid misusing the probabilistic classification output. For example, we can calibrate the scores using both parametric methods (based on Platt’s sigmoid model) or non-parametric methods (based on isotonic regression). We can also stack models using Logistic regression as the last layer output when training the models. 
Q&A section (about 3 minutes)

## Recording
[![test](./pic/RXMu96RJj_s&t.png)](https://www.youtube.com/watch?v=RXMu96RJj_s&t)


## Summary
In machine learning, a common task is to predict whether an unclassified observation belongs to one class or another. However, people are often actually more interested to know the probability of belonging to a class rather than just the most likely class. In such cases, a traditional classification problem becomes a probabilistic classification problem. This distinction is subtle yet crucial, and therefore should be carefully handled. Firstly, the probability-ish outputs of most classifiers are not true probabilities even they are from functions like predict_proba(). Moreover, if we use traditional metrics such as AUC score or F1 score on probabilistic classification problems, we may end up selecting the wrong models. Fortunately, probability calibration techniques, advanced model stacking/blending methods, and more suitable metrics can fix these issues.  

## Author Bio
Gordon is a University of Michigan Wolverine, who has academic degrees in Applied Statistics, Software Engineering, and Economics. Using Data Science technologies to solve challenging business problems is Gordon's passion. His Data Science journey started in 2006 when he led a team of students to win the 1st prize, out of 10,000 competing teams, in the China Undergraduate Mathematical Contest in Modeling (CUMCM). In Gordon's career, he has worked on various business problems, including managing a team of data scientists to develop the core probabilistic classification model for Kinnser RiskPoint, a product that is significantly reducing homecare industry hospitalization rate and earning millions of dollars in revenue per year for the company. Gordon currently works as a Principal Data Scientist at Oracle.

## Scipy 2019 info
[Website](https://www.scipy2019.scipy.org/)  
[Speaker Directory](https://www.scipy2019.scipy.org/speaker-directory)  
[Conference Schedule](https://www.scipy2019.scipy.org/confschedule)  
Gordon's talk is between 4:00 pm and 4:30 pm on July 10th, 2019 at the Zlotnik Ballroom.
