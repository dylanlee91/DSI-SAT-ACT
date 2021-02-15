![alt text](https://github.com/dylanlee91/DSI-Ames-Housing/blob/ga_logo.png?raw=true)
# General Assembly Data Science Immersive Project 1: 
### SAT & ACT Analysis & Policy Recommendations to College Board for 2017/2018
## Introduction: How can College Board increase SAT participation rates?
The SAT is a standardised university admissions test administed by College board that competes with the ACT, another standardised test. Many states in the USA make testing mandatory for one of the two tests, while others do not and leave it up to their students to elect to take one or both.

Using the provided dataset that contains data on SAT and ACT average test scores and participation rates by US state for the year 2017 and 2018, an exploratory analysis and visualisation of the data will be constructed, to identify useful qualitative and quantitative relationships in the data between states, test scores, and participation rates.

Once reasonable relationships have been identified, this data will be used to inform a set of recommendations to College Board on appropriate measures to take that can increase SAT participaction rates in the coming years.

### Data Dictionary of the 2017 data
Here is a sample of the SAT and ACT data types for 2017 that are found in the data. A matching set of data from 2018 was also used.

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*string*|The United States|The 50 States of the United States of America as well the District of Columbia.|
|**sat17participation**|*int*|2017 College Board data|Statewide student SAT participation rate as a percentage of total cohort |
|**sat17readwrite**|*int*|2017 College Board data|Statewide mean reading and writing score of the SAT taking cohort in 2017|
|**sat17math**|*int*|2017 College Board data|Statewide mean math score of the SAT taking cohort in 2017|
|**sat17total**|*int*|2017 College Board data|Statewide mean total score of the SAT taking cohort in 2017|
|**act17participation**|*int*|2017 ACT data|Statewide student ACT participation rate as a percentage of total cohort |
|**act17composite**|*float*|2017 ACT data|Statewide mean composite score of the ACT taking cohort in 2017 |
|**act17english**|*float*|2017 ACT data|Statewide mean english score of the ACT taking cohort in 2017 |
|**act17math**|*float*|2017 ACT data|Statewide mean math score of the ACT taking cohort in 2017 |
|**act17reading**|*float*|2017 ACT data|Statewide mean reading score of the ACT taking cohort in 2017 |
|**act17science**|*float*|2017 ACT data|Statewide mean science score of the ACT taking cohort in 2017 |

# Recommendations to College Board for measures to take to increase SAT participation in Midwestern states
It can be observed that every state with below 10% participation in the SAT in both years is relatively rural, with many of these states being in the Midwest. Additionally, not all of these states have >90% participation in the ACT, suggesting that it may not just be statewide policy in these states that causes this.

The first option to College board is to work together with state education boards to pursue policy reform with the intention of making SAT participation mandatory statewide. This was done in Illinois and Colorado and contributed to the two largest positive changes in SAT parcipation observed between 2017 and 2018. It should be noted that this was achieved by College Board submitting better bids than the ACT. It is likely that incentivising state education boards to jump ship with price packages and logistical support will be necessary.

The second option to College Board to increase SAT participation is to increase the marginal attractiveness through of SAT participation by private individuals in states without mandatory participation. The case study of Florida is relevant in this: by improving accessibility of preparatory material, students were both encouraged to take the SAT and better prepared, resulting in both better participation rates and better scores. Additionally, by providing financial incentives in the form of cheaper test taking, students in Florida at the margins were better able to afford to take the test. 
- Other ways to improve accessibility of preperation material
    - Provide travelling workships that visit schools and provide advice on SAT taking
    - Provide more free online material similar to the Khan Academy partnership mentioned in [[*1*]](#[1]-%E2%80%9CSAT,-ACT:-Florida-Students-Lag-behind-National-Averages.%E2%80%9D)
- Improve accessibility of test taking in sparsely populated states
    - It is unlikely to be a coincidence that the states with low SAT participation are all relatively rural. By making test taking more friendly in such states, participation may increase.
- Improve public perception of usefulness of SAT test taking
    - As noted in [[*5*]](#[5]-%E2%80%9CMore-Students-Are-Taking-the-SAT-Than-Ever-Before.%E2%80%9D), College Board needs to address the public perception of class discrimination in testing

### One possible future experiment design for investigation of effectiveness of College Board measures
College Board is already beginning to collect socioeconomic data together with test results, as part of it's commitment to providing relevant socioeconomic data to colleges along with academic results, in order to improve the fairness of admissions decision making.

With a dataset of (anonymised) student identification, test participation and associated socioeconomic status, a time series regression can be designed where the effectiveness of measures that target marginal populations of specific socioeconomic status can be statistically investigated across different sample populations. This is necessary given that the cohort of test takers changes every year. By matching students of socio economic status across time periods, a set of matched samples with approximately equal mean and variance can be formed, enabling statistical testing.

For example, one possible form of the regression could be:

yt=xtß+εt

where:

yt is the change of participation rate in SAT tests of a given sample socioeconomic population in period t        
xtß is the set of interventions in period t that are hypothesized to  affect the participation rate        
εt is an error term

With a more complete data set, a linear regression model could be explored and thus a more robust statistical forecast of the effectiveness of treatment measures that improve SAT participation could be made.

# Appendix
###### Appendix 1: Citations
###### [1] “SAT, ACT: Florida Students Lag behind National Averages.” 
Postal, Leslie. Orlandosentinel.com, Orlando Sentinel, 6 Apr. 2019, www.orlandosentinel.com/news/education/os-ne-act-sat-florida-scores-20181024-story.html.

###### [2] “SAT Scores Rise, as Do the Numbers of Test-Takers.”
POLITICO, 25 Oct. 2018, www.politico.com/newsletters/morning-education/2018/10/25/sat-scores-rise-as-do-the-numbers-of-test-takers-388387.

###### [3]  “Colorado Changed to the SAT in 2017: What You Need to Know.” 
Wheeler, Daniel. Testive, 10 July 2018, www.testive.com/colorado-sat-change-2017/.

###### [4] “Illinois SAT Scores Lag Behind Nation.” 
Antinori, Shannon. Across Illinois, IL Patch, Patch, 29 Oct. 2018, www.patch.com/illinois/across-il/illinois-sat-scores-lag-behind-nation.

###### [5] “More Students Are Taking the SAT Than Ever Before.” 
U.S. News &amp; World Report, U.S. News & World Report, www.usnews.com/news/education-news/articles/2019-09-24/more-students-are-taking-the-sat-than-ever-before.

###### [6] “Harvard Drops the SAT Essay Requirement, What Does This Mean for Your Students?” 
Laet, Katie Rose-De. Applerouth, www.applerouth.com/blog/2018/04/10/harvard-drops-the-sat-essay-requirement-what-does-this-mean-for-your-students/.

###### [7] “File:SAT-ACT-Preference-Map.svg.” 
File:SAT-ACT-Preference-Map.svg - Wikimedia Commons, www.commons.wikimedia.org/wiki/File:SAT-ACT-Preference-Map.svg.

###### [8] “New York City Offers SAT to All High School Juniors, Hoping to Clear a Path to College.” 
Veiga, Christina.Chalkbeat New York, Chalkbeat New York, 3 Apr. 2017, www.ny.chalkbeat.org/2017/4/3/21099704/new-york-city-offers-sat-to-all-high-school-juniors-hoping-to-clear-a-path-to-college.

###### [9] “SAT School Day.” 
SAT Suite of Assessments, 11 May 2018, www.collegereadiness.collegeboard.org/sat/k12-educators/sat-school-day.

###### [10] “SAT School Day.” “More Than 2 Million Students in the Class of 2018 Took the SAT, Highest Ever.” 
The College Board, 18 Mar. 2019, www.collegeboard.org/releases/2018/more-than-2-million-students-in-class-of-2018-took-sat-highest-ever.

###### Appendix 2: External Data Sources
2017 ACT Data 
https://nces.ed.gov/programs/digest/d17/tables/dt17_226.60.asp

2017 SAT Data
https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/

2018 ACT Data
http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf

2018 SAT Data
https://reports.collegeboard.org/pdf/2018-total-group-sat-suite-assessments-annual-report.pdf

https://reports.collegeboard.org/pdf/2018-florida-sat-suite-assessments-annual-report.pdf
