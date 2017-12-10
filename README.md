# Final Project - Analysis of Census Income Data

## Abstract

_words_

## Organization of the project

The project has the following structure:

```
data-512-final-project/
  |- analysis/
     |- README.md
     |- eda_country.png
     |- eda_education.png
     |- eda_income.png
     |- eda_marital.png
     |- eda_occupation.png
     |- eda_race.png
     |- eda_relationship.png
     |- eda_sex.png
     |- eda_type_employer.png
     |- m1_coefficient_values_bargraph.png
     |- m1_conf_mat.png
     |- m1_pearson_corr_heatmap.png
     |- m1_pearson_corr_heatmap_filtered.png
     |- m2_conf_mat.png
     |- m3_conf_mat.png
     |- m4_coefficient_values_bargraph.png
     |- m4_conf_mat.png
     |- m4_pearson_corr_heatmap.png
  |- data_clean/
     |- README.md
     |- method1.csv
     |- method2.csv
     |- method3.csv
     |- method4.csv
  |- data_raw/
     |- README.md
     |- adult-test.csv
     |- adult-training.csv
  |- project_plan/
  	 |- README.md
  |- src/
     |- README.md
     |- hcds-final-project.ipynb
```

### Goal

The goal of this project is to explore the "[US Adult Income](https://www.kaggle.com/johnolafenwa/us-census-data)" data and develop a model to predict whether an individual's income will be less than or equal to $50,000, or greater than $50,000. This prediction will be based on a number of features that describe the [data](/data_raw).

Initially, we will perform an exploratory data analysis (EDA) to determine the integrity of the data and decide how issues with missing or unclear data will be handled. We will also present some summary statistics via visualizations.

We will then perform a more focused [analysis](/analysis) which includes a series of visualizations and tables that serve to answer the following research questions:

1. Given a set of features, can we predict whether the income of a person will be greater than or less than $50,000?
2. Which feature is the most important in determining income classification?
3. Ignoring income, what factors appear to be highly correlated with each other?

In conclusion, we will reflect on the implication of the findings from this analysis. We will also reflect on any limitations that may be reflected in the data.

### Licenses and links

Data is provided by the US Census Bureau and has been archived in the University of California, Irvine (UCI) repository. The "[US Adult Income](https://www.kaggle.com/johnolafenwa/us-census-data)" dataset was obtained from [Kaggle](https://www.kaggle.com) on 11/9/2017.

https://www.kaggle.com/johnolafenwa/us-census-data

- [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0)

### Cleaned data

The [cleaned data](/data_clean) files are in a `.csv` format. Details regarding the format can be seen in the [cleaned data](/data_clean) directory.

### Reproducibility

The steps for reproducing this analysis can be found in the jupyter notebook [hcds-final-project.ipynb](/src/hcds-final-project.ipynb) under the [src](/src) directory.

### Issues/special considerations

---------------
- Combining the datasets removed rows where country names were not uniform. This is intentional and per the instructions of the analysis.

- The [`page_data.csv`](/data_raw) contains revision ids that the ORES API may not find. These articles have most likely been deleted. The API call will list any relevant revision ids that were not found and a prediction value of 'NA' will be inserted into the article quality prediction.
---------------

### Additional attribution(s)

Relevant information pertaining to this assignment was gathered from [HCDS (Fall 2017) Assignments](https://wiki.communitydata.cc/HCDS_(Fall_2017)/Assignments#A6:_Final_project_report).

- CC-BY-SA 3.0