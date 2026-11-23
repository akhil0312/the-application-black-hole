# the-application-black-hole

### Exploratory Recruitment Analytics | Python | Power BI

## Project Overview

Why do some job applications progress to an offer while others remain at earlier stages?

**The Application Black Hole** explores recruitment data to understand application-stage distributions, candidate sources, interview outcomes and offer acceptance patterns.

The project analyses 15,000 applications alongside related candidate, company, job, interview and offer records. It uses Python for data preparation and statistical analysis, and Power BI to present the findings in an interactive dashboard.

> **Important:** This project uses synthetic recruitment data. The findings are exploratory and should not be interpreted as real-world hiring outcomes.

## Objectives

- Understand how applications are distributed across recruitment stages.
- Compare application volumes across different sources.
- Examine offer acceptance across employment types, industries and company sizes.
- Explore whether the time taken to issue an offer differs between accepted and rejected offers.
- Identify patterns while distinguishing statistical significance from practical importance.

## Dataset

**Source:** [Hugging Face – Job Postings & Applications](https://huggingface.co/datasets/mindweave/job-postings-applications)

The dataset contains six related tables:

| Table | Records |
|---|---:|
| Applications | 15,000 |
| Candidates | 9,000 |
| Companies | 320 |
| Interviews | 7,196 |
| Jobs | 2,000 |
| Offers | 938 |
| **Total** | **34,454** |

The tables were connected using their relevant identifiers, including application, candidate, job and company IDs.

## Tools & Technologies

- **Python:** Data cleaning, preparation, merging and exploratory analysis.
- **Pandas:** Data manipulation and aggregation.
- **Statistical analysis:** Chi-square tests and Cramér's V.
- **Power BI:** KPI development, visualisation and dashboard design.

## Key Findings

### 1. Offer Acceptance by Employment Type

- Contract: 82.0% (89 offers)
- Full-time: 74.5% (820 offers)
- Part-time: 51.7% (29 offers)

The overall association between employment type and offer acceptance was statistically significant (p = 0.0051), although the effect size was small (Cramér's V = 0.106).

The part-time category had a relatively small sample, so its result should be interpreted cautiously.

### 2. Offer Acceptance by Industry

- Logistics recorded the highest acceptance rate at 77.5%.
- Retail recorded the lowest at 66.9%.

The overall association was not statistically significant (p = 0.2335).

### 3. Offer Acceptance by Company Size

- Startups: 75.5%
- Enterprise: 75.2%
- Growth companies: 73.2%

Acceptance rates were similar across the three company-size categories. The association was not statistically significant (p = 0.7593).

### 4. Time to Offer

- Accepted offers: 28.74 days on average.
- Rejected offers: 28.58 days on average.

The difference was only 0.16 days, indicating very similar average offer timelines in this dataset.

## Power BI Dashboard

The dashboard contains two pages:

**Page 1 – Recruitment Overview**
- Total applications and offers.
- Offer acceptance rate and accepted offers.
- Application stage distribution.
- Applications by source.
- Offer acceptance by employment type and industry.

**Page 2 – Key Insights**
- Employment type analysis.
- Industry comparison.
- Company-size comparison.
- Time-to-offer analysis.

## Data Preparation & Validation

The analysis included:

- Checking missing values and duplicate records.
- Validating relationships between the six tables.
- Verifying application and offer identifiers.
- Checking calculated time-to-offer values.
- Reviewing statistical associations between selected categories and offer acceptance.

Some fields were excluded from specific analyses where their meaning or data consistency could not be established.

## Limitations

- The dataset is synthetic and does not represent actual recruitment activity.
- Findings are descriptive and do not establish causation.
- Application stages represent recorded stage categories, not a validated sequential conversion funnel.
- Some categories have relatively small sample sizes.
- Salary currency and pay period are not specified in the source data.
- Statistical significance does not necessarily indicate a large or practically important effect.

## Project Takeaway

This project demonstrates an end-to-end analytical workflow: working with related datasets, validating records, preparing analysis-ready data, performing exploratory and statistical analysis, and communicating findings through a Power BI dashboard.

The emphasis is on interpreting data responsibly rather than simply producing visualisations.
