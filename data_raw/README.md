# Raw Data

Data is provided by the US Census Bureau and has been archived in the University of California, Irvine (UCI) repository. The "[US Adult Income](https://www.kaggle.com/johnolafenwa/us-census-data)" dataset was obtained from [Kaggle](https://www.kaggle.com) on 11/9/2017.

The data is released under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0).

For both files, "adult-test.csv" and "adult-training.csv," the raw data files are in a `.csv` format and contain 15 columns in the following format:

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
