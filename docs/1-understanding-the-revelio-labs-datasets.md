---
title: "Understanding the Revelio Labs Datasets"
parent: "Accessing and Querying the Revelio Datasets"
layout: default
nav_order: 1
---

### Understanding the Revelio Labs Datasets

Note: Data Dictionaries for the six products listed below can be found [here](https://www.data-dictionary.reveliolabs.com/). The University of Toronto does not license the *Transitions* Dataset.

##### Workforce Dynamics

This dataset provides an overview of a company's composition. This includes headcounts, inflows, and outflows for every unique position, segmented by job, seniority, geography, salary, education, skills, and gender & ethnicity. Coverage is global, from 2007 - 2024.

##### Job Postings

This dataset includes active postings, new postings, removed postings, salaries, and full text of postings for any company, segmented by various employee characteristics (occupation, seniority, geography, keywords, skills, etc). This dataset is pulled from over 350 thousand company websites, all major job boards, and staffing firm job boards. Coverage is global, from 2021-2024.

There are three subfolders within this dataset: *unified, linkedin*, and *indeed.* The unified job postings is comprehensive of all sources and includes linkedin, indeed, companies sites, and other job aggregators. Note however that this folder contains fewer records as records in the *unified* folder have been deduplicated not only across sources but also within sources. So, a post that got posted 5 times on LinkedIn for seemingly the same role would only appear once in the unified postings.

Note also that the University of Toronto does not license the aggregate "Job Postings Dynamic" dataset, but only the individual-level data. Finally, although this is not listed in the data dictionary, these datasets do contain a "description" field with the original job description text, when available.

##### Sentiment

This datasets includes employee reviews for all companies, with the full text of each review split into positive and negative text. Reviews are mapped to various employee characteristics (occupation, seniority, geography). Coverage is global, from 2008-2024.

##### Layoff Notices

This dataset includes post data and effective date for all layoffs in every company in the United States. Coverage is limited to the US, and dates range from 2008-2020 to 2024, depending on the State.

##### Individual Level Data

This datasets contains data on the full professional history of individuals, including their roles, education, skills, gender, ethnicity, salary, seniority, and geography. Coverage is global, from 2008-2024.

##### Company Reference Data

This dataset contains information on companies that are covered by or referenced in the five other datasets listed above.