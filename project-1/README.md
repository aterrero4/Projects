# Introduction
## Background
### SAT / ACT
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

### SNAP
[SNAP](https://www.fns.usda.gov/snap) stands for the Supplemental Nutrition Assistance Program, which is a federal assistance program in the United States aimed at providing nutrition assistance to low-income individuals and families. It was formerly known as the Food Stamp Program.

SNAP benefits are designed to help [eligible participants](https://www.fns.usda.gov/snap/recipient/eligibility) purchase food and improve their access to nutritious meals. The program provides electronic benefit transfer (EBT) cards that can be used like debit cards to purchase eligible food items at authorized retailers, including grocery stores, supermarkets, and farmers markets.

The eligibility for SNAP benefits is primarily based on household income and size, with specific income thresholds set by the federal government. The program serves a wide range of individuals, including low-wage workers, unemployed individuals, elderly people, and families with children.

SNAP plays a crucial role in reducing food insecurity and improving nutritional outcomes for vulnerable populations. It is administered by the United States Department of Agriculture (USDA), and each state is responsible for implementing the program within its jurisdiction
The objective of this project is to examine the relationship between the percentage of participating SNAP households with children in fiscal years 2018 and 2019 and SAT scores by state in the same years.

### The project aims to address the following research questions:
1. How does the percentage of participating SNAP households with children vary across states in fiscal years 2018 and 2019?
2. Is there any correlation between the percentage of participating SNAP households with children and SAT scores by state in fiscal years 2018 and 2019?
3. Can the percentage of participating SNAP households with children be used as a predictor for SAT scores by state?

By analyzing these datasets and exploring the potential relationship between SAT scores and SNAP benefits participation, this project aims to provide insights into any potential associations or patterns that may exist. Such findings could have implications for policymakers and educators in developing strategies to support students from economically disadvantaged backgrounds.

# Data Description
## Data Sources
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State
* [`snap_2018.csv`](./data/snap_2018.csv): Percentage of Participating SNAP Households with Children (FY 2018) 
* [`snap_2019.csv`](./data/snap_2019.csv): Percentage of Participating SNAP Households with Children (FY 2019)
* [`sat_snap_2018_2019`]('./data/sat_snap_2018_2019.csv'): Merged data set
## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*integer*|SAT 2018|Locations in the USA where data has been sampled from| 
|**participation_rate_2018**|*float*|SAT 2018|participation percentage of students who tok the exam| 
|**total_score_2018**|*integer*|SAT 2018|SAT test scores out of 1600|
|**participation_rate_2019**|*float*|SAT 2019|participation percentage of students who tok the exam|
|**total_score_2019**|*integer*|SAT 2019|SAT test scores out of 1600|
|**total_number_of_snap_households_in_thousands_2018**|*integer*|total number of snap households in thousands|
|**number_of_snap_households_with_children_in_thousands_2018**|*integer*|total number of snap households with children in thousands|
|**percentage_of_snap_households_with_children_2018**|*float*|percent of snap households with children|
|**total_number_of_snap_households_in_thousands_2019**|*integer*|total number of snap households in thousands|
|**number_of_snap_households_with_children_in_thousands_2019**|*integer*|total number of snap households with children in thousands|
|**percentage_of_snap_households_with_children_2019**|*float*|percent of snap households with children|

# Data Analysis
## SNAP Households with Children:

The states with the highest percentage of SNAP households with children in 2019 were predominantly from the South and West. Texas led with 53.4%, followed closely by Utah, California, Wyoming, and Arkansas. These states demonstrate a higher reliance on SNAP benefits within households with children, which could be indicative of larger socio-economic challenges in those regions.

## SAT Scores:

Minnesota consistently achieved the highest SAT scores in both 2018 and 2019, indicating a potentially robust education system. Other states with consistently high performance included Wisconsin, North Dakota, Iowa, and Kansas. Conversely, states with consistently low performance, such as West Virginia, District of Columbia, Delaware, Idaho, and Utah may struggle with educational challenges.

## SNAP Households with Children and SAT Scores:

Interestingly, some states like Utah and Idaho were present in both the list of states with high percentages of SNAP households with children and low SAT scores. This intersection could be the focus of more in-depth analysis, potentially indicating areas where socio-economic factors could be impacting educational performance.

However, not all states followed this pattern. For instance, California had a high percentage of SNAP households with children, yet was not among the states with the lowest SAT scores.

## Correlation Analysis:

Our correlation analysis revealed a coefficient of 0, indicating no overall correlation between the percentage of SNAP households with children and SAT scores by state for the years 2018 and 2019. This finding suggests that at the state level, having a higher percentage of SNAP households with children does not directly translate to lower SAT scores, and vice versa.

# Conclusions/Recomendations
There aren't any noticeable relationships between SNAP participation and SAT scores for the years of 2018-2019. Although it's likely because the data used was limited in its ability to establish a clear connection between these two variables. The data examined includes overall state-level SNAP participation and SAT scores, and these are aggregate measures that can encompass a wide range of underlying factors. Both SNAP participation and SAT scores can be influenced by a multitude of socio-economic and educational factors that are not directly measured in the dataset, such as income inequality, quality of education, state educational funding, etc.
To make a more definitive conclusion, it'd be beneficial to have a more granular dataset that includes information at a more local level (such as county or school district), and additional variables that can potentially influence both SNAP participation and SAT scores. For instance, socio-economic indicators like median household income, unemployment rate, education level, and percentage of students receiving free or reduced-price lunch at school could provide more context and allow for a more in-depth analysis.
