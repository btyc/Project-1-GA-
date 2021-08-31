# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

Benjamin Toh, DSIF2

Problem Statement

Is there a bias between the ACT and SAT and what advice can we provide to the education board to help increase test scores?

Executive Summary
This project is using data which covers participation rates and scores for students who are taking the SAT and ACT exams. The data will be representing the individual US states. Research has been done to extract external datasets consisting of state-level per capita income and number of test centers each states have. These datas will be use to explore relationships with respect to the total scores of each states. 


Based on the analysis, there are states which consistently maintained as one of the worse performing states for these exams. They are also the states with a lower income as well especially for the ACT exam scores. A strong positive correlation between median income and ACT test scores is found. This prove that states with high median income are likely to see higher ACT scores as compared to states with low median income. However, no correlation was found for SAT scores and median income.


The formula for accessibility is (Participation * No.of Graduates / No. of Test Centers). This is to measure the ratio of graduates who took the respectively exams to one test centers. The higher the result, it will mean it is not convenient for students to take the exams in the states. A very weak negative correlation was discovered between accessibility of test centers to SAT scores as the correlation might be due to the few outliers in the dataset. This might mean that the more accessible the test centers, the lower the SAT scores. On the other hand, no correlation was found for ACT scores and accessibility of test centers. 


Conclusions and Recommendations

Based on our exploration of the data, we can conclude that income do play a part in affecting the ACT test score. High income families do have the capability in affording more or better prep courses, etc. However, that is not the case for SAT. Accessibilty of test centers does not matter for ACT but does have a very weak relationship for SAT. The high accessibility values are from outliers, hence there isn't a firm conclusion. 


It will be recommended for students to take SAT exams for standardize testing as there is no bias to income. There is no need to build additional test centers as well since it does not improve test scores.  


Further research into other factors, eg. what did states which improved do to increase score, number of prep centers, number of hours each students took to prepare, etc has to be done. 

Data
Data sources:
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))

External data
* https://collegereadiness.collegeboard.org/sat/register/find-test-centers

Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|State|object|sat_2017/sat_2018/sat_2019|Individual US States| 
|Participate17|float|sat_2017|Participation Rate in 2017|
|EBRW17|int|sat_2017|Evidence-Based Reading and Writing Scores for 2017|
|Math17|int|sat_2017|Math Scores for 2017|
|Total17|int|sat_2017|Total SAT Score for 2017|
|Participate18|float|sat_2018|Participation Rate in year 2018|
|EBRW18|int|sat_2018|Evidence-Based Reading and Writing Scores for 2018|
|Math18|int|sat_2018|Math Scores for 2018|
|Total18|int|sat_2018|Total SAT Score for 2018|
|Participate19|float|sat_2019|Participation Rate in year 2019|
|EBRW19|int|sat_2019|Evidence-Based Reading and Writing Scores for 2019|
|Math19|int|sat_2019|Math Scores for 2019|
|Total19|int|sat_2019|Total SAT Score for 2019|
|State Code|object|state1|2 Letters Code that represent each states|
|No. of SAT Test Centers|int|state1|Number of SAT test centers in each states|
|2016 - 2017 (No. of Graduates)|int|state1|Number of college graduates from 2016 - 2017|
|2017 - 2018 (No. of Graduates)|int|state1|Number of college graduates from 2017 - 2018|
|2018 - 2019 (No. of Graduates)|int|state1|Number of college graduates from 2018 - 2019|
|2019 - 2020 (No. of Graduates)|int|state1|Number of college graduates from 2019 - 2020|
|2017 (SAT Accessibility)|float|sat_17_18_19_access|Participation * Number of graduates / Number of test centers. The ratio of number of graduates who took SAT exams to 1 test center in 2017|
|2018 (SAT Accessibility)|float|sat_17_18_19_access|Participation * Number of graduates / Number of test centers. The ratio of number of graduates who took SAT exams to 1 test center in 2018|
|2019 (SAT Accessibility)|float|sat_17_18_19_access|Participation * Number of graduates / Number of test centers. The ratio of number of graduates who took SAT exams to 1 test center in 2019|
