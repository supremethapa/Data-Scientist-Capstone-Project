# Udacity Data Scientist Nanodegree Capstone Project

This repository has all the code and report for my Udacity Data Scientist Nanodegree Capstone project.

## Starbucks Capstone Challenge: Using Starbucks app user data to predict effective offers

## Table of Contents
1. [Installation](#installation)
2. [Introducing a Dataset](#dataset-introduction)
3. [Project Motivation](#project-motivation)
4. [File Descriptions](#files)
5. [Results](#results)
6. [Licensing, Authors, Acknowledgements](#license)

### Installation <a name="installation"></a>
For running this project, the most important library is Python version of Anaconda Distribution. It installs all necessary packages for analysis and building models. 

### Introducing a Dataset <a name="dataset-introduction"></a>
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

### Project Motivation <a name="project-motivation"></a>
In this project, I use the data to answer 2 business questions:

  - 1. What are the main features influencing the effectiveness of an offer on the Starbucks app?
  - 2. Could the data provided, namely offer characteristics and user demographics, predict whether a user would take up an offer?

To answer the above 2 questions, I created 3 models for the data on the 3 offer types provided. The three offers are: Buy One Get One Free (BOGO), Discount (discount with purchase), and Informational (provides information about products).

### File Descriptions <a name="files"></a>
This repo contains 4 files.There is a notebook available here to showcase work related to the above questions and wrangling process. There are 3 data files used to address the above qustions
1. portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
2. profile.json - demographic data for each customer
3. transcript.json - records for transactions, offers received, offers viewed, and offers completed

## Results<a name="results"></a>

As a brief summary of my findings:
#### i. Question 1 findings:
For Question 1, the feature importance given by all 3 models were that the tenure of a member is the biggest predictor of the effectiveness of an offer.

For all three models, the top 3 variables were the same - membership tenure, income and age. However, income and age switched orders depending on offer type. 

For BOGO and discount offers, the distribution of feature importances were relatively equal. However, for informational offers, the distribution is slightly more balanced, with income the second most important variable.

#### ii. Question 2 findings:

My decision to use 3 separate models to predict the effectiveness of each offer type ended up with good accuracy for the BOGO and discount models (82.87% for BOGO and 87.38% for discount), while slightly less accurate performance for informational offers (75.23%). However, I would regard 75% as acceptable in a business setting, as for informational offers, there is no cost involved to inform users of a product.

Meanwhile, for BOGO and discount models, I am quite happy with the 80% and above accuracy, as in a business setting that would be acceptable to show offers to people, even if the model misclassifies a few, the overall revenue increase might justify the few mistakes.


The main observations of the code are published [here](https://medium.com/@smittal3797/sending-out-starbucks-offer-in-a-more-intelligent-manner-2b0dd2af6514).

### Licensing, Authors, Acknowledgements, etc.<a name="license"></a>

Data for coding project was provided by Udacity.
