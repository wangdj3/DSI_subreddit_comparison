# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) 




# Project 3: Standardized Test Analysis


---
## Problem Statement

During a recent expedition to the ruins of alpha-Earth, an exploration team recovered a semi-operable server containing data from the popular 21st century website Reddit, with intact data from two notable subreddits: r/anime and r/Naruto.  

Additionally, the team discovered a manual on early 21st century data science techniques for classification and machine learning.  These data remnants were transmitted to my team at the Neo-Earth Research Council for further study.  

Combining the wisdom of these two cultural artifacts, we use these 21st century methods to analyze this 21st century data.  Fascinating, no?  We explored the use of natural language processing and several classification algorithms to differentiate between posts from r/anime vs. those from r/Naruto.  

We present these findings at the 3023 Mars Conference on Pre World War 3 Humanoid Anthropology.  

---
## Data Background

Our study used publicly available data from the California Department of Education regarding:
- ACT performance/participation [1]
- SAT performance/participation [2]
- Overall graduation and college matriculation rates [3]

…for the 2018-2019 school year.

---
## Data Dictionary

#### Shared across ALL datasets
|Feature|Type|Dataset|Description|
|---|---|---|---|
|rtype|object|ACT, SAT, CGR|Record Type: C=County\| D=District\| S=School\| X=State|
|sname|object|ACT, SAT, CGR|School Name\| N/A = County or District Level Record|
|dname|object|ACT, SAT, CGR|District Name\| N/A = County Level Record|
|cname|object|ACT, SAT, CGR|County Name|

#### Originating from the ACT dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|enroll12|float|ACT|Enrollment of Grade 12 (as reported from the ACT data set)|
|num_act_takr|float|ACT|Number of (ACT) Test Takers|
|avg_scr_read|float|ACT|Average ACT Reading Score|
|avg_scr_eng|float|ACT|Average ACT  English Score|
|avg_scr_math|float|ACT|Average ACT Math Score|
|avg_scr_sci|float|ACT|Average ACT Science Score|
|num_ge_21|float|ACT|Number of Test Takers Whose ACT Composite Scores Are Greater or Equal to 21.|
|pct_ge_21|float|ACT|Percent of Test Takers Whose ACT Composite Scores Are Greater or Equal to 21.|
|pct_act_takr|float|ACT|Percent of Grade 12 Enrollees Who Take the ACT|
|||||

#### Originating from the SAT dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|enroll12sat|float|SAT|Enrollment of Grade 12 (as reported from the SAT data set)|
|num_sat_takr12|float|SAT|Number of (SAT) Test Takers Grade 12|
|num_erw_benchmark12|float|SAT|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 12.|
|pct_erw_benchmark12|float|SAT|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12.|
|num_math_benchmark12|float|SAT|The number of students who met or exceeded the benchmark for the New SAT Math test format as of March 2016 for Grade 12.|
|pct_math_benchmark12|float|SAT|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 12.|
|enroll11sat|float|SAT|Enrollment of Grade 11 (as reported from the SAT data set)|
|num_sat_takr11|float|SAT|Number of (SAT) Test Takers Grade 11|
|num_erw_benchmark11|float|SAT|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 11.|
|pct_erw_benchmark11|float|SAT|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 11.|
|num_math_benchmark11|float|SAT|The number of students who met or exceeded the benchmark for the New SAT Math test format as of March 2016 for Grade 11.|
|pct_math_benchmark11|float|SAT|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 11.|
|tot_num_both_benchmark12|float|SAT|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.|
|pct_both_benchmark12|float|SAT|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.|
|tot_num_both_benchmark11|float|SAT|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.|
|pct_both_benchmark11|float|SAT|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.|
|pct_sat_takr12|float|SAT|The percent of 12th graders who took the SAT. = 'num_sat_takr12'/'enroll12sat'|
|||||

#### Originating from the CGR dataset
|Feature|Type|Dataset|Description|
|---|---|---|---|
|completer_type|object|CGR|"AGY = Count of graduates meeting a-g requirements for admission into a University of California (UC) or California State University (CSU) school. AGN = Count of graduates not meeting a-g requirements for admission into a UC or CSU school. NGC = Count of non-graduate completers not meeting a-g requirements for admission into a UC or CSU school. TA = Total (all high school completers)."|
|hs_completers|float|CGR|The number of students who graduated from a California public high school with a regular high school diploma or who otherwise successfully finished high school as a non-graduate completer during the reporting period for the associated academic year |
|enrolled_college_total|float|CGR|The total number of California public high school completers who enrolled in any postsecondary institution within 16 months of completing high school.|
|college_going_rate|float|CGR|The total percentage of California public high school completers who enrolled in any public or private postsecondary institution (in-state or out-of-state) within 16 months of completing high school.|
|not_enrolled_college|float|CGR|The number of California public high school completers (1) who did not enroll in a public or private postsecondary institution inside or outside California within 12 or 16 months of completing high school or (2) whose postsecondary educational directory information records were blocked from being shared by the student or institution pursuant to privacy rights outlined in the Family Educational Rights and Privacy Act (FERPA).|


