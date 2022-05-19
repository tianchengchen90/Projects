## Problem Statement

With SAT and ACT signing statewide contract with states in order to gain market share, state actors would need to make decisions on whether ot not to go with the SAT or ACT, as well as evaluate if statewide contracts is beneficial. Usage of key data with the help of data science will be helpful to make such decisions regarding education and standardized testing. 

Hawaii remains as one of the states that favors neither ACT nor SAT. As a consultant hired to aid the state actor of Hawaii state, I am to evaluate the potential tradeoffs when signing statewide contracts with the SAT or ACT, and thereby answer whether Hawaii should sign a statewide contract with SAT or ACT.

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|ALL|State which SAT and ACT scores and partipation rates are collected from.| 
|**2017_sat_rate**|*float*|2017 SAT|Percentage of students in the state who participates in taking the examination.|
|**2017_sat_edrw**|*integer*|2017 SAT|Mean score of test-takers for Evidence-Based Reading and Writing section in the year (Min:200, Max:800).|
|**2017_sat_math**|*integer*|2017 SAT|Mean score of test-takers for Mathematics section in the year (Min:200, Max:800).|
|**2017_sat_total**|*integer*|2017 SAT|Mean score overall score for all test-takers in the year (Min:200, Max:800).|
|**2018_sat_rate**|*float*|2018 SAT|Percentage of students in the state who participates in taking the examination.|
|**2018_sat_edrw**|*integer*|2018 SAT|Mean score of test-takers for Evidence-Based Reading and Writing section in the year (Min:200, Max:800).|
|**2018_sat_math**|*integer*|2018 SAT|Mean score of test-takers for Mathematics section in the year (Min:200, Max:800).|
|**2018_sat_total**|*integer*|2018 SAT|Mean score overall score for all test-takers in the year (Min:200, Max:800).|
|**2019_sat_rate**|*float*|2019 SAT|Percentage of students in the state who participates in taking the examination.|
|**2019_sat_edrw**|*integer*|2019 SAT|Mean score of test-takers for Evidence-Based Reading and Writing section in the year (Min:200, Max:800).|
|**2019_sat_math**|*integer*|2019 SAT|Mean score of test-takers for Mathematics section in the year (Min:200, Max:800).|
|**2019_sat_total**|*integer*|2019 SAT|Mean score overall score for all test-takers in the year (Min:200, Max:800).|
|**2017_act_rate**|*float*|2017 ACT|Percentage of students in the state who participates in taking the examination.|
|**2017_act_english**|*float*|2017 ACT|Mean score of test-takers for English section in the year (Min:1, Max:36).|
|**2017_act_math**|*float*|2017 ACT|Mean score of test-takers for Mathematics section in the year (Min:1, Max:36).|
|**2017_act_reading**|*float*|2017 ACT|Mean score of test-takers for Reading section in the year (Min:1, Max:36).|
|**2017_act_science**|*float*|2017 ACT|Mean score of test-takers for Science section in the year (Min:1, Max:36).|
|**2017_act_total**|*float*|2017 ACT|Mean score overall score for all test-takers in the year (Min:1, Max:36).|
|**2018_act_rate**|*float*|2018 ACT|Percentage of students in the state who participates in taking the examination.|
|**2018_act_total**|*float*|2018 ACT|Mean score overall score for all test-takers in the year (Min:1, Max:36).|
|**2019_act_rate**|*integer*|2019 ACT|Percentage of students in the state who participates in taking the examination.|
|**2019_act_total**|*float*|2019 ACT|Mean score overall score for all test-takers in the year (Min:1, Max:36).|

## Executive Summary
A data science approach was used to guide the analysis. The problem statement was defined as whether the state of Hawaii should sign a statewide contract with ACT or SAT. Next, data was evaluated to identify credible and useful sources of information, and it was finalised to be ACT and SAT test scores and participation rates from 2017 to 2019. Data was imported as a dataframe and cleaned before merging. As part of the data cleaning process, any anomalies in scores, completeness of data, redundant data, and erroneous datatypes were fixed. An exploratory data analysis was to evaluate common parameters, and understand key trends, before coming up with the areas which will be visualized. The dataframe was then used to perform data visualization. The following data visualizations were used:

1) heatmap

2) histogram subplots

3) scatterplot and line of regression

4) boxplots

Inferences are made at each visualisation and exploratory data analysis stage, and external reasons and research were made to give insights. 

## Key Findings
- 1) From 2017 to 2019, SAT has been steadily gaining market share from ACT. Statewide contracts is one of the key reason which has allowed their aggressive growth.

- 2) Hawaii remains one of the only few states that is neutral to both SAT and ACT, and has high participation rate of more than 50% for all three years. 

- 3) States with high participation rate in SAT test tends to do worst in SAT overall score compared against the mean.

- 4) Similarly, states with high participation rate in ACT test tends to do worst in ACT overall score compared against the mean.

- 5) States that focus on one test tends to do worst in the other test, likely due to focusing of resources like preparation, monies, and time into one test.

- 6) The results of ACT is more consistent over the year, and is therefore more standardized in measuring performance, as compared to the SAT, which has had sagas with leaking of question, and overly easy difficulty setting in the three years.

- 7) Hawaii has lower average overall scores for both SAT and ACT than the national average, suggesting the need to move away from status quo.

## Conclusions and Recommendations
We see a few trends occuring between 2017 to 2019. SAT has been aggressively expanding its market share, and has had success. Hawaii is in a special position, and is one of the only states in the United States to have more than 50% participation rate for both SAT and ACT between 2017 to 2019. However, the state has fared lower than the average of other states for both ACT and SAT scores across all three years. As such, there is no inclination of one test being better over the other for Hawaii, making there room for negotiation with the test providers.

From the data visualisation of scores of SAT total and ACT composite, it can be suggested that ACT is the superior standardized test to measure, and does not deviate with time. ACT scores across three years are much more stable compared to the SAT. Furthermore, the SAT has had sagas of setting questions that are too easy, and even leaks of their questions in Asia that allows United States test takers to have an unfair advantage to.

There is a strong negative correlation between participation rate and scores. Thus state actors need to be mindful that Hawaii is already not faring very well in the aspect of scoring, as further dampening of score may happen as a consequence of compulsory statewide testing.

There is a negative correlation between SAT scores and ACT scores. On top of this being a state's individual prefence, state actors can also implement in their policies to encourage one test over the other by making it compulsory, thereby giving focus to one test type, and it should give rise to a increase in scores.

In conclusion, based on the data that I have, I recommend that Hawaii signed a statewide contract for ACT over SAT. I would greatly recommend to the state actor that statewide contracts can give rise to economies of scale. This may perhaps create or free up resources, where Hawaii can focus and channel into improving their test taker's preparedness. I would also recommend for further tracking of scores and participation in the future, as SAT will revamp their test once again in 2024.




