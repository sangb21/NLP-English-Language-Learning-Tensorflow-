# NLP [Kaggle Competition](https://www.kaggle.com/competitions/feedback-prize-english-language-learning/overview): Feedback Prize - English-Language-Learning. Evaluete language knowledge of ELL students from grades 8-12


## Problem description (Duration: 30 August 2022 - November 29 2022)


The goal of this competition is to assess the language proficiency of 8th-12th grade English Language Learners (ELLs). 
Utilizing a dataset of essays written by ELLs will help to develop proficiency models that better supports all students.

## Data Description 

he dataset presented here (the ELLIPSE corpus) comprises argumentative essays written by 8th-12th grade English Language Learners (ELLs). 
The essays have been scored according to six analytic measures: 
**cohesion**, **syntax**, **vocabulary**, **phraseology**, **grammar**, and **conventions**.

Each measure represents a component of proficiency in essay writing, with greater scores corresponding to greater proficiency in that measure. 
The scores range from 1.0 to 5.0 in increments of 0.5. 
Your task is to predict the score of each of the six measures for the essays given in the test set.

Data [Link](https://www.kaggle.com/competitions/feedback-prize-english-language-learning/data)

## Approach

Approach was to use Transformers models with a regression head. 

## Important features 

* Model - DeBerta Base

* Certain features were added to model to improve the cros-validation score such as:
  * Weighted Meal-Pool
  * Last Layer Reinitialization
  * Layerwise Learning Rate Decay
  
 * MultilabelStratifiedKFold was used to split the training data into 5 folds. 
