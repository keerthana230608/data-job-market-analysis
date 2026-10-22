# Data Job Market Analysis

An exploratory analysis of 2023 job postings, comparing requested skills, remote-work share, and represented countries across Data Analyst, Senior Data Analyst, Data Scientist, and Senior Data Scientist roles.

## Questions

- Which skills appear most often in each role?
- How do skill requirements differ between analyst and scientist roles?
- What share of postings are marked as remote?
- Which countries are most represented in the analyzed sample?

## Dataset

[Luke Barousse’s data jobs dataset](https://huggingface.co/datasets/lukebarousse/data_jobs), containing 785,741 job postings from 2023.

## Tools and methods

- Python, pandas, matplotlib, and Hugging Face Datasets
- Inspected missing values, data types, and duplicate rows
- Selected four analyst and scientist job-title categories
- Kept postings with non-empty skill information and parsed the skill lists
- Counted each skill once per posting and calculated the percentage of skill-bearing postings mentioning it
- Compared remote-work and country counts using the same skill-bearing subset

The selected roles contributed **362,147** postings with skill information. A check found **101 exact duplicate rows** in the full source dataset; this exploratory run retains them.

## Findings

Among the analyzed skill-bearing postings:

- **Data Analyst:** SQL appeared in **58.0%**, Excel in **41.9%**, and Python in **35.9%**.
- **Senior Data Analyst:** SQL appeared in **71.2%**, Python in **44.4%**, and Tableau in **40.2%**.
- **Data Scientist:** Python appeared in **78.0%**, SQL in **54.2%**, and R in **40.9%**.
- **Senior Data Scientist:** Python appeared in **80.8%**, SQL in **58.0%**, and R in **39.7%**.
- The remote share ranged from **7.2%** for Data Analyst postings to **11.0%** for Senior Data Scientist postings.
- The United States was the most represented country in all four role groups. India was among the top represented countries for Data Scientist roles.

## Limitations

This is a historical 2023 snapshot, not a view of the current job market. Counts describe postings in this dataset, not the full set of jobs available in each country. Skill, remote-work, and country comparisons use postings with non-empty skill information. Exact duplicate source rows were identified but not removed in this exploratory run.

## Run the notebook

Open [job analysis.ipynb](job%20analysis.ipynb) in Google Colab and choose **Runtime → Run all**. The notebook downloads the dataset and regenerates the analysis tables and charts.