---
## Primary Findings

- Fairly good correlation suggests that SAT & ACT are in rough agreement about their findings (i.e., how well a given student performs on verbal or math)

- Though they are both “messy” datasets, the tighter clustering (lower variance) on the SAT scores over the ACT scores suggests a stronger correlation (& predicting ability) on whether a student will go to college or not as predicted by meeting benchmark scores on given test.

- There is mild agreement between our metrics and those of U.S. News and World Report for ranking high schools.



### My "Top 10" Lists for as generated using various criteria:

#### Schools
||College-Going Rate|% students meeting SAT benchmarks|% students meeting ACT benchmarks|
|---|---|---|---|
|1|Independence High (Alternative)|William & Marian Ghidotti High|Oxford Academy|
|2|Delta High|Whitney (Gretchen) High|River Valley Charter|
|3|Biggs High|Monta Vista High|Santa Susana High|
|4|South Sutter Charter|Mission San Jose High|Whitney (Gretchen) High|
|5|Selma High|California Academy of Mathematics and Science|Piedmont High|
|6|Emery Secondary|Lynbrook High|Monta Vista High|
|7|Rancho Campana High|Saratoga High|Saratoga High|
|8|Saint Helena High|Oxford Academy|Mission San Jose High|
|9|Lemoore Middle College High|Henry M. Gunn High|Lynbrook High|
|10|Terra Nova High|Northwood High|Canyon Crest Academy|
|||||

#### Districts
||College-Going Rate|% students meeting SAT benchmarks|% students meeting ACT benchmarks|
|---|---|---|---|
|1|Orcutt Union Elementary|La Canada Unified|Lakeside Union Elementary|
|2|South Pasadena Unified|San Marino Unified|Los Gatos-Saratoga Joint Union High|
|3|La Canada Unified|Los Gatos-Saratoga Joint Union High|Santa Cruz County Office of Education|
|4|Temple City Unified|Palo Alto Unified|Piedmont City Unified|
|5|Arcadia Unified|Irvine Unified|Fremont Union High|
|6|Manhattan Beach Unified|South Pasadena Unified|La Canada Unified|
|7|Acalanes Union High|Manhattan Beach Unified|Oak Park Unified|
|8|Oak Park Unified|Davis Joint Unified|Sierra Sands Unified|
|9|Piedmont City Unified|Fremont Union High|Davis Joint Unified|
|10|Palo Alto Unified|Oak Park Unified|Fremont Unified|

---
## Comments/Instructions for Graders

- Initial data grab via API is performed in 'my-project3-getdata.ipynb'

- Datasets are then processed in 'my-project3-data-cleaning.ipynb'

- Cleaned datasets are merged and classified in 'my-project3-classification.ipynb'


---
## Sources & References

#### Dataset Sources

1.  File: [`act_2019_ca.csv`](./data/act_2019_ca.csv) .  “2019 ACT Scores in California by School.” California Department of Education.  ([source] (https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary] (https://web.archive.org/web/20210831222336/https://www.cde.ca.gov/ds/sp/ai/reclayoutact19.asp))

2.  File: [`sat_2019_ca.csv`](./data/sat_2019_ca.csv) . “2019 SAT Scores in California by School.” California Department of Education. ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://web.archive.org/web/20210831212915/https://www.cde.ca.gov/ds/sp/ai/reclayoutsat19.asp))

3.  File: [`cgr16mo19.txt`](./data/cgr16mo19.txt) (Posted 2-Nov-2022). “College-Going Rate for HS Completers (16-month).” California Department of Education.  https://www.cde.ca.gov/ds/ad/filescgr16.asp


<!-- NO?
U.S. Department of Justice (DOJ) Office of Juvenile Justice and Delinquency Prevention (OJJDP)
Easy Access to State and County Juvenile Court Case Counts (EZACO)
https://www.ojjdp.gov/ojstatbb/ezaco/ -->


#### Other References

4. “Largest & Smallest Public School Districts.” California Department of Education. https://www.cde.ca.gov/ds/ad/ceflargesmalldist.asp

5. “Best High Schools in California.” U.S. News & World Report L.P. https://www.usnews.com/education/best-high-schools/california



