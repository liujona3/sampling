# Assignment: Questionnaire Design and Sample Evaluation

## Requirements

The goal of this assignment is to practice developing and evaluating sampling materials.

### Part A - Survey Design:

Select one of the scenarios below and design a survey to meet the need(s) outlined in the prompt.

1.	In two to three sentences, describe the purpose of your survey
2.	Describe your target population, sampling frame, sampling units, and overall sampling strategy.
3.	Write a 5-10 question survey to address your chosen scenario below.

##### Scenarios
1.	You work in the Human Resources Department at a large tech company. Over the past few months, the company has been experiencing a high turnover rate across many of its departments, specifically within the entry- and lower-level positions. The company wishes to understand why this turnover is happening, and what changes need to occur to improve employee satisfaction.
2.	You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
3.	You are a student researcher in the sociology department at the University of Toronto. You are working on a research project that concerns the relationship between music taste and age. This involves both comparisons between different people of different ages and comparisons of the same individual at different ages during their lifetime. You wish to understand to what extent age influences music taste, specifically as it relates to perceptions of popular music. Your results will be written into an academic paper that you hope to publish.

### Part B - Survey Evaluation:

For the **Canadian General Social Survey on Giving, Volunteering, and Participating, 2018 (cycle 33)**, conducted by Statistics Canada find any and all available documentation for the data gathered and identify and describe the survey features indicated below.

1. Sample type
2. Sample size
3. Target population
4. Sampling frame
5. Survey mode(s) 
6. Timeline
7. Response rate
8. Weights
9. Data processing
10. Cleaning, imputation, etc
11. Sources of error
12. Limitations, known biases, etc
13. Link to documentation and any additional sources used


# Your Changes

## Part A - Survey Design: 

The number of your chosen topic: `3`

Describe the purpose of your survey:
```
The purpose of this survey is to investigate if age influences music tastes, specifically how 'popular music' might be perceived across age groups. We aim to compare musical preferences across different age groups in addition to tracking how an individual's music tastes may have changed over time. ```

Describe your target population, sampling frame, sampling units, and observational units:
```
Our target population are adults (18+) in Toronto.

The sampling frame will surveys around the City of Toronto and online in Toronto-related forums. 

The sampling units will be individuals that respond to the survey.

The observational units will also be the indivudals within the survey population. 

Sampling strategy would be to take a non-probability convenience sampling approach. We aim to include participants of various age ranges and stratify them into age groups (18-24, 25-30, 31-35, 36-40, etc.) for comparisons across diffreent age groups. People under the age of 18 will be excluded  Targeted surveys will be posted at various diverse locations across the city such as retirement communites, commercial buildings(work places, malls, etc.), and school related grounds and campuses. We will also aim to recruit through Toronto-related online forums to reach a more diverse set of responses. We will try to include enough participants for each stratum/age group as well. 
```

Your 5-10 question survey:
```
1. What is your age?
2. What is your gender?
3. Where do you currently live?
4. What are your top 3 favourite music genres at the moment? (With rankings 1-3, pop, hiphop, rick, country, jazz, rnb, classical, other [please specify])
5. How would you describe your opinion on current pop music? (Likert-type scale, 1-5, 1 - Very negative and 5 - Very positive)
6. Has your music taste changed over time in terms of genre?
7. What were your favorite genres of music during different times over your life? What are your top 3 favourite music genres at the moment? (For each age group that is applicable for the participant: with rankings 1-3, pop, hiphop, rick, country, jazz, rnb, classical, other [please specify])
8. Do you think your current age infleunces your taste in music?
9. Do you believe people in general tend to be less open to new music as they age? (Likert-type scale, 1-5, 1 - Strongly disagree and 5 - Strongly agree)
```

## Part B - Survey Evaluation:

Identify and describe survey features:

```
1. Sample type
    - probability sampling with stratified design (province CMA level); houses first grouped by telephone numbers, then individuals randomly selected from the house 
    - rejective sampling was also implemented
2. Sample size
    - 50,000 units used
    - 40,000 invitations to electronic questionnaires sent
    - expected 24,000 completed questionnaires
3. Target population
    - All persons 15 years of age and older living in the ten provinces of Canada, excluding full-time residents of institutions
4. Sampling frame
    - A frame consisting of landline and cellular telephone numbers from the Census and administrative sources, including Stats Canada's dwelling frame to enhance coverage of households with telephone access
5. Survey mode(s)
    - Electronic questionnaires
6. Timeline
    - Data collection was from 2018-09-04 to 2018-12-28
7. Response rate
    - 40,000 sent, expected 24,000, so expected response rate was 60% but ended up being 41.9%
8. Weights
    - WGHT_PER - basic weighting factor for analysis at the person level
    - adjusted for the 'rejectin' of a proportion of respondents that are not volunteers by multiplying the person weight by a factor for  respondents that are not 'rejected' and are not volunteers  
9. Data processing
    - Used SSPE set of generalized processing steps for easy processing of the survey with high quality outputs
10. Cleaning, imputation, etc
    - Edits performed automatically and manually at various stages of processing at both macro and micro levels, which include family(relationships to ensure integrity), consistency(series of checks), and flow edits(ensures correct path adn fix offpath situations).
    - Imputations were made using donor records which were selected using a score function
        - If donor imputation could not be used, mean imputation was used via pool of donors
        - Carried out in 9 steps
11. Sources of error
    - Error detection was done through edits programmed into the CATI system
    - Potential sources of errors:
        - sampling error from just a simple sample
        - data processing errors
        - coverage errors, may under represent or over represent
        - non sampling errors
12. Limitations, known biases, etc
    - Non-response bias: perhaps there is a certain demographic that tends to respond to these questionnaires and may be over represented.
    - Exclusion of territories and institutionalized populations limits generalizability to these populations
13. Link to documentation and any additional sources used
    - https://www150.statcan.gc.ca/n1/pub/45-25-0001/index-eng.htm
    - https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&Id=796234

```

## Rubric

-	All required components are present and complete **Complete / Incomplete**
-	Choice of sampling strategy for Part A is justified and related to survey purpose **Complete / Incomplete**
-	Information for Part B is complete and correct **Complete / Incomplete**

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 18/04/2025`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (a2_survey_design_and_evaluation.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
