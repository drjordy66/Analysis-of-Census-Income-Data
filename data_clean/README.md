# Cleaned Data

The cleaned data was created using the [raw data](../data_raw) on 12/9/2017.

As there were four varying methods for cleaning the data, there are four cleaned `.csv` files in the following formats:

## Method 1

Delete all rows associated with missing values reducing the total number of rows from 48,842 to 45,222.

Column | Type
--- | ---
age | int
type_employer | str
education_num | int
marital | str
occupation | str
relationship | str
race | str
sex | boolean
capital_gain | int
capital_loss | int
hr_per_week | int
country | str
income | boolean

## Method 2

Delete the features associated with missing values reducing the feature space from 14 to 11.

Column | Type
--- | ---
age | int
education_num | int
marital | str
relationship | str
race | str
sex | boolean
capital_gain | int
capital_loss | int
hr_per_week | int
income | boolean

## Method 3

Encode missing values as a category (not advised). This does not remove any features or rows, and adds a bias to the data severely reducing the impact categorical features have on income prediction.

Column | Type
--- | ---
age | int
type_employer | str
education_num | int
marital | str
occupation | str
relationship | str
race | str
sex | boolean
capital_gain | int
capital_loss | int
hr_per_week | int
country | str
income | boolean

## Method 4

Binarize the categorical features expanding the feature space significantly.

Column | Type
--- | ---
age | int
 education_num | int
 sex | boolean
 capital_gain | int
 capital_loss | int
 hr_per_week | int
 income | boolean
 type_employer_ Federal-gov | boolean
 type_employer_ Local-gov | boolean
 type_employer_ Never-worked | boolean
 type_employer_ Private | boolean
 type_employer_ Self-emp-inc | boolean
 type_employer_ Self-emp-not-inc | boolean
 type_employer_ State-gov | boolean
 type_employer_ Without-pay | boolean
 marital_ Divorced | boolean
 marital_ Married-AF-spouse | boolean
 marital_ Married-civ-spouse | boolean
 marital_ Married-spouse-absent | boolean
 marital_ Never-married | boolean
 marital_ Separated | boolean
 marital_ Widowed | boolean
 occupation_ Adm-clerical | boolean
 occupation_ Armed-Forces | boolean
 occupation_ Craft-repair | boolean
 occupation_ Exec-managerial | boolean
 occupation_ Farming-fishing | boolean
 occupation_ Handlers-cleaners | boolean
 occupation_ Machine-op-inspct | boolean
 occupation_ Other-service | boolean
 occupation_ Priv-house-serv | boolean
 occupation_ Prof-specialty | boolean
 occupation_ Protective-serv | boolean
 occupation_ Sales | boolean
 occupation_ Tech-support | boolean
 occupation_ Transport-moving | boolean
 relationship_ Husband | boolean
 relationship_ Not-in-family | boolean
 relationship_ Other-relative | boolean
 relationship_ Own-child | boolean
 relationship_ Unmarried | boolean
 relationship_ Wife | boolean
 race_ Amer-Indian-Eskimo | boolean
 race_ Asian-Pac-Islander | boolean
 race_ Black | boolean
 race_ Other | boolean
 race_ White | boolean
 country_ Cambodia | boolean
 country_ Canada | boolean
 country_ China | boolean
 country_ Columbia | boolean
 country_ Cuba | boolean
 country_ Dominican-Republic | boolean
 country_ Ecuador | boolean
 country_ El-Salvador | boolean
 country_ England | boolean
 country_ France | boolean
 country_ Germany | boolean
 country_ Greece | boolean
 country_ Guatemala | boolean
 country_ Haiti | boolean
 country_ Holand-Netherlands | boolean
 country_ Honduras | boolean
 country_ Hong | boolean
 country_ Hungary | boolean
 country_ India | boolean
 country_ Iran | boolean
 country_ Ireland | boolean
 country_ Italy | boolean
 country_ Jamaica | boolean
 country_ Japan | boolean
 country_ Laos | boolean
 country_ Mexico | boolean
 country_ Nicaragua | boolean
 country_ Outlying-US(Guam-USVI-etc) | boolean
 country_ Peru | boolean
 country_ Philippines | boolean
 country_ Poland | boolean
 country_ Portugal | boolean
 country_ Puerto-Rico | boolean
 country_ Scotland | boolean
 country_ South | boolean
 country_ Taiwan | boolean
 country_ Thailand | boolean
 country_ Trinadad&Tobago | boolean
 country_ United-States | boolean
 country_ Vietnam | boolean
 country_ Yugoslavia | boolean
