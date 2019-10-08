---
title: "Assignment 2 - Language Development in ASD - Part 1 - Explaining development"
author: "Alexander Mirz & Jakub Raszka"
date: '[DATE]'
output:
  html_document: 
    keep_md: yes
  pdf_document: default
---
    


# Assignment 2

In this assignment you will have to discuss a few important questions (given the data you have). More details below. The assignment submitted to the teachers consists of:
- a report answering and discussing the questions (so we can assess your conceptual understanding and ability to explain and critically reflect)
- a link to a git repository with all the code (so we can assess your code)

Part 1 - Basic description of language development
- Describe your sample (n, age, gender, clinical and cognitive features of the two groups) and critically assess whether the groups (ASD and TD) are balanced
- Describe linguistic development (in terms of MLU over time) in TD and ASD children (as a function of group). 
- Describe how parental use of language (in terms of MLU) changes over time. What do you think is going on?
- Include individual differences in your model of language development (in children). Identify the best model.

Part 2 - Model comparison
- Discuss the differences in performance of your model in training and testing data
- Which individual differences should be included in a model that maximizes your ability to explain/predict new data?
- Predict a new kid's performance (Bernie) and discuss it against expected performance of the two groups

Part 3 - Simulations to plan a new study
- Report and discuss a power analyses identifying how many new kids you would need to replicate the results

The following involves only Part 1.

## Learning objectives

- Summarize and report data and models
- Critically apply mixed effects (or multilevel) models
- Explore the issues involved in feature selection


# Quick recap
Autism Spectrum Disorder is often related to language impairment. However, this phenomenon has not been empirically traced in detail:
i) relying on actual naturalistic language production,  ii) over extended periods of time.

We therefore videotaped circa 30 kids with ASD and circa 30 comparison kids (matched by linguistic performance at visit 1) for ca. 30 minutes of naturalistic interactions with a parent. We repeated the data collection 6 times per kid, with 4 months between each visit. We transcribed the data and counted: 
i) the amount of words that each kid uses in each video. Same for the parent.
ii) the amount of unique words that each kid uses in each video. Same for the parent.
iii) the amount of morphemes per utterance (Mean Length of Utterance) displayed by each child in each video. Same for the parent. 

This data is in the file you prepared in the previous class. 

NB. A few children have been excluded from your datasets. We will be using them next week to evaluate how good your models are in assessing the linguistic development in new participants.

This RMarkdown file includes 
1) questions (see above). Questions have to be answered/discussed in a separate document that you have to directly send to the teachers.
2) A break down of the questions into a guided template full of hints for writing the code to solve the exercises. Fill in the code and the paragraphs as required. Then report your results in the doc for the teachers.

REMEMBER that you will have to have a github repository for the code and send the answers to Kenneth and Riccardo without code (but a link to your github/gitlab repository). This way we can check your code, but you are also forced to figure out how to report your analyses :-)

Before we get going, here is a reminder of the issues you will have to discuss in your report:

1- Describe your sample (n, age, gender, clinical and cognitive features of the two groups) and critically assess whether the groups (ASD and TD) are balanced
2- Describe linguistic development (in terms of MLU over time) in TD and ASD children (as a function of group). 
3- Describe how parental use of language (in terms of MLU) changes over time. What do you think is going on?
4- Include individual differences in your model of language development (in children). Identify the best model.

# Let's go

### Loading the relevant libraries

Load necessary libraries : what will you need?
- e.g. something to deal with the data
- e.g. mixed effects models
- e.g. something to plot with



### Define your working directory and load the data
If you created a project for this class and opened this Rmd file from within that project, your working directory is your project directory.

If you opened this Rmd file outside of a project, you will need some code to find the data:
- Create a new variable called locpath (localpath)
- Set it to be equal to your working directory
- Move to that directory (setwd(locpath))
- Load the data you saved last time (use read_csv(fileName))



### Characterize the participants (Exercise 1)

<!-- Identify relevant variables: participants demographic characteristics, diagnosis, ADOS, Verbal IQ, Non Verbal IQ, Socialization, Visit, Number of words used, Number of unique words used, mean length of utterance in both child and parents. -->

<!-- Make sure the variables are in the right format. -->

<!-- Describe the characteristics of the two groups of participants and whether the two groups are well matched. -->



## Let's test hypothesis 1: Children with ASD display a language impairment  (Exercise 2)

### Hypothesis: The child's MLU changes: i) over time, ii) according to diagnosis





How would you evaluate whether the model is a good model?



<!-- As per the graphical representations above, there seems to be steeper and more consistent development over time for the children that do not have the ASD diagnosis.  -->

## Let's test hypothesis 2: Parents speak equally to children with ASD and TD  (Exercise 3)



### Adding new variables (Exercise 4)



<!-- In addition to Diagnosis and visit, the MLU of the children is also correlated with the following measurements:  -->
<!-- Using AIC / nested F-tests as a criterium, we compared models of increasing complexity and found that ... -->

## Part 2

### Exercise 1) Testing model performance




### Exercise 2) Model Selection via Cross-validation (N.B: ChildMLU!)



<!-- [HERE GOES YOUR ANSWER] -->

### Exercise 3) Assessing the single child

<!-- Let's get to business. This new kiddo - Bernie - has entered your clinic. This child has to be assessed according to his group's average and his expected development. -->

<!-- Bernie is one of the six kids in the test dataset, so make sure to extract that child alone for the following analysis. -->

<!-- You want to evaluate: -->

<!-- - how does the child fare in ChildMLU compared to the average TD child at each visit? Define the distance in terms of absolute difference between this Child and the average TD. -->

<!-- - how does the child fare compared to the model predictions at Visit 6? Is the child below or above expectations? (tip: use the predict() function on Bernie's data only and compare the prediction with the actual performance of the child) -->





