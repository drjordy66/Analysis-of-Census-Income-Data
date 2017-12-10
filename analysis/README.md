# Analysis/Visualizations

## Contents

- [Exploratory Data Analysis - EDA](#Exploratory Data Analysis---EDA)
  - [High-Level](#High-Level)
  - [Summary Statistics of Numerical Features](Summary-Statistics-of-Numerical-Features)
  - [Summary of Categorical Features - Tables and Graphs](Summary-of-Categorical-Features---Tables-and-Graphs)
    - [type_employer](#type_employer)
    - [education](#education)
    - [marital](#marital)
    - [occupation](#occupation)
    - [relationship](#relationship)
    - [race](#race)
    - [sex](#sex)
    - [country](#country)
    - [income](#income)
- [Research Questions](#Research-Questions)
  - [RQ1](#1.-Given-a-set-of-features,-can-we-predict-whether-the-income-of-a-person-will-be-greater-than-or-less-than-$50,000?)

## Exploratory Data Analysis - EDA

### High-Level

feature | dtype | unique_count
--- | --- | ---
age | int64 | 74
type_employer | object | 9
fnlwgt | int64 | 28523
education | object | 16
education_num | int64 | 16
marital | object | 7
occupation | object | 15
relationship | object | 6
race | object | 5
sex | object | 2
capital_gain | int64 | 123
capital_loss | int64 | 99
hr_per_week | int64 | 96
country | object | 42
income | object | 4

### Summary Statistics of Numerical Features

--- | age | fnlwgt | education_num | capital_gain | capital_loss | hr_per_week
--- | --- | --- | --- | --- | --- | ---
count | 48842 | 48842 | 48842 | 4035 | 2282 | 48842
mean | 38.643585 | 189664.1 | 10.078089 | 13061.665675 | 1872.825592 | 40.422382
std | 13.710510 | 105604 | 2.570973 | 22711.237412 | 364.048529 | 12.391444
min | 17 | 12285 | 1 | 114 | 155 | 1
25% | 28 | 117550.5 | 9 | 3411 | 1672 | 40
50% | 37 | 178144.5 | 10 | 7298 | 1887 | 40
75% | 48 | 237642 | 12 | 13550 | 1977 | 45
max | 90 | 1490400 | 16 | 99999 | 4356 | 99

### Summary of Categorical Features - Tables and Graphs

#### type_employer

Table:

type_employer | count
--- | ---
Federal-gov | 1432
Local-gov | 3136
Never-worked | 10
Private | 33906
Self-emp-inc | 1695
Self-emp-not-inc | 3862
State-gov | 1981
Without-pay | 21

Bar Graph:

![Alt text](/analysis/eda_type_employer.png?raw=true "type_employer")

#### education

Table:

education | count
--- | ---
Preschool | 83
1st-4th | 247
5th-6th | 509
7th-8th | 955
9th | 756
10th | 1389
11th | 1812
12th | 657
HS-grad | 15784
Some-college | 10878
Assoc-voc | 2061
Assoc-acdm | 1601
Bachelors | 8025
Masters | 2657
Prof-school | 834
Doctorate | 594

Bar Graph:

![Alt text](/analysis/eda_education.png?raw=true "education")

#### marital

Table:

marital | count
--- | ---
Divorced | 6633
Married-AF-spouse | 37
Married-civ-spouse | 22379
Married-spouse-absent | 628
Never-married | 16117
Separated | 1530
Widowed | 1518

Bar Graph:

![Alt text](/analysis/eda_marital.png?raw=true "marital")

#### occupation

Table:

occupation | count
--- | ---
Adm-clerical | 5611
Armed-Forces | 15
Craft-repair | 6112
Exec-managerial | 6086
Farming-fishing | 1490
Handlers-cleaners | 2072
Machine-op-inspct | 3022
Other-service | 4923
Priv-house-serv | 242
Prof-specialty | 6172
Protective-serv | 983
Sales | 5504
Tech-support | 1446
Transport-moving | 2355

Bar Graph:

![Alt text](/analysis/eda_occupation.png?raw=true "occupation")

#### relationship

Table:

relationship | count
--- | ---
Husband | 19716
Not-in-family | 12583
Other-relative | 1506
Own-child | 7581
Unmarried | 5125
Wife | 2331

Bar Graph:

![Alt text](/analysis/eda_relationship.png?raw=true "relationship")

#### race

Table:

race | count
--- | ---
Amer-Indian-Eskimo | 470
Asian-Pac-Islander | 1519
Black | 4685
Other | 406
White | 41762

Bar Graph:

![Alt text](/analysis/eda_race.png?raw=true "race")

#### sex

Table:

sex | count
--- | ---
Female | 16192
Male | 32650

Bar Graph:

![Alt text](/analysis/eda_sex.png?raw=true "sex")

#### country

Table:

country | count
--- | ---
Cambodia | 28
Canada | 182
China | 122
Columbia | 85
Cuba | 138
Dominican-Republic | 103
Ecuador | 45
El-Salvador | 155
England | 127
France | 38
Germany | 206
Greece | 49
Guatemala | 88
Haiti | 75
Holand-Netherlands | 1
Honduras | 20
Hong | 30
Hungary | 19
India | 151
Iran | 59
Ireland | 37
Italy | 105
Jamaica | 106
Japan | 92
Laos | 23
Mexico | 951
Nicaragua | 49
Outlying-US(Guam-USVI-etc) | 23
Peru | 46
Philippines | 295
Poland | 87
Portugal | 67
Puerto-Rico | 184
Scotland | 21
South | 115
Taiwan | 65
Thailand | 30
Trinadad&Tobago | 27
United-States | 43832
Vietnam | 86
Yugoslavia | 23

Bar Graph:

![Alt text](/analysis/eda_country.png?raw=true "country")

#### income

Table:

income | count
--- | ---
<=50K | 24720
<=50K. | 12435
>50K | 7841
>50K. | 3846

Bar Graph:

![Alt text](/analysis/eda_income.png?raw=true "income")

## Research Questions

### 1. Given a set of features, can we predict whether the income of a person will be greater than or less than $50,000?

#### Method 1 Confusion Matrix

![Alt text](/analysis/m1_conf_mat.png?raw=true "m1_conf_mat")

#### Method 2 Confusion Matrix

![Alt text](/analysis/m2_conf_mat.png?raw=true "m2_conf_mat")

#### Method 3 Confusion Matrix

![Alt text](/analysis/m3_conf_mat.png?raw=true "m3_conf_mat")

#### Method 4 Confusion Matrix

![Alt text](/analysis/m4_conf_mat.png?raw=true "m4_conf_mat")

### 2. Which feature is the most important in determining income classification?

#### Method 1

Coefficient Values:

![Alt text](/analysis/m1_coefficient_values_bargraph.png?raw=true "m1_coefficient_values_bargraph")

#### Method 4

Coefficient Values:

![Alt text](/analysis/m4_coefficient_values_bargraph.png?raw=true "m4_coefficient_values_bargraph")

### 3. Ignoring income, what factors appear to be highly correlated with each other?

#### Method 1

![Alt text](/analysis/m1_pearson_corr_heatmap.png?raw=true "m1_pearson_corr_heatmap")

Filtered with a 0.2 threshold:

![Alt text](/analysis/m1_pearson_corr_heatmap_filtered.png?raw=true "m1_pearson_corr_heatmap_filtered")

#### Method 4

![Alt text](/analysis/m4_pearson_corr_heatmap.png?raw=true "m4_pearson_corr_heatmap")
