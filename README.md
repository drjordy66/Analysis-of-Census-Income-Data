# Final Project Plan

## Introduction

For a final project I have chosen to work with a [1994 US Adult Census dataset](/data_raw) relating income to social factors including age, education, marital status, race, gender. The dataset is available on Kaggle.com and was obtained from the University of California, Irvine (UCI) repository. While the data is old, it is still important to see how social factors that contribute to income have changed over the years. This way we can determine whether there has been progress made in bridging the income gap based on these factors. We may not necessarily be able to identify the problems causing these gaps in income, but this dataset will help detect where the gaps are so further investigation can be made into these areas. While I do not currently have a recent dataset for relating income to social factors, I believe that the analysis and results from the 1994 dataset could be replicated with a more recent dataset, to provide insight into how social factors contributing to income have changed over time.

## Prior Work

I do not have any direct knowledge or experience with income and social factors, however, I have “heard” that several gaps exist between these factors and income. These include but are not limited to gaps between gender, race, age, marital status, and education. Performing this analysis should provide more evidence for these gaps should they actually exists (and I believe they do).

## Data

The data was obtained via Kaggle.com. It originated from the 1994 US Adult Census and was archived in the UCI repository. It was released under CC0 1.0 Universal. It has been split into two comma-separated variable (csv) files labeled “adult-test.csv” and “adult-training.csv.” Each file contains 15 columns:

Column | Type | Description/Categories
--- | --- | ---
age | int | self-describing
type_employer | str | the type of the employer the individual has (i.e. government, military, private, etc.).
fnlwgt | int | the final sampling weight (i.e. the number of people the census believes that observation represents)
education | str | the highest education attained
education_num | int | a numerical representation of the highest education attained
marital | str | marital status (i.e. married, single, divorced, etc.)
occupation | str | generic field of work
relationship | str | contains family relationship values like husband and father
race | str | self-describing
sex | boolean | sex at birth
capital_gain | int | income received other than salary
capital_loss | int | income lost other than salary
hr_per_week | int | number of hours worked per week
country | str | country of origin of the individual
income | boolean | less than $50K, or greater than or equal to $50K

The "relationship" attribute contains family relationship values like husband and father, however, there is only one per record. I will need to investigate the relevance of this attribute more.

The “adult-training.csv” file contains 32,561 rows and the “adult-test.csv” file contains 16,281 rows. For the purposes of this analysis, the two files will be joined together and split randomly later during the process.

Depending on feasibility, a more recent dataset may also be obtained in order to see if there have been any changes in how social factors influence income since 1994. This is not part of the goal of this analysis but rather a possibility should a dataset be readily available and time permitted.

There are some missing data points. At the moment it is unknown how these will be handled. Possibilities include imputation, deletion, or null values.

## Research Questions

1. Do income gaps exist based on social factors (gender, race, age, marital status, and education)?

Based on current knowledge, I expect that income gaps do exist based on social factors. It is pertinent to establish this first with the data.

2. Which social factor is the largest determining factor in income?

Having no prior knowledge or experience with this type of data, I would expect that education affects income the most.

3. Given a set of social factors, can we predict whether the income of the person will be greater than or less than $50K?

Yes, I believe that we will be able to predict the income classification of a person, given a set of social factors. As a guess, I will say that the accuracy is approximately 75%.

4. Ignoring income, what factors that appear to be highly correlated with each other?

While I believe that education affects income the most, the education I expect to be highly correlated with other contributing factors as well. I would expect to see the highest correlation between education and race.

## Process

The analysis for this project will be done using Python 3 in the Jupyter Notebook environment. Packages anticipated for use include but are not limited to matplotlib, numpy, pandas, and scikit-learn. The data and project will be available via GitHub.

The data will first need to be cleaned with missing values imputed, deleted, or replaced with null values. The columns currently do not have headers and the headers (from the Data section above) had to be obtained separately from the US Census Bureau. The two datasets will also be combined for the analysis portion of this study and split later for the machine learning model.

While plans may deviate once the analysis is underway, I do anticipate viewing the features in multiple ways. For instance, looking simply at how education affects income may not allow us to view everything involved. I may choose to subset the data first on race, and then analyze how education affects income. I may also look more into the relationships between social factors rather than how they each affect income.

For the machine learning process, I plan to first use a simple Logistic Regression classification model as this is binary classification problem given the “salary class” field. I will also look at using Lasso to perform feature selection, and determine which social factor contributes most to determining income classification.

All processes will be thoroughly documented within the Jupyter Notebook in markdown. All pertinent code will also be documented and associated with markdown documentation. This process should be both reproducible with this dataset and replicable with a more recent dataset in the same format (or is easily changed to the same format).

## Deliverables

The first deliverable is the machine learning model(s) that are used to predict a binary income classification given social factors. This will be obtained using a random training and test split of the data, with the model being trained on the training split and validated on the test split.

The second deliverable is an analysis of the entire dataset with insight into how social factors correlate between one another and how they correlate with income classification. Based on this analysis, we should be able to get an idea of whether income gaps exist based on the above mentioned social factors, and the severity of these gaps.

A possible third deliverable would be a comparison between the 1994 US Adult Census income data and a more recent census report. This is contingent upon time and availability of such a dataset.

## Conclusion

We often hear about “gaps” between gender, race, income, and several other societal factors. Some of these gaps exist for reasons that are unknown, however, some exist for reasons that are known but not enough has been done to address them. This study serves to objectively identify whether or not income gaps exist based on social factors that should not necessitate an income gap. It does not identify the root cause or problem, but rather identifies where further research should be done. It helps to narrow the scope of future research that may identify the problems contributing to the gaps.

If income gaps exist based on social factors (and I believe they do), these could be deemed discriminatory and unfair to those that are being discriminated against. Researching these gaps and ultimately their root causes allows us to determine what measures need to be taken in order to begin closing the gaps. Analyzing the census data from 1994 and comparing it with a more recent census could provide unique insight into whether or not anything has been done to improve incomes gaps related to social factors. Everyone deserves equal opportunity, however, that is not necessarily the case. Identifying that there is a problem is the first step towards correcting it.
